
# 💡 Introduction to Minikube
- minikube is easy and quickly sets up a local Kubernetes cluster on macOS, Linux, and Windows.

![Screenshot](/minikube/images/screenshot.png)

All you need is Docker (or similarly compatible) container or a Virtual Machine environment, and Kubernetes is a single command away: 

``
minikube start
``

## What you’ll need - Installation Requirements

* 2 CPUs or more
* 2GB of free memory
* 20GB of free disk space
* Internet connection
* Container or virtual machine manager

<h2 class="step"><span class="fa-stack fa-1x"><i class="fa fa-circle fa-stack-2x"></i><strong class="fa-stack-1x text-primary">1</strong></span>Installation Steps</h2>


## Minikube Basic Commands

```shell
minikube start

minukube status
minikube
kubeclt
kubeclt version
kubectl get nodes
```
![Screenshot](/minikube/images/kubversion.png)

```shell
kubectl get nodes

minukube status

```

## 💡  Examples CURD Operation

Lets create simple deployment and using nginx:alpine images
Example : 1

```shell
1. kubectl create deployment nginx-alpine --image=nginx:alpine
deployment.apps/nginx-alpine created

2. kubectl get deployments,pods,replicaset | grep nginx
```

![Screenshot](/minikube/images/podsview.png)

Now Edit the deployment and make some changes in replicaset to 2

```shell
1. kubectl edit deployment nginx-alpine

2. kubectl get deployment,pods,replicaset | grep nginx-alpine
```

![Screenshot](/minikube/images/edit.png)

![Screenshot](/minikube/images/viewall.png)

Now how to check the logs and describe command

```shell
1. kubectl logs nginx-alpine
2. kubectl descirbe pod nginx-alpine
```

Now lets delete the deployment

```shell
1. kubectl delete deployment nginx-alpine

2. kubectl get deployment,pods,replicaset | grep nginx-alpine
```

![Screenshot](/minikube/images/del.png)

