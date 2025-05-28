# Day 4 assignment
 
## Overview

This is a Helm chart for deploying the Node Hello app.
 
---
 
## How to Use
 
### 1. Clone the repository
 
```bash

git clone https://github.com/Somyanegi321/pi-shaped-workshop-Somay.git

cd pi-shaped-workshop-Somya/docker-k8s-workshop/day4

```
 
## 2: Install the Helm chart
 
```bash

helm install node-hello ./node-hello

```
 
## 3: Update /etc/hosts for Domain Resolution
 
```bash

sudo nano /etc/hosts

192.168.49.2 node.local //Add this line at the end:

```
 
## 4: Access the App
 
Now open your browser and go to:
http://node.local/hello
 
 
## Core Concept Questions
 
### 1. Why is Helm important for managing configuration across different environments in a real-world product (e.g., dev, staging, prod)?
 
Helm is important because it lets you reuse the same Kubernetes templates across environments by simply changing configuration values. This ensures consistent deployments in dev, staging, and prod, and makes updates, rollbacks, and automation easy through CI/CD pipelines.
 
---
 
### 2. How does Helm simplify deployment rollback during a production incident?
 
Helm simplifies deployment rollback by tracking the history of each release. If a production incident occurs, you can quickly revert to a previous stable version using a single command:
```bash
helm rollback <release-name> <revision-number>

```
This makes recovery fast and minimizes downtime.

 
