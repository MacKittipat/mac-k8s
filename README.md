# mac-k8s-sample 

## Basic command 
```
kubectl cluster-info

kubectl get nodes
kubectl get replicaset
kubectl get services
kubectl get deploy

kubectl describe node ${NODE_NAME}
kubectl describe pods ${POD_NAME}
kubectl describe service ${SERVICE_NAME}
kubectl describe deploy ${DEPLOY_NAME}

kubectl exec -it ${POD_NAME} -- sh

kubectl logs -f ${POD_NAME}
kubectl logs -f -l app=mac-nginx
```

## Pod 
```
kubectl apply -f pod-nginx.yml
kubectl port-forward mac-nginx 8080:80
kubectl delete pod mac-nginx
kubectl get all

curl http://localhost:8080
```
## Deployment and Service
### Deployment
```
kubectl apply -f deploy-nginx.yml
kubectl get deployment --show-labels
kubectl delete deployment mac-nginx-deployment
kubectl scale deployment mac-nginx-deployment --replicas=3
```

### Service
```
kubectl apply -f service-nginx.yml
kubectl delete service mac-nginx-service
curl http://localhost:30001
```