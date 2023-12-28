# K8ssandra Cluster Sample Helm Chart

This chart bootstraps a [K8ssandra](https://k8ssandra.io) cluster on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager. It assumes that you already have [K8ssandra Operator](https://github.com/k8ssandra/k8ssandra-operator) installed. This is implemented as a reference implementation with the expectation that it will be forked and customized to fit individual user needs. Contributions are welcome!

## Pre-requisites

1. [Helm](https://helm.sh/)
2. [Cert-Manager](https://cert-manager.io/) - `helm install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace --version v1.13.3 --set installCRDs=true`
3. [K8ssandra Operator](https://k8ssandra.io/) - `helm install k8ssandra-operator k8ssandra/k8ssandra-operator -n k8ssandra-operator --create-namespace --set global.clusterScoped=true`

## Installation

Create your own `values.yaml` file based on the [sample](./values.yaml) and then install the chart:

```console
git clone https://github.com/k8ssandra/k8ssandra-cluster.git
helm install k8ssandra-cluster ./k8ssandra-cluster -f values.yaml
```
