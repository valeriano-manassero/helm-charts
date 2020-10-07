# Valeriano Manassero Helm Charts Library for Kubernetes

Popular applications, provided by [Valeriano Manassero](https://github.com/valeriano-manassero), ready to launch on Kubernetes using [Kubernetes Helm](https://github.com/helm/helm).

## Requirements

### Setup a Kubernetes Cluster

For setting up Kubernetes on various platforms refer to the Kubernetes [getting started guide](http://kubernetes.io/docs/getting-started-guides/).

### Install Helm

Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured Kubernetes resources.

To install Helm, refer to the [Helm install guide](https://github.com/helm/helm#install) and ensure that the `helm` binary is in the `PATH` of your shell.

## Usage

```bash
$ helm repo add valeriano-manassero https://valeriano-manassero.github.io/helm-charts
$ helm search repo valeriano-manassero
$ helm install my-release valeriano-manassero/<chart>
```
