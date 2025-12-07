Kubernetes Nginx Ingress + Flask Load Balancing 

This project demonstrates:

- Nginx **Ingress** as a reverse proxy
- Kubernetes **Service** for load balancing across multiple pods
- A simple **Flask** application running in Docker

```
k8s-nginx-flask-ingress/
├─ app/
│  ├─ app.py              # Flask application
│  ├─ requirements.txt    # Python dependencies
│  └─ Dockerfile          # Docker image for the app
├─ k8s/
│  ├─ deployment.yaml     # Deployment with 2 replicas
│  ├─ service.yaml        # ClusterIP service for the app
│  ├─ ingress.yaml        # Nginx Ingress routing to the service
├─ .gitignore
└─ README.md
```
```

🧩 Architecture Overview
Client (browser / curl)
   │
   │   Host: flask.test
   │
[Nginx Ingress Controller]  ← reverse proxy entrypoint
   │
[ClusterIP Service]         ← load balancing
   │
[Flask Pods (2 replicas)]   ← application backend


✅ Prerequisites
Docker
kubectl
A running Kubernetes cluster (e.g. Minikube)
Nginx Ingress Controller



