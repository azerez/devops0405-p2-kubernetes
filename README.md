# DevOps Course Project - Phase 2: Kubernetes Orchestration

This project is part of the DevOps course final assignment.  
It demonstrates Kubernetes orchestration capabilities by deploying a simple Flask-based application using various K8s components.

## 📁 Project Structure

All Kubernetes manifests are located in the `k8s/` directory and include:

- `deployment.yaml` – Deploys the Flask application.
- `pod.yaml` – Defines a standalone pod.
- `service.yaml` – Exposes the application internally or externally.
- `configmap.yaml` – Stores configuration values.
- `secret.yaml` – Stores sensitive data.
- `pod-with-configmap.yaml` – Pod consuming ConfigMap.
- `pod-with-secret.yaml` – Pod consuming Secret.
- `cronjob.yaml` – A scheduled job example.
- `hpa.yaml` – Horizontal Pod Autoscaler configuration.
- `deployment-with-liveness-readiness.yaml` – Adds probes for better reliability.

## 🚀 How to Use

1. **Make sure you're connected to a Kubernetes cluster**  
   (e.g., Minikube, Docker Desktop, or a cloud provider like EKS/GKE/AKS).

2. **Apply ConfigMap and Secret (optional):**
   ```bash
   kubectl apply -f k8s/configmap.yaml
   kubectl apply -f k8s/secret.yaml
   ```

3. **Deploy the application:**
   ```bash
   kubectl apply -f k8s/deployment.yaml
   kubectl apply -f k8s/service.yaml
   ```

4. **(Optional) Apply additional components:**
   ```bash
   kubectl apply -f k8s/hpa.yaml
   kubectl apply -f k8s/cronjob.yaml
   kubectl apply -f k8s/deployment-with-liveness-readiness.yaml
   ```

5. **Check status:**
   ```bash
   kubectl get all
   ```

## 🧪 Features Demonstrated

- ConfigMap and Secret injection
- Liveness & Readiness probes
- Horizontal Pod Autoscaler (HPA)
- CronJob scheduling
- Secure pod definitions using secrets
- Reusability and modular manifests

## 📝 Prerequisites

- Kubernetes cluster (v1.20+ recommended)
- `kubectl` CLI configured
- Docker (for building images if needed)

## 📦 Project Goals

- Demonstrate real-world use of Kubernetes manifests
- Emphasize modularity and clean structure
- Practice readiness/liveness monitoring
- Implement auto-scaling and scheduled tasks

---

## 📌 Notes

- This is part of a two-phase project. Phase 1 included Docker and local deployment.
- Please refer to `phase1/` directory for those files (to be added).

## 📤 Author

Erez Azoulay  
DevOps Course – 0405  
GitHub: [@azerez](https://github.com/azerez)
