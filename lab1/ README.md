# Kubernetes Ingress Labs

This repository contains practice labs for **Kubernetes Ingress** as part of CKA preparation.

## 🗂 Repository Structure

| File | Description |
|------|-------------|
| `01-deployments-and-services.yaml` | Deploys 3 backend apps and their ClusterIP services. Required before any Ingress. |
| `02-ingress-basic-path.yaml` | Path-based routing Ingress. Routes `/` → `webapp-svc`, `/api` → `api-svc`. |
| `03-ingress-host-based.yaml` | Host-based routing. Routes `myapp.local` → `webapp-svc`, `api.myapp.local` → `api-svc`, `admin.myapp.local` → `admin-svc`. |
| `04-ingress-default-backend.yaml` | Adds a `defaultBackend` (`webapp-svc`) to catch all unmatched paths. |
| `05-ingress-path-types.yaml` | Demonstrates `pathType: Prefix` vs `Exact`. `/api` (Prefix), `/admin` (Exact), `/` → `webapp-svc`. |
| `06-ingress-full-lab.yaml` | Full lab with `/`, `/api`, `/admin` routes in one Ingress. |

---

## ⚡ Prerequisites

- Kubernetes cluster (Minikube recommended)  
- `kubectl` installed  
- Ingress Controller enabled:

```bash
minikube addons enable ingress