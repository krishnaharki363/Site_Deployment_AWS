# 🚀 Site Deployment on AWS using Docker, Nginx, Prometheus & Grafana

This project demonstrates a complete **DevOps-based deployment** of a static website on an AWS EC2 server using Docker, Nginx reverse proxy, custom domain configuration, and monitoring with Prometheus and Grafana.

---

## 🌐 Live Demo

🔗 https://python.krishnaharki.com.np

---

## 🧰 Tech Stack

- AWS EC2 (Ubuntu)
- Docker & Docker Compose
- Nginx (Reverse Proxy)
- Prometheus (Monitoring)
- Grafana (Visualization)
- Cloudflare (DNS Management)
- Certbot (SSL - Let's Encrypt)

---

## 📁 Project Structure


.
├── Dockerfile
├── docker-compose.yaml
├── index.html
├── style.css
├── prometheus.yml


---

## ⚙️ Features

- 🚀 Containerized web application using Docker
- 🔁 Multi-service orchestration using Docker Compose
- 🌍 Custom domain setup via Cloudflare DNS
- 🔀 Nginx reverse proxy configuration
- 🔒 HTTPS enabled using Let's Encrypt (Certbot)
- 📊 Monitoring with Prometheus
- 📈 Visualization dashboards using Grafana

---

## 🐳 Running the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
2. Start services
docker-compose up -d
3. Check running containers
docker ps

🌍 Access Services
Service	URL
Website	http://localhost:8080

Prometheus	http://localhost:9090

Grafana	http://localhost:3000
🔐 Default Grafana Login
Username: admin
Password: admin

☁️ Deployment Steps (High Level)
Launch EC2 instance (Ubuntu)
Install Docker & Docker Compose
Clone project repository
Run containers using Docker Compose
Install and configure Nginx
Set up domain via Cloudflare DNS
Configure reverse proxy (Nginx → Docker app)
Enable HTTPS using Certbot
Verify monitoring tools (Prometheus & Grafana)

📊 Monitoring Setup
Prometheus collects metrics from services
Grafana visualizes metrics using dashboards
Ports exposed:
9090 → Prometheus
3000 → Grafana

⚠️ Troubleshooting
Docker Permission Issue
sudo usermod -aG docker $USER
newgrp docker
Port Access Issue (AWS)

Make sure the following ports are open in the Security Group:

80 (HTTP)
443 (HTTPS)
3000 (Grafana)
9090 (Prometheus)
Nginx Config Test
sudo nginx -t
sudo systemctl reload nginx

🙌 Acknowledgment

This project was built as part of a hands-on learning journey in DevOps and Cloud Deployment, focusing on real-world implementation.

📌 Author

Krish Naharki
Aspiring DevOps & Cloud Engineer
