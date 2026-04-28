# 🛡️ Cyber Security Dashboard v1

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green?logo=fastapi)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18+-61DAFB?logo=react)](https://react.dev/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue?logo=docker)](https://www.docker.com/)

**Cyber Security Dashboard v1** is a full-stack security observability platform designed to centralize asset monitoring, automate vulnerability scanning, and provide real-time threat intelligence. Built for security engineers and SOC analysts, it provides a scalable, modular foundation for simulating and managing security operations.

---

## 🧠 Core Concept
This platform mimics a real-world security pipeline, automating the journey from **discovery** to **remediation**:
1. **Discovery:** Assets are identified via subdomain enumeration.
2. **Scanning:** Automated Nmap integration assesses the attack surface.
3. **Enrichment:** Findings are mapped against CVE and GeoIP databases for context.
4. **Analysis:** Vulnerabilities are aggregated and severity-scored.
5. **Monitoring:** Real-time updates via WebSockets trigger instant alerts.

---

## 🏗️ Technical Architecture

### Backend (FastAPI)
The backend follows a **Clean Architecture** approach:
* **API Layer:** RESTful endpoints and WebSocket streams.
* **Services Layer:** Orchestrates business logic (Scans, Findings, Reports).
* **Integrations:** Adapter-based design for security tools (Nmap, CVE).
* **Repositories:** Data access abstraction layer.

### Frontend (React)
A **feature-based** modular architecture:
* **Real-time Engine:** WebSocket client for live dashboard updates.
* **Component Library:** Built with TailwindCSS for UI consistency.
* **State Management:** Data synchronization with React Query.

---

## 🚀 Getting Started

### Prerequisites
* Python 3.10+
* Node.js 18+
* Docker & Docker Compose
* Nmap (installed on the host or in the container)

### Environment Setup
1. Copy the example environment file:
   ```bash
   cp .env.example .env
