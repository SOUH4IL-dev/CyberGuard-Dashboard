🛡️ Cyber Security Dashboard v1
FastAPI • React • Real-Time Threat Monitoring Platform

An advanced full-stack cybersecurity monitoring dashboard built with Python (FastAPI) and React, designed to centralize asset monitoring, vulnerability scanning, findings analysis, and real-time security alerts in a scalable and modular architecture.

📌 Overview

Cyber Security Dashboard v1 is a professional-grade security observability platform focused on:

Centralized asset management
Automated vulnerability scanning
Real-time security findings & alerts
Interactive security dashboard
Scalable microservice-style backend design

It is built for developers and security engineers who want to simulate or build SOC (Security Operations Center)-like systems.

🧠 Core Concept

The platform simulates a real-world security monitoring pipeline:

Assets discovery & management
Automated scanning (Nmap / subdomain enumeration)
CVE & enrichment mapping
Findings aggregation & severity scoring
Alerts + real-time websocket updates
Reporting & audit logging
🏗️ Architecture
🔙 Backend (FastAPI)

Modular layered architecture:

API Layer → REST + WebSocket endpoints
Services Layer → Business logic (scans, findings, alerts)
Repositories Layer → Database abstraction
Integrations Layer → External security tools (Nmap, CVE, GeoIP)
Tasks Layer → Background scanning & reporting jobs
WebSocket Layer → Real-time event streaming
🎨 Frontend (React)

Feature-based architecture:

Authentication system
Real-time dashboard
Assets management module
Findings & vulnerability tracking
Scans monitoring panel
Reports visualization
Settings & configuration panel
⚙️ Key Features
🔐 Security Core
JWT authentication system
Role-based access control (RBAC)
Audit logging middleware
Rate limiting protection
🧪 Scanning Engine
Nmap integration adapter
Subdomain enumeration module
Automated scan scheduling
Background scan tasks
📊 Dashboard Intelligence
Asset risk overview
Vulnerability severity scoring
Live alerts stream
Security metrics visualization
🚨 Alert System
Real-time WebSocket alerts
Severity-based classification
Alert persistence & history
📄 Reporting Engine
Automated security reports
Exportable findings summaries
Scheduled report generation
🧩 Backend Structure
backend/
│
├── app/
│   ├── main.py
│   ├── api/
│   │   ├── v1/
│   │   │   ├── endpoints/
│   │   │   │   ├── auth.py
│   │   │   │   ├── dashboard.py
│   │   │   │   ├── assets.py
│   │   │   │   ├── scans.py
│   │   │   │   ├── findings.py
│   │   │   │   ├── reports.py
│   │   │   │   ├── users.py
│   │   │   │   ├── websocket.py
│   │   ├── middleware/
│   │   │   ├── audit.py
│   │   │   ├── rate_limit.py
│   │
│   ├── services/
│   ├── repositories/
│   ├── models/
│   ├── schemas/
│   ├── integrations/
│   ├── tasks/
│   ├── websocket/
│   ├── core/
│   ├── utils/
🎨 Frontend Structure
frontend/
│
├── src/
│   ├── features/
│   │   ├── auth/
│   │   ├── dashboard/
│   │   ├── assets/
│   │   ├── scans/
│   │   ├── findings/
│   │   ├── reports/
│   │   ├── settings/
│   │
│   ├── components/
│   ├── hooks/
│   ├── services/
│   ├── store/
│   ├── utils/
│   ├── lib/
│   ├── styles/
│   ├── types/
🔌 Integrations
🛠 Security Tools
Nmap scanner adapter
Subdomain enumeration tool
CVE enrichment API
GeoIP enrichment module
📡 Real-Time Systems
WebSocket manager
Live dashboard updates
Streaming alerts engine
📊 Features Breakdown
Module	Description
Assets	Manage scanned systems & hosts
Scans	Run & monitor security scans
Findings	Vulnerability tracking system
Alerts	Real-time security notifications
Reports	Automated security reporting
Users	Authentication & role management
⚙️ Environment Setup

Create a .env file:

DATABASE_URL=your_database_url
SECRET_KEY=your_secret_key
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
🚀 Installation
Backend
cd backend
pip install -r requirements.txt
Frontend
cd frontend
npm install
▶️ Run the Project
Start Backend
uvicorn app.main:app --reload
Start Frontend
npm run dev
🧠 Tech Stack
Backend
Python 3.10+
FastAPI
SQLAlchemy
WebSockets
Celery / Background Tasks
Frontend
React.js
TailwindCSS
Axios
React Query
WebSocket client
Security Tools
Nmap
CVE databases
GeoIP enrichment
📈 Roadmap
v1 (current)
Modular backend architecture ✅
Asset & scan system ✅
Findings engine ✅
Real-time alerts (WebSocket) ✅
v2 (planned)
🧠 AI-based vulnerability prioritization
📊 Advanced SOC dashboard analytics
☁️ Cloud asset integration (AWS/Azure)
🔍 Threat intelligence feeds
📱 Mobile dashboard version
🔐 Security Notice

This project is designed for:

Educational cybersecurity labs
SOC simulation environments
Authorized security testing only

Unauthorized scanning or monitoring of systems is strictly discouraged.

🤝 Contributing
Fork repository
Create feature branch
Implement changes
Submit pull request
👨‍💻 Author

Souhail

GitHub: https://github.com/SOUH4IL-dev

⭐ Support

If this project helps you or your portfolio, consider giving it a ⭐ on GitHub.
