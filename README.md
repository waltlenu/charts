# Helm Repository

### TL;DR

```bash
$ helm repo add waltlenu https://waltlenu.github.io/charts
$ helm search repo waltlenu
$ helm install my-release waltlenu/<chart>
```

### Prerequisites
- Kubernetes 1.12+
- Helm 3.1.0

### Install Helm

Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured Kubernetes resources.

To install Helm, refer to the [Helm install guide](https://github.com/helm/helm#install) and ensure that the `helm` binary is in the `PATH` of your shell.

### Add Repository

The following command allows you to download and install all the charts from this repository:

```bash
$ helm repo add waltlenu https://waltlenu.github.io/charts
```

### Using Helm

Once you have installed the Helm client, you can deploy Helm Chart into a Kubernetes cluster.

Please refer to the [Quick Start guide](https://helm.sh/docs/intro/quickstart/) if you wish to get running in just a few commands, otherwise the [Using Helm Guide](https://helm.sh/docs/intro/using_helm/) provides detailed instructions on how to use the Helm client to manage packages on your Kubernetes cluster.

Useful Helm Client Commands:
* View available charts: `helm search repo waltlenu`
* Install a chart: `helm install my-release waltlenu/<chart-name>`
* Upgrade your application: `helm upgrade`

