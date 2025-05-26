# Day 3 Assignment
 
This Assignment demonstrates how to expose app in a Minikube  using **Ingress**, with service types like **ClusterIP** and  **NodePort**.


##  Minikube ingress addon enabled:
 
```bash

minikube addons enable ingress

```

---
 
## Step 1: Clone the Repo and apply yamls
 
```bash

git clone https://github.com/somyanegi321/pi-shaped-workshop-Somya.git

cd pi-shaped-workshop-Somya/docker-k8s-workshop/day3
kubectl apply -f deployment.yaml

kubectl apply -f service.yaml
kubectl apply -f ingress.yaml

```
 
## Step 2: Update /etc/hosts for Domain Resolution
 
```bash

sudo nano /etc/hosts

192.168.49.2 node.local //Add this line at the end:

```
 
## Step 3: Access the App on Browser

http://node.local/hello
 
## Core Concept Questions
 
### 1. How would you expose an internal microservice (e.g., user-auth) differently than a public-facing frontend in a Kubernetes-based product?

Internal microservices like user-auth are exposed using ClusterIP, making them accessible only within the cluster for better security. Public-facing services like frontend apps are exposed using Ingress or LoadBalancer to allow external access over the internet. This separation ensures secure and optimized traffic routing.
 
---
 
### 2. Why might a product use Ingress instead of directly exposing each microservice via LoadBalancer?
 
Using Ingress instead of exposing each microservice with a LoadBalancer is more efficient because:
It reduces cost by using one LoadBalancer to manage access to multiple services.
It simplifies routing with path-based or host-based rules.
It centralizes SSL/TLS termination and request management.
This makes the system more scalable and easier to maintain.
 
 
