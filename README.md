# 🚀 DevOps CI/CD Pipeline using Jenkins, Docker & AWS

## 📌 Project Overview

This project implements an automated CI/CD pipeline where a Node.js application is built into a Docker image using Jenkins and deployed on an AWS EC2 instance. The pipeline reduces manual deployment effort and ensures faster and consistent delivery.

## 🛠️ Tech Stack

* Jenkins (CI/CD Automation)
* Docker (Containerization)
* AWS EC2 (Cloud Hosting)
* GitHub (Source Code Management)
* Node.js (Application Runtime)
* Linux (Server Environment)

## ⚙️ Architecture

GitHub → Jenkins → Docker → AWS EC2

## 🔄 Pipeline Flow

1. Code pushed to GitHub repository
2. Jenkins pulls source code
3. Docker image is built
4. Container is deployed on AWS EC2
5. Application runs and is accessible via public IP

## ▶️ How to Run

```bash
git clone https://github.com/YOUR_USERNAME/devops-cicd-pipeline.git
cd devops-cicd-pipeline
docker build -t devops-app .
docker run -d -p 80:3000 devops-app
```

## 📸 Screenshots

(Added images inside /screenshots folder)

* Jenkins pipeline success
* Docker container running
* Application output in browser

## 📄 Detailed Documentation

For complete implementation steps, commands, and outputs:

👉 [View Full Project Report](./DevOps-CICD-Pipeline-Documentation.pdf)

## 💡 Future Improvements

* Add Jenkinsfile for pipeline as code
* Integrate GitHub Webhooks
* Use Docker Compose for scalability

## 📚 Key Learnings

* CI/CD pipeline automation
* Docker-based deployment
* AWS cloud infrastructure handling
