# 🚀 CI/CD Pipeline Automation with Jenkins, Docker, and Python Flask

This project demonstrates a fully automated **CI/CD pipeline** using **Jenkins**, **Docker**, and **GitHub**, deployed on an **AWS EC2 (Free Tier)** instance. The pipeline automates the build, test, and deployment of a containerized **Python Flask application**.

---

## 📌 Features

- ✅ CI/CD pipeline using Jenkins
- ✅ Containerized Flask app with Docker
- ✅ GitHub integration for automated builds
- ✅ Auto build, test, and deploy to staging (localhost)
- ✅ Hosted on AWS Free Tier (t2.micro EC2)

---

## 🧱 Tech Stack

- **Python 3.9**
- **Flask Web Framework**
- **Docker**
- **Jenkins**
- **Git & GitHub**
- **AWS EC2 (Amazon Linux / Ubuntu)**

---

## 📁 Project Structure

├── app.py

├── Dockerfile

├── Jenkinsfile

├── requirements.txt

└── README.md

---

## 🔧 Setup Instructions

### 1️⃣ Launch EC2 Instance

- OS: Amazon Linux 2 or Ubuntu 22.04
- Instance type: `t2.micro`
- Open ports: `22`, `8080`, `5000`

---

### 2️⃣ Install Required Tools

Install **Java**, **Jenkins**, **Docker**, and start the Jenkins service.

```bash
# Amazon Linux 2
sudo yum update -y
sudo yum install java-11-amazon-corretto docker git -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ec2-user

# Jenkins install
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io-2023.key
sudo yum install jenkins -y
sudo systemctl start jenkins
sudo systemctl enable jenkins
```
### 🔁 CI/CD Flow

Developer pushes code to GitHub.

Jenkins job triggers (via webhook or manual build).

Jenkins:

Pulls the code from GitHub.

Builds a Docker image.

Runs the Flask app in a container.

App is available on: http://<ec2-public-ip>:5000

### 📷 Screenshots

(Add screenshots of Jenkins pipeline, Docker running containers, or web output here)

### 💡 Future Enhancements

Add testing stage (e.g., Pytest)

Deploy to production using Nginx + Gunicorn

Use Docker Compose for multi-container apps

Setup monitoring with Prometheus + Grafana


### 🧑‍💻 Author

Bablu Alam

Cloud & DevOps Engineer

LinkedIn | Bangalore, India


