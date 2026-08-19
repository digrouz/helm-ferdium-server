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

- `image.repository`, `image.tag`, `image.pullPolicy` for the container image
- `config.db.*` for the database (sqlite, mysql, postgres)
- `config.smtp.*` for SMTP mail delivery
- `persistence.data.*` / `persistence.recipes.*` for persistent storage
- `ingress.webui.*` for ingress setup (host, TLS, annotations)
- `service.type` / `service.port` for the Service
- `probes.*` to enable/disable and tune liveness/readiness/startup probes
- `resources` for CPU/memory requests and limits
- `podSecurityContext` / `securityContext` for pod and container security settings

## Uninstallation

```sh
helm uninstall ferdium-server
```
