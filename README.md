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

###kubernetes-controllers

```
kubectl get pods -l app=frontend -w
kubectl scale replicaset frontend --replicas=3

kubectl get rs frontend
kubectl delete pods -l app=frontend | kubectl get pods -l app=frontend -w
kubectl get replicaset frontend -o=jsonpath='{.spec.template.spec.containers[0].image}'
kubectl get deployment paymentservice

kubectl rollout history deployment paymentservice
kubectl rollout undo deployment paymentservice --to-revision=1 | kubectl get rs -l app=paymentservice -w

kubectl rollout status deployment/frontend

```

### kubernamtes-security

```
kubectl create serviceaccount bob
kubectl create clusterrolebinding bob-cluster-admin-binding --clusterrole=cluster-admin --serviceaccount=default:bob -o yaml
kubectl create serviceaccount dave

k create namespace prometheus -o yaml
kubectl create serviceaccount bob
```