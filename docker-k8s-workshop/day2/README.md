# Docker Day 2 Exercise
 
## Overview
Now deployed on Kubernetes using pod scheduling with node affinity , Limited resources and tolerations using Day1 Assignment image. 
 
## How to Run
 
```bash
git clone https://github.com/somyanegi321/pi-shaped-workshop-Somya
cd pi-shaped-workshop-Somya/docker-k8s-workshop/day2
kubectl label nodes <node-name> disktype=ssd
kubectl taint nodes <node-name>  env=dev:NoSchedule
kubectl get nodes --show-labels
kubectl apply -f deployment.yaml
kubectl get pods -o wide
kubectl port-forward pod/<pod name> 8080:8080  #Access the Flask App
```
 
 
## Core Concept Questions
 
### 1. Why do we set requests and limits for CPU/memory in a production-grade product?
 
We set CPU and memory requests and limits in a production-grade product to:
1. Ensure reliability – guarantees each container gets the minimum resources it needs to function properly.
2. Prevent resource hogging – limits stop any one container from using up all CPU/memory and affecting others.
3. Enable better scheduling – Kubernetes uses requests to schedule pods on nodes with enough capacity.
4. Avoid crashes – setting proper limits prevents out-of-memory errors and CPU starvation.
This helps maintain stability, performance, and fairness across services in production.
 
---
 
### 2. When would a product team apply node affinity in Kubernetes?
 
A product team would apply node affinity in Kubernetes when they want to control which nodes a pod runs on based on custom rules. This is useful in scenarios like:
1. Hardware specialization – run pods on nodes with GPUs or SSDs.
2. Environment isolation – separate dev, staging, and prod workloads on different nodes.
3. Compliance/security – ensure sensitive workloads only run on trusted or compliant nodes.
4. Cost optimization – assign less critical workloads to cheaper nodes.
Node affinity helps improve performance, security, and resource management by aligning workloads with appropriate node types.
