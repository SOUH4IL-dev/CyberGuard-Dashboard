# 🛡️ CyberGuard Dashboard

> A full-stack Cyber Security Operations Dashboard for monitoring assets, detecting threats, running scans, and generating real-time security intelligence.

## 🚀 Overview
CyberGuard Dashboard is a SOC-inspired cybersecurity platform built to simulate real-world security operations. It allows monitoring of infrastructure, asset management, vulnerability scanning, threat detection, and automated reporting in real time.

## ✨ Features
🔐 Authentication & Security: JWT auth, role-based access control, secure APIs, rate limiting, audit logging.  
📊 Real-Time Dashboard: Live threat monitoring, analytics, system health metrics, interactive charts.  
🖥️ Asset Management: Track internal/external assets, categorize them, and map vulnerabilities.  
🔎 Security Scanning: Nmap integration, subdomain enumeration, background scan tasks.  
⚠️ Findings & Alerts: Threat classification, severity scoring, real-time WebSocket alerts.  
📄 Reports: Automated security reports with PDF/JSON export and historical tracking.

## 🏗️ Tech Stack
Backend: FastAPI, SQLAlchemy, PostgreSQL/MySQL, JWT, WebSockets, async tasks.  
Frontend: React.js, Tailwind CSS, React Query, Axios, Recharts/Chart.js.  
DevOps: Docker, Docker Compose, Nginx.

## 📁 Structure
backend → FastAPI API, services, models, scanners  
frontend → React UI dashboard  
scripts → security tools (scanner, enum, seeding)  
docker → deployment setup  

## ⚙️ Setup
git clone https://github.com/SOUH4IL-dev/cyber-security-dashboard.git  
cd cyber-security-dashboard  

Backend: cd backend && pip install -r requirements.txt && uvicorn app.main:app --reload  
Frontend: cd frontend && npm install && npm run dev  

Docker: docker-compose up --build  

## 📡 API Docs
Swagger: /docs  
Redoc: /redoc  

## 🧠 Security Modules
Nmap scanning, subdomain enumeration, CVE enrichment, GeoIP analysis, threat scoring engine, real-time alerts.

## 📈 Roadmap
AI threat detection, SIEM integration, email/SMS alerts, multi-tenant system, advanced anomaly detection, cloud deployment.

## 👨‍💻 Author
Souhail (SOUH4IL-dev) – Full-Stack & Cybersecurity Developer  
GitHub: https://github.com/SOUH4IL-dev  

## 📜 License
MIT License
