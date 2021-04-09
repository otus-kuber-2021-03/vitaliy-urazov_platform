# vitaliy-urazov_platform
vitaliy-urazov Platform repository

###kubernetes-intro
```
docker build -t kubernetes-intro .
docker push vurazov/kubernetes-intro
```

```
kubectl apply -f web-pod.yaml
kubectl get pods
kubectl get pod web -o yaml
kubectl describe pod web
kubectl get pods -w
kubectl port-forward --address 0.0.0.0 pod/web 8000:8000

```
