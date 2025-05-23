# Self-Healing Infrastructure with Prometheus, Alertmanager, and Nginx

This project demonstrates a basic self-healing infrastructure setup using Prometheus for monitoring, Alertmanager for alerting, and Nginx as a sample service. The system is containerized using Docker Compose.

---

## 📁 Folder Structure

self-healing-infra/ ├── docker-compose.yml ├── prometheus.yml ├── alertmanager/ │ └── alertmanager.yml ├── rules/ │ └── alert.rules.yml ├── nginx.conf └── README.md

## 🚀 How to Run

### 1. Clone the Repository

git clone git@github.com:Nilava786/Prometheus-demo.git
cd self-healing-infra

2. Start the Stack

docker-compose up -d --build
This will start:

Prometheus (port: 9090)

Alertmanager (port: 9093)

Nginx (port: 8080)

📡 Services

Service	URL
Prometheus	http://localhost:9090
Alertmanager	http://localhost:9093
Nginx Proxy	http://localhost:8080
⚙️ Prometheus Configuration

Located in prometheus.yml. It scrapes metrics from:

nginx_service (example service)

alertmanager

🚨 Alert Rules
Defined in rules/alert.rules.yml. Currently includes:

HighCpuUsage: Fires if CPU usage exceeds 90% for 5 minutes.

📬 Alertmanager Configuration
Found in alertmanager/alertmanager.yml. You can configure email, Slack, or other receivers here. Example uses email (replace with your own address).

🧹 Cleanup
To stop and clean everything:

docker-compose down --volumes --remove-orphans

📌 Notes
Ensure Docker and Docker Compose are installed.

Make sure ports 8080, 9090, and 9093 are available on your machine.

Update email configs in Alertmanager to actually receive alerts.

#   P r o m e t h e u s - d e m o  
 