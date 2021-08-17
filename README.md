# Aiven Helm Charts

This repository contains official Helm charts that are maintained by [Aiven](https://aiven.io)

## Adding the repository

```bash
helm add repo aiven https://aiven-helm-charts.github.io && helm repo update
```

## Installing a chart from the repository

### Installing the aiven-kubernetes-operator chart

```bash
helm install \
  aiven/aiven-kubernetes-operator \
  --generate-name \
  --namespace aiven-kubernetes-operator-system \
  --create-namespace
```
