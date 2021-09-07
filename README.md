# flux2-kustomize-multi-env-example

[![e2e](https://github.com/kharf/fluxv2-pg/actions/workflows/e2e.yaml/badge.svg)](https://github.com/kharf/fluxv2-pg/actions/workflows/e2e.yaml)

This example uses Flux and Kustomize to minimize duplicated configurations for a multi environment scenario.

## Testing

Any change to the Kubernetes manifests or to the repository structure should be validated in CI before
a pull requests is merged into the main branch and synced on the cluster.

This repository contains the following GitHub CI workflows:

* the [e2e](./.github/workflows/e2e.yaml) workflow validates the Kubernetes manifests and Kustomize overlays with kubeval and starts a Kubernetes cluster in CI and tests the staging setup by running Flux in Kubernetes Kind

## Special Thanks
 - [flux2-kustomize-helm-example](https://github.com/fluxcd/flux2-kustomize-helm-example) maintainers for providing a really good template