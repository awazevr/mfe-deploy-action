# mfe-deploy-action
This is a GitHub Action meant to be used as a [composite action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action) within an existing workflow. This action encapsulates the steps necessary to deploy an Awaze MFE.

The action encapsulates the following other actions:

- [benjlevesque/short-sha](https://github.com/benjlevesque/short-sha)
- [aws-actions/configure-aws-credentials](https://github.com/aws-actions/configure-aws-credentials)
- [actions/download-artifact](https://github.com/actions/download-artifact)



## Inputs

### `aws-access-key-id`

**Required** The associated AWS Secret Key Id for a given AWS Account.

### `aws-secret-access-key`

**Required** The associated AWS Secret Access Key for a given AWS Account. 

### `submodules_pat`

**Required** The PAT Access token required to access the submodules repository.

### `aws-region`

**Required** Specifies the AWS Region to use.

### `new-relic-api-key`

**Required** Specifies the New Relic API Key to use.

### `new-relic-region`

**Required** Specifies the New Relic Region to use.

### `new-relic-application-id`

**Required** Specifies the New Relic Application Id to use.

### `new-relic-account-id`

**Required** Specifies the New Relic account to use.

### `app-name`

**Required** The programatic name of your MFE

### `is-initial-environment`

Specifies if the environment you're deploying to is your first environment (e.g. dev), determines if ECR 'promote from previous environment' steps need to be run or not.

### `source-ecr`

If you're promoting from a previous environment (e.g. dev -> pprd), the ECR repo that contains the image you wish to promote.

### `destination-ecr`

If you're promoting from a previous environment (e.g. dev -> pprd), the ECR repo that you wish to promote the image to.




## Usage
You can use this composite Action in your own workflow by adding:

```yml
name: search-mfe-composite

on:
  push:
    branches: [ main ]

  workflow_dispatch:

jobs:
  deploy_dev:
    environment: dev
    runs-on: ubuntu-latest

    steps:
      - name: Deploy dev
        uses: awazevr/mfe-deploy-action@v1.0.0
        with:
          app-name: search-mfe
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: eu-west-2
          submodules-pat: ${{ secrets.SUBMODULE_PAT }}
          new-relic-api-key: ${{ secrets.NEW_RELIC_API_KEY }}
          new-relic-region: ${{ secrets.NEW_RELIC_REGION }}
          new-relic-application-id: ${{ secrets.NEW_RELIC_APPLICATION_ID }}
          new-relic-account-id: ${{ secrets.NEW_RELIC_ACCOUNT_ID }}
          is-initial-environment: true
          
  deploy_pprd:
    environment: pprd
    runs-on: ubuntu-latest

    steps:
      - name: Deploy pprd
        uses: awazevr/mfe-deploy-action@v1.0.0
        with:
          app-name: search-mfe
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: eu-west-2
          submodules-pat: ${{ secrets.SUBMODULE_PAT }}
          new-relic-api-key: ${{ secrets.NEW_RELIC_API_KEY }}
          new-relic-region: ${{ secrets.NEW_RELIC_REGION }}
          new-relic-application-id: ${{ secrets.NEW_RELIC_APPLICATION_ID }}
          new-relic-account-id: ${{ secrets.NEW_RELIC_ACCOUNT_ID }}
          source-ecr: 12345678.dkr.ecr.eu-west-2.amazonaws.com/mfe-repo
          destination-ecr: 87654321.dkr.ecr.eu-west-2.amazonaws.com/mfe-repo

```

