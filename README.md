# Aiven Helm Charts

This repository contains official Helm charts that are maintained by [Aiven](https://aiven.io)

## Adding the repository

```bash
helm repo add aiven https://aiven-helm-charts.github.io && helm repo update
```

## Installing a chart from the repository

### Installing the aiven-kubernetes-operator-crds chart

```bash
helm install aiven/aiven-kubernetes-operator-crds --generate-name
```

### Installing the aiven-kubernetes-operator chart

Before installing the `aiven-kubernetes-operator` chart, please make sure to have the CRDs chart installed.

Installation with webhooks enabled ( requires a cert-manager deployment in the cluster ):

```bash
helm install aiven/aiven-kubernetes-operator --generate-name
```

Without webhooks enabled:

```bash
helm install aiven/aiven-kubernetes-operator --generate-name --set webhooks.enabled=false
```
