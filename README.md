# helm-ferdium-server
  
A Helm chart for deploying [Ferdium Server](https://github.com/ferdium/ferdium-server) on Kubernetes.

## Features

- Easy deployment and management of Ferdium Server
- Configurable environment variables
- Persistent storage support
- Ingress configuration

## Prerequisites

- Kubernetes cluster
- Helm 3.x installed

## Installation

```sh
helm repo add myrepo https://example.com/helm-charts
helm install ferdium-server myrepo/helm-ferdium-server
```

## Configuration

You can customize the deployment by editing the `values.yaml` file or using `--set` flags. Common options include:

- `image.repository` and `image.tag`
- `env` for environment variables
- `persistence.enabled` for persistent storage
- `ingress.enabled` for ingress setup

## Uninstallation

```sh
helm uninstall ferdium-server
```
