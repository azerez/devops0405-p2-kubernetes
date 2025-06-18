# README - Kubernetes Project for Flask Application

This project demonstrates a complete Kubernetes-based deployment lifecycle for a Dockerized Flask web application, including advanced configurations such as autoscaling, secret management, scheduled tasks, and health monitoring.

## 🚀 Project Overview

The project walks through deploying and managing a simple Flask app (`erezazu/devops0405-docker-flask-app:v1`) in a Kubernetes environment using Minikube.

---

## 👩‍💼 Tasks Summary

### 1. **Cluster Initialization**

Set up a local Kubernetes cluster using **Minikube** to simulate a production-like environment.

### 2. **Dockerized App Deployment as Pod**

Deployed the `flask-app` container as a standalone Pod.

- **File**: `flask-app-pod.yaml`

### 3. **Deployment and ReplicaSet**

Wrapped the Pod in a Deployment with multiple replicas to ensure availability.

- **File**: `flask-app-deployment.yaml`

### 4. **Expose Application via Service**

Created a NodePort Service to expose the Flask application externally.

- **File**: `flask-service.yaml`

### 5. **Horizontal Pod Autoscaler (HPA)**

Configured HPA to automatically scale Pods based on CPU usage using a stress pod to simulate load.

- **Files**:
  - `flask-hpa.yaml`
  - `cpu-stress-pod.yaml`

### 6. **ConfigMap and Secrets**

Created ConfigMap and Secret resources to externalize application configuration and sensitive data.

- **Files**:
  - `flask-configmap.yaml`
  - `flask-pod-with-configmap.yaml`
  - `flask-secret.yaml`
  - `flask-pod-with-secret.yaml`

### 7. **CronJobs for Periodic Tasks**

Implemented CronJob to periodically send HTTP requests to the application endpoint.

- **File**: `flask-cronjob.yaml`

### 8. **Health Probes**

Integrated **Readiness** and **Liveness** Probes to monitor the application lifecycle and behavior.

- **File**: `flask-app-deployment-with-liveness-readiness.yaml`
- Endpoint used: `/` (returns `Hello, World!` from the Flask app)

---

## 📁 Files Created

```
cpu-stress-pod.yaml
flask-app-deployment.yaml
flask-app-deployment-with-liveness-readiness.yaml
flask-app-pod.yaml
flask-configmap.yaml
flask-cronjob.yaml
flask-hpa.yaml
flask-pod-with-configmap.yaml
flask-pod-with-secret.yaml
flask-secret.yaml
flask-service.yaml
```



