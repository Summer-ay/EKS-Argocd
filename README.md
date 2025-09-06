# GitOps Argo CD Demo

This repository contains a sample Kubernetes application managed with Argo CD.

## Structure
- `manifests/` → Kubernetes YAML manifests for a simple nginx app.

## Application
- **Deployment**: Runs 2 replicas of nginx.
- **Service**: Exposes nginx on port 80 (NodePort for Minikube).

## Usage with Argo CD
1. Connect this repo in Argo CD UI (Settings → Repositories).
2. Create an Application:
   - Repository URL: (this repo’s URL)
   - Path: `manifests`
   - Destination: Your cluster (`https://kubernetes.default.svc`)
   - Namespace: `default`
3. Sync the Application → nginx will deploy automatically.

