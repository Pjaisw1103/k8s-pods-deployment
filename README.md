# 📦 Kubernetes Pod Manifests

[![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)](#)

Declarative Kubernetes **Pod** specifications for deploying standalone web server and application workloads (`Nginx` & `Firefox`).

---

## 📌 Workloads Included

| Pod Name | Image | Port | Description |
| :--- | :--- | :--- | :--- |
| `nginx-pod` | `nginx:latest` | `80` | Light-weight high-performance HTTP web server |
| `firefox-pod` | `lscr.io/linuxserver/firefox:latest` | `3001` | Containerized web browser application |

---

## 📂 Repository Structure

```text
k8s-pods-deployment/
├── pod.yaml       # Declarative manifest for standalone Pod workloads
└── README.md      # Repository Documentation
```

---

## 🚀 Usage Guide

### Prerequisites
- Active Kubernetes cluster (e.g. AKS, Minikube, Kind)
- `kubectl` CLI installed and configured

### Apply Pod Manifests

```bash
# Deploy Pods to your default namespace
kubectl apply -f pod.yaml

# Verify execution status
kubectl get pods -o wide
```

### Inspect Pod Logs & Details

```bash
# Check detailed status of Nginx pod
kubectl describe pod nginx-pod

# Stream logs from Nginx container
kubectl logs -f nginx-pod
```

### Cleanup

```bash
kubectl delete -f pod.yaml
```

---

## 👩‍💻 Author

**Priya Jaiswal**  
[GitHub Profile](https://github.com/Pjaisw1103)
