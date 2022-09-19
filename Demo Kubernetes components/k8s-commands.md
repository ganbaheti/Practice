***
kubectl apply commands in order
---
kubectl apply -f mongo-secret.yaml
<br>
kubectl apply -f mongo.yaml
<br>
kubectl apply -f mongo-configmap.yaml 
<br>
kubectl apply -f mongo-express.yaml
<br>

***
kubectl get commands
---

kubectl get pod
<br>
kubectl get pod --watch
<br>
kubectl get pod -o wide
<br>
kubectl get service
<br>
kubectl get secret
<br>
kubectl get all | grep mongodb
<br>

***
kubectl debugging commands
---

kubectl describe pod mongodb-deployment-xxxxxx
<br>
kubectl describe service mongodb-service
<br>
kubectl logs mongo-express-xxxxxx
<br>


***
give a URL to external service in minikube
---
<br>
minikube service mongo-express-service
