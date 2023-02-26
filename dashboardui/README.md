# Kubernetes Dashboard UI
The Dashboard UI is not deployed by default. To deploy it, run the following command:

`kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml`

You can enable access to the Dashboard using the kubectl command-line tool, by running the following command:

`kubectl proxy`

Kubectl will make Dashboard available at http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/

# Generate a token on Dashboard UI

1. `kubectl apply -f dashboardui-serviceAccount.yaml`
2. `kubectl -n kubernetes-dashboard create token admin-user`