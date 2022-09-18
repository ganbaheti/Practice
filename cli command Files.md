***
install hyperhit and minikube
---
 -> brew update
<br>
 -> brew install hyperkit
<br>
 -> brew install minikube
<br>
 -> kubectl
<br>
 -> minikube
<br>

***

create minikube cluster
---
minikube start --vm-driver=hyperkit
<br>
kubectl get nodes
<br>
minikube status
<br>
kubectl version
<br>

***

delete cluster and restart in debug mode
---
minikube delete
<br>
minikube start --vm-driver=hyperkit --v=7 --alsologtostderr
<br>
minikube status
<br>

***
kubectl commands
---
kubectl get nodes
<br>
kubectl get pod
<br>
kubectl get services
<br>
kubectl create deployment nginx-depl --image=nginx
<br>
kubectl get deployment
<br>
kubectl get replicaset
<br>
kubectl edit deployment nginx-depl
<br>

***
debugging
---
kubectl logs {pod-name}
<br>
kubectl exec -it {pod-name} -- bin/bash
<br>

***
create mongo deployment
---
kubectl create deployment mongo-depl --image=mongo
<br>
kubectl logs mongo-depl-{pod-name}
<br>
kubectl describe pod mongo-depl-{pod-name}
<br>

***
delete deplyoment
---
kubectl delete deployment mongo-depl
<br>
kubectl delete deployment nginx-depl
<br>


***
create or edit config file
---
vim nginx-deployment.yaml
<br>
kubectl apply -f nginx-deployment.yaml
<br>
kubectl get pod
<br>
kubectl get deployment
<br>

***
delete with config
---
kubectl delete -f nginx-deployment.yaml
<br>


#Metrics
kubectl top The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, or for a particular pod or node if specified.
