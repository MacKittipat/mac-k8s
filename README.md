# mac-k8s-sample 

## Pod 
```
kubectl apply -f pod-nginx.yml
kubectl port-forward mac-nginx 8080:80
kubectl delete pod mac-nginx
kubectl get all
```

## Deployment
```
kubectl apply -f deploy-nginx.yml
kubectl get deployment --show-labels
kubectl delete deployment mac-nginx-deployment
kubectl scale deployment mac-nginx-deployment --replicas=3
```

## Service
```
kubectl apply -f service-nginx.yml
kubectl delete service mac-nginx-service
http://localhost:30001
```