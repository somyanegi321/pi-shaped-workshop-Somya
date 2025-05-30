# 2-Tier App Deployment with Performance Optimization
 
## Objective
Deploy a frontend-backend application using Kubernetes with performance tuning and cost optimization features.
 
## Features
- Helm chart structure
- Resource requests/limits
- Liveness and readiness probes
- Horizontal Pod Autoscaler (HPA)
 
## Performance & Cost Optimizations
- Resource limits prevent optimize cluster usage.
- HPA handles traffic.
 
## Core Concept Questions
 
### 1. Why are liveness and readiness probes critical in keeping a product’s user experience stable and reliable?
 
Liveness and readiness probes ensure app stability by automatically restarting unresponsive containers and routing traffic only to ready ones. This prevents downtime and avoids sending users to broken or initializing services, keeping the experience smooth and reliable.
 
 
### How does HPA help in handling flash sales, seasonal load spikes, or traffic surges in real-world applications like an e-commerce platform?
 
HPA (Horizontal Pod Autoscaler) automatically scales the number of pods based on CPU/memory usage or custom metrics. During flash sales or traffic spikes, it increases pods to handle the load, ensuring the app stays responsive and avoids crashes.
