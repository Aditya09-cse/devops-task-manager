# 🚀 DevOps Task Manager (Flask + Docker + Kubernetes + CI/CD + AWS)

[![Docker Publish](https://github.com/Aditya09-cse/devops-task-manager/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/Aditya09-cse/devops-task-manager/actions/workflows/docker-publish.yml)

A production-style multi-tier Flask Task Manager application demonstrating modern DevOps practices, including Docker containerization, Kubernetes orchestration, GitHub Actions CI/CD, and cloud deployment on AWS.

---

# 📌 Project Overview

This project demonstrates an end-to-end DevOps workflow by building, containerizing, deploying, and orchestrating a Flask application with PostgreSQL.

The application is designed to run consistently across local and cloud environments using Docker and Kubernetes while leveraging GitHub Actions for automated container builds and Docker Hub image publishing.

---

# 🛠️ Tech Stack

### Backend
- Python
- Flask
- SQLAlchemy
- PostgreSQL

### DevOps
- Docker
- Docker Compose
- Kubernetes
- GitHub Actions

### Cloud
- AWS EC2

### Container Registry
- Docker Hub

---

# ✨ Features

- ✅ Flask Task Management Application
- ✅ PostgreSQL Database Integration
- ✅ Dockerized Application
- ✅ Multi-container Development using Docker Compose
- ✅ Kubernetes Multi-Tier Deployment
- ✅ ConfigMap & Secret Management
- ✅ Internal Service Communication
- ✅ GitHub Actions CI/CD Pipeline
- ✅ Docker Image Publishing to Docker Hub
- ✅ AWS EC2 Deployment

---

# 🔄 CI/CD Workflow

```
Developer
     │
     ▼
GitHub Repository
     │
     ▼
GitHub Actions
     │
     ├── Install Dependencies
     ├── Build Docker Image
     ├── Push Image to Docker Hub
     ▼
Docker Hub
     │
     ▼
AWS EC2 / Kubernetes Cluster
```

---

# ☸️ Kubernetes Architecture

```
                  User
                    │
                    ▼
            Flask Service
                    │
                    ▼
         Flask Deployment (Pods)
                    │
                    ▼
         PostgreSQL Service
                    │
                    ▼
      PostgreSQL Deployment
```

### Kubernetes Resources

| Resource | Purpose |
|----------|---------|
| Namespace | Resource Isolation |
| Deployment | Flask Application |
| Deployment | PostgreSQL Database |
| Service | Flask Internal Access |
| Service | PostgreSQL Internal Communication |
| ConfigMap | Store Configuration |
| Secret | Store Sensitive Credentials |

---

# 📂 Project Structure

```
devops-task-manager/
│
├── .github/
│   └── workflows/
│       └── docker-publish.yml
│
├── app/
│   ├── static/
│   ├── templates/
│   ├── app.py
│   ├── models.py
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── requirements.txt
│   └── .gitignore
│
├── k8s/
│   ├── namespace.yml
│   ├── configmap.yml
│   ├── secret.yml
│   ├── flask-deployment.yml
│   ├── flask-service.yml
│   ├── postgres-deployment.yml
│   └── postgres-service.yml
│
└── README.md
```

---

# 🚀 Running with Docker

### Clone Repository

```bash
git clone https://github.com/Aditya09-cse/devops-task-manager.git

cd devops-task-manager/app
```

### Build & Start

```bash
docker compose up --build
```

Application:

```
http://localhost:5000
```

---

# ☸️ Deploy on Kubernetes

Apply the manifests:

```bash
kubectl apply -f k8s/namespace.yml

kubectl apply -f k8s/configmap.yml

kubectl apply -f k8s/secret.yml

kubectl apply -f k8s/postgres-deployment.yml

kubectl apply -f k8s/postgres-service.yml

kubectl apply -f k8s/flask-deployment.yml

kubectl apply -f k8s/flask-service.yml
```

Verify deployment:

```bash
kubectl get pods -n aditya-namespace

kubectl get svc -n aditya-namespace

kubectl get deployments -n aditya-namespace
```

Access the application:

```bash
kubectl port-forward svc/flask-service -n aditya-namespace 8081:80
```

Open:

```
http://localhost:8081
```

---

# ☁️ AWS Deployment

1. Launch an EC2 instance
2. Install Docker
3. Clone the repository
4. Run using Docker Compose **or**
5. Deploy using Kubernetes manifests

---

# 📊 Project Highlights

- 🚀 Automated Docker image builds using GitHub Actions
- 📦 Published Docker images to Docker Hub
- ☸️ Deployed a multi-tier application on Kubernetes
- 🔐 Managed application configuration using ConfigMaps and Secrets
- 🐳 Containerized the application for consistent deployments
- ☁️ Successfully deployed on AWS EC2
- 🔄 Demonstrated Pod-to-Pod communication through Kubernetes Services

---

# 🛠️ Troubleshooting Experience

During development, the following Kubernetes issues were diagnosed and resolved:

- Fixed Service selector mismatches
- Resolved PostgreSQL Service endpoint issues
- Debugged Flask-to-PostgreSQL connectivity
- Resolved missing database table (`relation "task" does not exist`)
- Used `kubectl logs`, `kubectl exec`, `kubectl describe`, `kubectl get endpoints`, and `psql` for troubleshooting

---

# 🚀 Future Improvements

- Helm Charts
- Horizontal Pod Autoscaler (HPA)
- Persistent Volumes for PostgreSQL
- Ingress Controller
- Prometheus & Grafana Monitoring
- ArgoCD GitOps Deployment
- Terraform Infrastructure Provisioning

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

Feel free to fork the repository and open a pull request.

---

# 👨‍💻 Author

**Aditya Singh Tomar**

- GitHub: https://github.com/Aditya09-cse
- LinkedIn: https://www.linkedin.com/in/aditya-tomar-42731628a/

---

⭐ If you found this project helpful, consider giving it a **Star**!
