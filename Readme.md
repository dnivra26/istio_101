## Steps to install Istio
1. ```kubectl apply -f install/kubernetes/helm/istio/templates/crds.yaml```
2. ```helm install install/kubernetes/helm/istio --name istio --namespace istio-system```
3. Enable Istio Injection
```kubectl create ns servicea```
```kubectl label ns servicea istio-injection=enabled```
