# ArgoCD Infra

## Install ArgoCD

- https://argo-cd.readthedocs.io/en/stable/getting_started/

I have already switched the "Type" to "LoadBalancer" on the "argocd-server" service.

## Set Argocd Admin Password

- https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli

For quick copy paste execution:

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```

## Documents

Official Docs:

- https://argo-cd.readthedocs.io/en/stable/user-guide/projects/
- https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/
- https://argo-cd.readthedocs.io/en/stable/user-guide/kustomize/

Re-used Manifests:
- https://github.com/argoproj/argo-cd/tree/stable/manifests
- https://github.com/argoproj/argo-cd/tree/stable/manifests/cluster-install

External References:

- https://stackoverflow.com/questions/63753700/unable-to-patch-service-name-using-kustomize
- https://stackoverflow.com/questions/57594001/how-can-i-create-a-namespace-with-kustomize
- https://elatov.github.io/2021/08/using-kustomize/
- https://github.com/kurtburak/argocd/tree/main/argocd-install
- https://medium.com/devopsturkiye/self-managed-argo-cd-app-of-everything-a226eb100cf0
