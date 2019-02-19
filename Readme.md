## Steps to install Istio  
1. ```kubectl apply -f install/kubernetes/helm/istio/templates/crds.yaml```  
2. ```helm install install/kubernetes/helm/istio --name istio --namespace istio-system```  
3. Enable Istio Injection  
```kubectl create ns servicea```  
```kubectl label ns servicea istio-injection=enabled```  
4. Deploy the services  
```helm upgrade --install servicea ./servicea --namespace servicea```  
```helm upgrade --install serviceb ./serviceb --namespace serviceb```  
```helm upgrade --install servicec ./servicec --namespace servicec```  

### Service Diagram
![service diagram](https://raw.githubusercontent.com/dnivra26/istio_101/master/service_diagram_istio.png)