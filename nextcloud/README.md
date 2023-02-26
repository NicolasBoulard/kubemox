# Nextcloud
Nextcloud is a self hosted service for store data, calendar, etc...

## Install nextcloud using Helm
### Pre-requisites
1. Add helm repo:
   `helm repo add nextcloud https://nextcloud.github.io/helm`
2. `kubectl create ns home`
3. `helm upgrade --install nextcloud nextcloud/nextcloud --namespace home   --values ./nextcloud-values.yaml`
