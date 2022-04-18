##Helm Installation
helm repo add argo https://argoproj.github.io/argo-helm

helm upgrade argocd argo/argo-cd --set server.service.type=LoadBalancer --namespace argo-system --install --create-namespace

helm uninstall argocd --namespace argo-system

Get LoadBalancer ip adddress
kubectl get svc -n argo-system 

get the admin secret from command-line or AKS secrets