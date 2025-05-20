Docker Day 1 – Hello Docker Node App
 
Overview

This is a simple **Hello, World! from Node.js + Docker** API containerized using Docker.
 
---
 
## Steps to Run
 
### 1. Clone the Repo

```bash

git clone https://github.com/username/pi-shaped-workshop-Somya.git

cd pi-shaped-workshop-Somya/docker-k8s-workshop/day1

```
 
## Docker Hub image

[https://hub.docker.com/r/somyanegi/node-hello]
 
 
 
## Core Concept Questions
 
### 1. Why is Docker useful in building and deploying microservices for a real-world product (like an e-commerce or banking app)?

Docker is useful in microservices as it allows each service to run in isolated containers with all dependencies, ensuring consistency across environments. It simplifies deployment, scales easily, and speeds up development. This makes it ideal for real-world apps like e-commerce or banking systems.

---

### 2. What is the difference between a Docker image and a container in the context of scaling a web application?
 
A Docker image is a static blueprint that contains the application code, dependencies, and environment setup. A container is a running instance of that image.
 
When scaling a web application, you create multiple containers from the same image to handle more traffic, ensuring consistency and efficient resource use.

---
 
### 3. How does Kubernetes complement Docker when running a product at scale (e.g., hundreds of containers)?
 
Kubernetes complements Docker by automating the deployment, scaling, and management of containers across multiple machines. While Docker runs individual containers, Kubernetes helps orchestrate hundreds of them, handling load balancing, self-healing, service discovery, and rolling updates, making it ideal for running products at scale reliably.
 
 
