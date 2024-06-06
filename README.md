![kuberise logo](docs/images/kuberise%20logo1%20-%20horizontal.png)
# Kuberise

Kuberise is a free opensource internal developer platform for Kubernetes environment. The goal is to provide tools and templates in Kubernetes environment by a fast and easy installation to help developers focus on the development of the business applications rather than installation and configuration of side tools and preparations of the environments and automation.

## Prerequisites

- CLI tools: kubectl, helm, htpasswd, git
- A Github account or another git repository system
- [K9s](https://k9scli.io/topics/install/) for dashboard (recommended)
- A [minikube](https://minikube.sigs.k8s.io/docs/start) kubernetes cluster for local installation (`minikube start`)

## Installation

1. Fork the current repository [https://github.com/kuberise/kuberise](https://github.com/kuberise/kuberise) into your Github account, or clone and push it to your other git repository.
2. Run these commands (first modify the url of the repository to point to your new repository):

```bash
export repoURL=https://github.com/[yourUserName]/kuberise.git
git clone $repoURL
cd kuberise

export CONTEXT=$(kubectl config current-context)
export ADMIN_PASSWORD=admin
export PG_SUPERUSER_PASSWORD=admin

./scripts/install.sh $CONTEXT local $repoURL main
```

To read more please refer to the [docs here](docs/README.md)
