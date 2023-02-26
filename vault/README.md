# Vault
Vault

## Install vault using Helm
### Pre-requisites
1. Add helm repo:
   `helm repo add hashicorp https://helm.releases.hashicorp.com`
2. `kubectl create ns vault`
3. `helm install vault hashicorp/vault`
4. `helm upgrade --install vault hashicorp/vault --namespace vault --values ./vault-values.yaml`
5. `helm repo add secrets-store-csi-driver https://kubernetes-sigs.github.io/secrets-store-csi-driver/charts`
6. `helm install csi-secrets-store secrets-store-csi-driver/secrets-store-csi-driver --namespace vault-csi`
7. `kubectl exec vault-0 -- vault operator unseal $VAULT_UNSEAL_KEY`