# Kubernetes (K8s)

Kubernetes is a container orchestration tool and much more than that. Kubernetes can run on cloud, servers, PCs and other related places. It can also replicate containers, Pods from one to another etc.

# What is Container Orchestration ?

This is a tool that deploy and manages exixsting containers. In today's business people wants to 

- Deploy containers
- Zero downtime updates of containers
- Self healing of containers
- Scale the containers
- Load balancing

Container orchestration tools helps developer to do that. Kubernetes is one of this tools.

# Architecture of Kubernetes

![Architecture of Kubernetes](./assets/images/kubernetes-constructs-concepts-architecture.jpg)
There should be **Kube-Proxy** inside the Nodes in Worker Nodes who communicates with the API server inside the Control Place.

**Kubernetes Cluster = Control Plane ( *previously known as Master Node* ) + Nodes**

**Kubectl** is a Command Line Tool like Docker command that helps you to communicate with Kubernetes Cluster

**Kubernetes Cluster** is made of by the combination of **Control Plane** and **Worker Nodes**

**Control Plane** is the program that controls the worker nodes. So you give commands using the Kubectl using terminal then Kubectl tells the Control Plane to do the task.

**Worker Nodes** are the nodes where the microservices, Pods, Containers are lies. Worker nodes are the one who actually storing the doing tasks on Control Plane's command.

**Pod** is a scheduling unit in Kubernetes it contains Container. So in Kubernetes all containers should be inside a Pod. One container one Pod is best practice but we can have more than one container inside a Pod.

**Control Manager** it is a tool that helps to manage the entire cluster. It has four functionalities 

- Desired State
- Current State
- Differences
- Make the changes

We can interact with the Kubectl using two ways in our terminal 

- Declarative Way : In this way we give all details in a manifest file or YAML file. 
- Imperative Way : In this way we give individual commands for each tasks.

# Basic Commands

`kubectl version`
`kubectl version --output=yaml`
`minikube version`
`minikube start`
`minikube status`
`kubectl get pods`
`kubectl get nodes`
`minikube dashboard`
`minikube docker-env`
`minikube ssh`
`kubectl config view`
`kubectl get all`
`kubectl delete pod pode-name`
`kubectl get deployments`
`kubectl delete deployments deployment-name`
