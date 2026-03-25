🚀 Site Deployment on AWS using Docker & Docker Compose

This project demonstrates how to deploy a static website on an AWS EC2 server using Docker, Docker Compose, and basic DevOps practices.

📌 Project Overview

This repository contains a simple website deployment setup using:

🐳 Docker for containerization
⚙️ Docker Compose for orchestration
☁️ AWS EC2 as the hosting server
🌐 Nginx (or web server) for serving static content

The goal is to showcase a real-world DevOps workflow for deploying a website efficiently.

🧱 Project Structure
Site_Deployment_AWS/
│── Dockerfile
│── docker-compose.yaml
│── index.html
│── style.css
│── prometheus.yml
⚙️ Technologies Used
Docker
Docker Compose
AWS EC2
Linux (Ubuntu)
Nginx (inside container)
Prometheus (for monitoring - optional)
🚀 Deployment Steps
1️⃣ Launch EC2 Instance
Create an EC2 instance (Ubuntu recommended)
Allow inbound ports:
22 (SSH)
80 (HTTP)
3000/8080 (if needed)
2️⃣ Connect to Server
ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
3️⃣ Install Docker & Docker Compose
sudo apt update
sudo apt install docker.io -y
sudo apt install docker-compose -y

sudo systemctl start docker
sudo systemctl enable docker
4️⃣ Clone Repository
git clone https://github.com/krishnaharki363/Site_Deployment_AWS.git
cd Site_Deployment_AWS
5️⃣ Run Application

⚠️ Important: If docker compose doesn't work, use:

sudo docker-compose up -d
6️⃣ Access Website

Open your browser:

http://<EC2-PUBLIC-IP>
🐳 Docker Details
Dockerfile
Builds a lightweight container
Serves static website files
docker-compose.yaml
Manages container lifecycle
Simplifies deployment with one command
📊 Monitoring (Optional)
prometheus.yml is included for monitoring setup
Can be extended with:
Prometheus
Grafana dashboards
