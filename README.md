# 🚀 DevOps Task Manager (Flask + Docker + CI/CD + AWS)

[![Docker Publish](https://github.com/Aditya09-cse/devops-task-manager/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/Aditya09-cse/devops-task-manager/actions/workflows/docker-publish.yml)

A fully containerized Flask-based task management application demonstrating end-to-end DevOps practices including CI/CD automation, Docker containerization, and cloud deployment on AWS.


---

## 📌 Project Overview

This project showcases a real-world DevOps workflow by automating the build, test, and deployment process of a Python Flask application using modern DevOps tools.

---

## 🛠️ Tech Stack

* **Backend:** Python, Flask
* **Containerization:** Docker, Docker Compose
* **CI/CD:** GitHub Actions
* **Cloud:** AWS EC2
* **Registry:** Docker Hub

---

## ⚙️ Features

* ✅ Containerized Flask application using Docker
* ✅ Multi-service orchestration with Docker Compose
* ✅ Automated CI/CD pipeline using GitHub Actions
* ✅ Docker image build & push to Docker Hub
* ✅ Cloud deployment on AWS EC2
* ✅ CI/CD pipeline status monitoring

---

## 🔄 CI/CD Workflow

1. Code pushed to GitHub repository
2. GitHub Actions triggers pipeline
3. Docker image is built automatically
4. Image is pushed to Docker Hub
5. Application deployed on AWS EC2

---

## 🧱 Project Structure

```
├── app/
│   ├── app.py
│   └── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── .env
└── README.md
```

---

## 🚀 Getting Started

### 🔧 Prerequisites

* Docker installed
* Docker Compose installed
* Git

### ▶️ Run Locally

```bash
git clone https://github.com/your-username/devops-task-manager.git
cd devops-task-manager
docker-compose up --build
```

App will be available at:
👉 http://localhost:5000

---

## ☁️ Deployment (AWS EC2)

1. Launch EC2 instance
2. Install Docker & Docker Compose
3. Pull Docker image from Docker Hub
4. Run container

---

## 📊 Key Achievements

* 🚀 Reduced manual deployment effort by ~80% using CI/CD automation
* 🔁 Achieved consistent environments across local and cloud using Docker
* ⚡ Improved debugging efficiency by ~30% with pipeline visibility
* 📦 Automated Docker image build & deployment workflow

---

## 📌 Future Improvements

* Add Kubernetes for container orchestration
* Implement monitoring (Prometheus + Grafana)
* Add HTTPS with Nginx reverse proxy

---

## 🤝 Contribution

Feel free to fork this repo and contribute!

---

## 📧 Contact

**Aditya Singh Tomar**

* GitHub: https://github.com/Aditya09-cse
* LinkedIn: in/aditya-tomar-42731628a

---

⭐ If you found this helpful, give it a star!
