# Deploy and manage a full-stack application on Kubernetes

<img width="1918" height="1066" alt="Screenshot 2025-09-13 114241" src="https://github.com/user-attachments/assets/244d9a56-b544-4abe-ab87-a0e3898cacbe" />


This newsletter project demonstrates the deployment and management of a full-stack web application on a Kubernetes cluster, featuring:
- Node.js backend
- MongoDB database
- Nginx frontend
- Docker containerization
- Kubernetes orchestration
- ConfigMaps for environment management
- Persistent Volumes for data storage

Follow along for hands-on experience with deploying, managing, and scaling a complete application on Kubernetes.

## Pre-requisites

**Docker**: Installed and running on the system.

**Minikube** (k8s): Installed and configured on the system.

**Node.js v20.15**: Installed on the system (for the backend &amp; frontend).

**MongoDB**: Installed on the system (for the database).

## To quickly deploy the application, run:

```sh
bash deploy
```

Then, navigate to `http://localhost:8000` from your host browser.

> Make sure to have `/mnt/data` on your local machine. The db seeks that particular location to store and persist clients' data.

## ☸️ Deploy on Kubernetes
- Step1. git clone https://github.com/PrajwalBambulkar/Newsletter-.git
- cd Newsletter/deployment.
- kubectl apply -f .
- kubectl port-forward -n fullstack-app svc/frontend-service 8080:80 --address 0.0.0.0
- access ec2ip:8080
