# [1.1.0](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.13...v1.1.0) (2022-03-23)


### Bug Fixes

* **CHECK-364:** bash syntax ([693c3ee](https://github.com/awazevr/mfe-deploy-action/commit/693c3eeb1fb72ff2dc041e2fa8b0900c2dcd3e3c))
* **CHECK-364:** check the value of the new param is true ([965fdea](https://github.com/awazevr/mfe-deploy-action/commit/965fdeaf3f3b902c07bf401248322e79ed119991))
* **CHECK-364:** don't wait for the task to start ([bcb828a](https://github.com/awazevr/mfe-deploy-action/commit/bcb828acf870d25b34b707ff0cca7b5cfeb2ef54))
* **CHECK-364:** echo ([477e4ac](https://github.com/awazevr/mfe-deploy-action/commit/477e4aca6dc8e598288a10abe3e28dd98958502b))
* **CHECK-364:** output raw value from jq ([c0c8e78](https://github.com/awazevr/mfe-deploy-action/commit/c0c8e78eeaad27efe2a90b3e644fda791d811050))
* **CHECK-364:** rename parameter name to match input ([6995233](https://github.com/awazevr/mfe-deploy-action/commit/699523396953de771b93d6d052342684e7cd71f5))
* **CHECK-364:** TEMP - comment out the new relic deployment martker step ([5eb7859](https://github.com/awazevr/mfe-deploy-action/commit/5eb78596ca8a7f508f5790b08bf2efe2c1c29f31))
* **CHECK-364:** typo ([14ed467](https://github.com/awazevr/mfe-deploy-action/commit/14ed46732d458153be1b1a37b7d66ddb20a72487))
* **CHECK-364:** use a action tag ([5c958fe](https://github.com/awazevr/mfe-deploy-action/commit/5c958fef81a847e3c128ca2b7ad0ef436662981e))
* **CHECK-364:** use single quotes ([2e77273](https://github.com/awazevr/mfe-deploy-action/commit/2e77273e56de2fd617afc7aef6c94b4f805edd72))


### Features

* **CHECK-364:** Make new relic deployment marker step optional ([c2fc20f](https://github.com/awazevr/mfe-deploy-action/commit/c2fc20f1ab44686da8749a3bb1ff3cb7ff44f71c))
* **CHECK-364:** Move AWS config to using IAM role ([824db86](https://github.com/awazevr/mfe-deploy-action/commit/824db86fb40ad664d6f5a503c36347a8504d9b8b))
* **CHECK-364:** mutate task definition and deploy it ([5037900](https://github.com/awazevr/mfe-deploy-action/commit/50379004c69d70925031c2e4b828a8f5ff7059d7))
* **CHECK-364:** output only the task definition not the wrapper ([3be6dee](https://github.com/awazevr/mfe-deploy-action/commit/3be6deef2b1c3c6b091ba1c3decb911967114edf))
* **CHECK-364:** parameterise the ecs deploy inputs ([2779678](https://github.com/awazevr/mfe-deploy-action/commit/2779678fca3fdad5424b4a2b370de0b9d38074bb))
* **CHECK-364:** print task definition to output ([9639b7c](https://github.com/awazevr/mfe-deploy-action/commit/9639b7cf31cdf49859756551e3da46598e5cb602))
* **CHECK-364:** remove ignored properties from task definition ([2db605c](https://github.com/awazevr/mfe-deploy-action/commit/2db605c14c85eeef566bc4c6f9866163b67f8406))
* **CHECK-364:** start replacing deploy.sh with internal action script ([e487eb5](https://github.com/awazevr/mfe-deploy-action/commit/e487eb531fad0ea61f79741c87955881663f4c1b))
* **CHECK-364:** try not using the mfe-infrastructure submodule as a working dir ([5eda160](https://github.com/awazevr/mfe-deploy-action/commit/5eda160a26570f60066235200c893aa7fd58692b))
* **CHECK-364:** wait for ecs to deploy ([f940b0b](https://github.com/awazevr/mfe-deploy-action/commit/f940b0ba7a8effd807b31dcf1ddc09ef51a259fa))


### BREAKING CHANGES

* **CHECK-364:** - makes the destination-ecr input required

Co-authored-by: Dzhakov, Kristiyan <Kristiyan.Dzhakov@awaze.co.uk>

## [1.0.13](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.12...v1.0.13) (2022-01-20)


### Bug Fixes

* Revert unnecessary guard on promote steps ([2d7d998](https://github.com/awazevr/mfe-deploy-action/commit/2d7d9988de1e39bb6a2a289cf3196b6b5e030e33))

## [1.0.12](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.11...v1.0.12) (2022-01-20)


### Bug Fixes

* Add git-sha as optional input ([52b3337](https://github.com/awazevr/mfe-deploy-action/commit/52b33373cc8a00c46953297fc1b891aea26c5419))

## [1.0.11](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.10...v1.0.11) (2022-01-20)


### Bug Fixes

* reference inputs rather than missing env for promote ([773efe1](https://github.com/awazevr/mfe-deploy-action/commit/773efe1eb165335cdc773afa2eab53b06e94ec0d))

## [1.0.10](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.9...v1.0.10) (2022-01-20)


### Bug Fixes

* new relic application id invalid reference ([bcae805](https://github.com/awazevr/mfe-deploy-action/commit/bcae80587562144892c55a1b2f4f6e958da8edab))

## [1.0.9](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.8...v1.0.9) (2022-01-20)


### Bug Fixes

* environment input not being correctly templated ([b2ebb54](https://github.com/awazevr/mfe-deploy-action/commit/b2ebb5423a17f449def237fd3c93a7c5ca970157))

## [1.0.8](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.7...v1.0.8) (2022-01-20)


### Bug Fixes

* More syntax errors ([b7ef8fc](https://github.com/awazevr/mfe-deploy-action/commit/b7ef8fc43f39d21452ca47fff9f65701985a5d62))

## [1.0.7](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.6...v1.0.7) (2022-01-19)


### Bug Fixes

* More indentation issues ([7c0919d](https://github.com/awazevr/mfe-deploy-action/commit/7c0919dff8109d9f8e4d99363ed3102bd6ab2aa8))

## [1.0.6](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.5...v1.0.6) (2022-01-19)


### Bug Fixes

* indentation issues ([e6b7d87](https://github.com/awazevr/mfe-deploy-action/commit/e6b7d876dbeb178c8caa8727dc81d792c5d3e4dc))

## [1.0.5](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.4...v1.0.5) (2022-01-19)


### Bug Fixes

* **MFE-6:** Update input descriptions and required flags ([26a96c4](https://github.com/awazevr/mfe-deploy-action/commit/26a96c430fd0511833c9d3c385cf982d1f8116aa))

## [1.0.4](https://github.com/awazevr/mfe-deploy-action/compare/v1.0.3...v1.0.4) (2022-01-19)


### Bug Fixes

* Update action name ([e5d5022](https://github.com/awazevr/mfe-deploy-action/commit/e5d5022036ff22b85f9b10c7a922ee9d7b0cce00))

## [1.0.3](https://github.com/awazevr/mfe-deploy-pprd-action/compare/v1.0.2...v1.0.3) (2022-01-19)


### Bug Fixes

* **MFE-6:** Refactor to make environment and mfe agnostic ([7e4620c](https://github.com/awazevr/mfe-deploy-pprd-action/commit/7e4620cfab08b72b0bb46a09f0ad9b5823e2d100))

## [1.0.2](https://github.com/awazevr/mfe-deploy-pprd-action/compare/v1.0.1...v1.0.2) (2022-01-17)


### Bug Fixes

* **MFE-3:** renoved hard-coded destination ecr as it is now an input parameter ([7967b68](https://github.com/awazevr/mfe-deploy-pprd-action/commit/7967b682dd2c8b9c73f0c60d48a5ce79f71c2428))

## [1.0.1](https://github.com/awazevr/mfe-deploy-pprd-action/compare/v1.0.0...v1.0.1) (2022-01-17)


### Bug Fixes

* **MFE-3:** parameterised the deployment environment ([3b8c069](https://github.com/awazevr/mfe-deploy-pprd-action/commit/3b8c069e4eac717613ddd46e2af5c5ace6bfcc1a))

# 1.0.0 (2022-01-14)


### Features

* **MFE-3:** initial commit for this action ([ac7cb20](https://github.com/awazevr/mfe-deploy-pprd-action/commit/ac7cb200d2ef6e5dfe97a55be540b3114d3ca30c))
