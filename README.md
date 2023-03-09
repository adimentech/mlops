# MLOps

Easy ML platform

## Local run with kind
```shell
kind create cluster --name mlops --config kind-config.yaml
```

## Bootstrap Flux
```shell
flux bootstrap github --owner=adimentech \
  --repository=mlops --branch=main --path=/gitops/ --verbose
```
#### Dependency management
HelmRelease has dependsOn - configure if your chart depends on another one
Kustomization has the same
If you need CRs, place them in apps directory, and instal CRDs in infrastructure

export OIDC_CLIENT_ID="mlops-oidc"
export OIDC_CLIENT_SECRET="vc2z5KIJagIh4XCpNoEszXMWBujGeRBu"