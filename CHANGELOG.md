# Changelog

## [4.1.2](https://github.com/Jmainguy/helm-webapp/compare/helm-webapp-v4.1.1...helm-webapp-v4.1.2) (2026-08-23)


### Bug Fixes

* **ci:** authenticate Notation without credential store ([3e2cff5](https://github.com/Jmainguy/helm-webapp/commit/3e2cff5fefbb28f2b7bdf2d8d650ad4ddd9f79e6))

## [4.1.1](https://github.com/Jmainguy/helm-webapp/compare/helm-webapp-v4.1.0...helm-webapp-v4.1.1) (2026-08-23)


### Bug Fixes

* **ci:** use supported Notation CLI version ([7a1abc1](https://github.com/Jmainguy/helm-webapp/commit/7a1abc107b7f1be7a4bc9ca17cf4e3b80ed66370))

## [4.1.0](https://github.com/Jmainguy/helm-webapp/compare/helm-webapp-v4.0.1...helm-webapp-v4.1.0) (2026-08-23)


### Features

* **ci:** sign releases with Notation ([00f8fbd](https://github.com/Jmainguy/helm-webapp/commit/00f8fbde086fe4064b0092cb6983caa8ce49cd48))

## [4.0.1](https://github.com/Jmainguy/helm-webapp/compare/helm-webapp-v4.0.0...helm-webapp-v4.0.1) (2026-08-23)


### Bug Fixes

* **ci:** authenticate Cosign to Zot ([cf04578](https://github.com/Jmainguy/helm-webapp/commit/cf04578c08b942209fa87dac5d5bcd2c02fd674b))

## [4.0.0](https://github.com/Jmainguy/helm-webapp/compare/helm-webapp-v3.3.0...helm-webapp-v4.0.0) (2026-08-23)


### ⚠ BREAKING CHANGES

* the chart is now published as zot.soh.re/jmainguy/helm-webapp.
* BREAKING CHANGE updated pvc to persistence
* add configmaps, change cluster to postgres

### Features

* add configmaps, change cluster to postgres ([55a29f2](https://github.com/Jmainguy/helm-webapp/commit/55a29f246209693c24fa10c203d6eac3988f5fb8))
* add optional in-cluster Redis (Chainguard) ([789a515](https://github.com/Jmainguy/helm-webapp/commit/789a51556bfd35fd2eedc77d176c4fb94629cd3d))
* add postgres database feature ([58cf911](https://github.com/Jmainguy/helm-webapp/commit/58cf9117c53bbded2d21e9fd318bf3763a6dc1be))
* add pvc ([a8418c8](https://github.com/Jmainguy/helm-webapp/commit/a8418c84cec17de175bc558e573da52fb2df61e6))
* adopt canonical OCI chart name ([e27e2da](https://github.com/Jmainguy/helm-webapp/commit/e27e2dafd144cab12b441731a05f76d7f830a45e))
* BREAKING CHANGE updated pvc to persistence ([15adf67](https://github.com/Jmainguy/helm-webapp/commit/15adf67ca90ddf740b188631321130cfc8049ab5))
* **ci:** sign labeled Helm releases with Cosign ([453ecd3](https://github.com/Jmainguy/helm-webapp/commit/453ecd3e7bb6ffd8ea5adc9cba131e6f7a545f29))
* initial version of chart ([37ae8b3](https://github.com/Jmainguy/helm-webapp/commit/37ae8b3da93b13757f5e8552c9ce95cd6d929e76))
* support arbitrary env variables ([2918597](https://github.com/Jmainguy/helm-webapp/commit/29185975f196b8b44ae47bd08ce4253eafbc496d))
* support readWriteMany for pvc ([8baebb6](https://github.com/Jmainguy/helm-webapp/commit/8baebb61d969dae5a8203207a87230cce57df39f))
* support secrets ([cd6b6bd](https://github.com/Jmainguy/helm-webapp/commit/cd6b6bd9bb9cf4b8ef485ea36b2e7bdb29c58e1c))
* support tls certs and www redirect ([e46ca22](https://github.com/Jmainguy/helm-webapp/commit/e46ca22ab1dfd4a4874542abda386e9215f0234b))
* trigger release because zot deleted everything ([2aae02b](https://github.com/Jmainguy/helm-webapp/commit/2aae02bd60fc04aeeb754aefb1d682c1912678d2))


### Bug Fixes

* **ci:** push helm charts to zot.soh.re with DOCKER credentials ([7300af5](https://github.com/Jmainguy/helm-webapp/commit/7300af58e6b41ad9f62ff008f5534f1e4847af3c))
* redirect at vs level ([991088a](https://github.com/Jmainguy/helm-webapp/commit/991088a3300a7588797bde7a20ba3e6236d1cc4a))
* repository and name ([536d041](https://github.com/Jmainguy/helm-webapp/commit/536d0414b628124f5d9fef5e8cf3b6f9470e49ad))
* set default secret to not mount ([608f8f6](https://github.com/Jmainguy/helm-webapp/commit/608f8f682853677340b79c22b9ef73a43c8ed8cd))
* use redirect in vs ([c5a388a](https://github.com/Jmainguy/helm-webapp/commit/c5a388a2a7c0a7aed0b460347c38a981b5706ef3))
* use standard names ([8e7afe5](https://github.com/Jmainguy/helm-webapp/commit/8e7afe53d0895ba6615faf2ba843dd8c994e365e))


### Reverts

* restore HELM_* release workflow ([988d0a2](https://github.com/Jmainguy/helm-webapp/commit/988d0a279dafdcb4eb72bdb90aeb77c2c5c9c084))

## [3.3.0](https://github.com/Jmainguy/helm-webapp/compare/webapp-v3.2.1...webapp-v3.3.0) (2026-08-23)


### Features

* **ci:** sign labeled Helm releases with Cosign ([453ecd3](https://github.com/Jmainguy/helm-webapp/commit/453ecd3e7bb6ffd8ea5adc9cba131e6f7a545f29))

## [3.2.1](https://github.com/Jmainguy/helm-webapp/compare/webapp-v3.2.0...webapp-v3.2.1) (2026-08-02)


### Bug Fixes

* **ci:** push helm charts to zot.soh.re with DOCKER credentials ([7300af5](https://github.com/Jmainguy/helm-webapp/commit/7300af58e6b41ad9f62ff008f5534f1e4847af3c))


### Reverts

* restore HELM_* release workflow ([988d0a2](https://github.com/Jmainguy/helm-webapp/commit/988d0a279dafdcb4eb72bdb90aeb77c2c5c9c084))

## [3.2.0](https://github.com/Jmainguy/helm-webapp/compare/webapp-v3.1.0...webapp-v3.2.0) (2026-08-02)


### Features

* add optional in-cluster Redis (Chainguard) ([789a515](https://github.com/Jmainguy/helm-webapp/commit/789a51556bfd35fd2eedc77d176c4fb94629cd3d))

## [3.1.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v3.0.0...webapp-v3.1.0) (2026-02-28)


### Features

* support readWriteMany for pvc ([8baebb6](https://github.com/Standouthost/helm-webapp/commit/8baebb61d969dae5a8203207a87230cce57df39f))

## [3.0.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.4.0...webapp-v3.0.0) (2026-02-22)


### ⚠ BREAKING CHANGES

* BREAKING CHANGE updated pvc to persistence

### Features

* BREAKING CHANGE updated pvc to persistence ([15adf67](https://github.com/Standouthost/helm-webapp/commit/15adf67ca90ddf740b188631321130cfc8049ab5))

## [2.4.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.3.2...webapp-v2.4.0) (2025-11-10)


### Features

* trigger release because zot deleted everything ([2aae02b](https://github.com/Standouthost/helm-webapp/commit/2aae02bd60fc04aeeb754aefb1d682c1912678d2))

## [2.3.2](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.3.1...webapp-v2.3.2) (2024-10-27)


### Bug Fixes

* use redirect in vs ([c5a388a](https://github.com/Standouthost/helm-webapp/commit/c5a388a2a7c0a7aed0b460347c38a981b5706ef3))

## [2.3.1](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.3.0...webapp-v2.3.1) (2024-10-27)


### Bug Fixes

* redirect at vs level ([991088a](https://github.com/Standouthost/helm-webapp/commit/991088a3300a7588797bde7a20ba3e6236d1cc4a))

## [2.3.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.2.0...webapp-v2.3.0) (2024-10-27)


### Features

* support tls certs and www redirect ([e46ca22](https://github.com/Standouthost/helm-webapp/commit/e46ca22ab1dfd4a4874542abda386e9215f0234b))

## [2.2.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.1.0...webapp-v2.2.0) (2024-10-24)


### Features

* add pvc ([a8418c8](https://github.com/Standouthost/helm-webapp/commit/a8418c84cec17de175bc558e573da52fb2df61e6))

## [2.1.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v2.0.0...webapp-v2.1.0) (2024-10-24)


### Features

* support arbitrary env variables ([2918597](https://github.com/Standouthost/helm-webapp/commit/29185975f196b8b44ae47bd08ce4253eafbc496d))

## [2.0.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v1.2.0...webapp-v2.0.0) (2024-10-23)


### ⚠ BREAKING CHANGES

* add configmaps, change cluster to postgres

### Features

* add configmaps, change cluster to postgres ([55a29f2](https://github.com/Standouthost/helm-webapp/commit/55a29f246209693c24fa10c203d6eac3988f5fb8))

## [1.2.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v1.1.1...webapp-v1.2.0) (2024-10-22)


### Features

* add postgres database feature ([58cf911](https://github.com/Standouthost/helm-webapp/commit/58cf9117c53bbded2d21e9fd318bf3763a6dc1be))

## [1.1.1](https://github.com/Standouthost/helm-webapp/compare/webapp-v1.1.0...webapp-v1.1.1) (2024-10-17)


### Bug Fixes

* set default secret to not mount ([608f8f6](https://github.com/Standouthost/helm-webapp/commit/608f8f682853677340b79c22b9ef73a43c8ed8cd))

## [1.1.0](https://github.com/Standouthost/helm-webapp/compare/webapp-v1.0.2...webapp-v1.1.0) (2024-10-17)


### Features

* support secrets ([cd6b6bd](https://github.com/Standouthost/helm-webapp/commit/cd6b6bd9bb9cf4b8ef485ea36b2e7bdb29c58e1c))

## [1.0.2](https://github.com/Standouthost/helm-webapp/compare/webapp-v1.0.1...webapp-v1.0.2) (2024-10-17)


### Bug Fixes

* repository and name ([536d041](https://github.com/Standouthost/helm-webapp/commit/536d0414b628124f5d9fef5e8cf3b6f9470e49ad))

## [1.0.1](https://github.com/Standouthost/helm-webapp/compare/webapp-v1.0.0...webapp-v1.0.1) (2024-10-16)


### Bug Fixes

* use standard names ([8e7afe5](https://github.com/Standouthost/helm-webapp/commit/8e7afe53d0895ba6615faf2ba843dd8c994e365e))

## 1.0.0 (2024-10-16)


### Features

* initial version of chart ([37ae8b3](https://github.com/Standouthost/helm-webapp/commit/37ae8b3da93b13757f5e8552c9ce95cd6d929e76))
