# Aiven Charts

This repository contains official Helm charts that are maintained by [Aiven](https://aiven.io)

## Adding the repository

```bash
helm repo add aiven aiven https://aiven.github.io/aiven-charts && helm repo update
```

## Installing a chart from the repository

### Installing the aiven-operator-crds chart

```bash
helm install aiven-operator-crds aiven/aiven-operator-crds
```

### Installing the aiven-operator chart

Before installing the `aiven-operator` chart, please make sure to have the CRDs chart installed.

Installation with webhooks enabled ( requires a cert-manager deployment in the cluster ):

```bash
helm install aiven-operator aiven/aiven-operator
```

Without webhooks enabled:

```bash
helm install aiven-operator aiven/aiven-operator --set webhooks.enabled=false
```
