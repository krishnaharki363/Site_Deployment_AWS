🚀 Site Deployment on AWS (Docker)

This project demonstrates how to deploy a simple static website on an AWS EC2 server using Docker and Docker Compose.

📌 Overview
Deploy a website using Docker containers
Run and manage containers using Docker Compose
Host the application on an AWS EC2 instance
Basic setup for monitoring using Prometheus

📁 Project Structure
Site_Deployment_AWS/
│── Dockerfile
│── docker-compose.yaml
│── index.html
│── style.css
│── prometheus.yml

⚙️ Technologies Used
Docker
Docker Compose
AWS EC2 (Ubuntu)
Nginx (for serving website)
Prometheus (optional monitoring)

🚀 Deployment Steps
1. Launch EC2 Instance
Create Ubuntu EC2 instance
Allow ports: 22 (SSH), 80 (HTTP)

3. Connect to Server
ssh -i "your-key.pem" ubuntu@your-ec2-public-ip

5. Install Docker & Docker Compose
sudo apt update
sudo apt install docker.io -y
sudo apt install docker-compose -y
sudo systemctl start docker
sudo systemctl enable docker

4. Clone Repository
git clone https://github.com/krishnaharki363/Site_Deployment_AWS.git
cd Site_Deployment_AWS

6. Run the Application
sudo docker-compose up -d

8. Access Website
Open in browser: http://<EC2-PUBLIC-IP>

http://<EC2-PUBLIC-IP>
