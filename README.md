# Kraken CI

[Kraken CI](https://kraken.ci/) is a modern CI/CD, open-source, on-premise system that is highly scalable and focused on testing.

More details about Kraken CI can be found on https://kraken.ci.

# Kraken CI Helm Charts Repository

This is a Helm repository with Kraken CI charts.
More details can be found on [Artifact Hub](https://artifacthub.io/packages/helm/kraken-ci/kraken-ci).

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/kraken-ci)](https://artifacthub.io/packages/search?repo=kraken-ci)

## Get Repo Info

```console
$ helm repo add kraken-ci https://kraken.ci/helm-repo/charts
$ helm repo update
```

_See [helm repo](https://helm.sh/docs/helm/helm_repo/) for command documentation._

## Install Chart

```console
$ helm install [RELEASE_NAME] kraken-ci/kraken-ci [flags]
```

Example:

```console
$ helm install --create-namespace --namespace kraken --debug --wait kraken-ci kraken-ci/kraken-ci --version 0.753.0
```

This command installs version 0.753 of Kraken CI in a `kraken` namespace.

_See [configuration](#configuration) below._

_See [helm install](https://helm.sh/docs/helm/helm_install/) for command documentation._

## Uninstall Chart

```console
$ helm uninstall [RELEASE_NAME]
```

This removes all the Kubernetes components associated with the chart and deletes the release.

_See [helm uninstall](https://helm.sh/docs/helm/helm_uninstall/) for command documentation._

## Upgrade Chart

```console
$ helm upgrade [RELEASE_NAME] kraken-ci/kraken-ci [flags]
```

Example:

```console
$ helm upgrade  --install --create-namespace --namespace kraken --debug --wait kraken-ci kraken-ci/kraken-ci --version 0.757.0
```

This command upgrades or installs Kraken Ci to 0.757 version in `kraken` namespace.

_See [helm upgrade](https://helm.sh/docs/helm/helm_upgrade/) for command documentation._


## Configuration

See [Customizing the Chart Before Installing](https://helm.sh/docs/intro/using_helm/#customizing-the-chart-before-installing).
To see all configurable options with detailed comments, visit the chart's [values.yaml](./values.yaml), or run these configuration commands:

```console
$ helm show values kraken-ci/kraken-ci
```
