# 🚀 IntelliSOC – Smart Cyber Threat Detection System (Mini SIEM)

IntelliSOC is a full-stack Security Information and Event Management (SIEM) system developed as a collaborative project, focused on real-time cyber threat detection and log analysis.

This project was led from a cybersecurity perspective by Vansh Tiwari and Josh Yadav, while Keshav Gupta contributed as a Full Stack Developer, building and integrating the application across frontend and backend systems.

The system processes system logs, correlates events, and provides actionable insights through an intuitive and interactive dashboard. It is designed to detect suspicious activities such as brute-force attacks, repeated failed login attempts, and anomalous behavior patterns using rule-based and intelligent detection techniques.

## ⚠️ Problem

Modern systems generate massive volumes of logs, but analyzing them manually is:

* ⏳ Time-consuming
* ❌ Error-prone
* 🚫 Inefficient for real-time threat detection

Security teams need automated systems to quickly identify threats and reduce manual workload.

---

## 💡 Solution

IntelliSOC automates log analysis by:

* 🔍 Detecting cyber attacks instantly
* 🔗 Correlating multiple events to uncover real threats
* 🧠 Providing clear, explainable insights

It simulates a real-world SIEM system used in enterprise cybersecurity environments.

---

## 🎬 Demo Flow

1. Upload a `.log` file
2. System parses and structures logs
3. Detects threats like brute force & account compromise
4. Correlates events and assigns risk scores
5. Displays results in an interactive dashboard
6. Export results as CSV for further analysis

---

## 💡 Key Differentiators

* 🔍 **Explainable Alerts** – clear reasoning behind every detection
* ⏱️ **Time-Based Behavioral Analysis**
* 📊 **Session-Based Log Isolation**
* ⚡ **Lightweight SIEM Simulation** (fast & deployable)

---

## 🚀 Features

* **File Ingestion:** Upload `.log` files directly
* **Parsing Engine:** Converts raw logs → structured JSON
* **Threat Detection Engine:**

  * Brute Force Attack detection
  * Suspicious multi-user IP activity
* **Correlation Engine:** Detects account compromise patterns
* **Time-Based Logic & Aggregation:** Focuses on recent events and avoids duplicate alerts
* **Enrichment Layer:**

  * Risk scoring (0–100)
  * MITRE ATT&CK mapping
  * Human-readable explanations
* **Session Management:** Isolates each upload for clean analysis
* **Export Reports:** Download results as CSV

---

## 🏗️ Architecture

```mermaid
graph TD;
    A[User Uploads .log] -->|Frontend API Call| B(Backend API)
    B --> C{Parsing Engine}
    C -->|Structured JSON| D[Detection Engine]
    D --> E[Correlation Engine]
    E --> F[Enrichment Layer]
    F -->|Risk Scoring & MITRE| G[(PostgreSQL DB)]
    G -->|Alerts & Analytics API| H[Frontend Dashboard]
```

---

## 🛠️ Tech Stack

### Frontend

* React 19 + TypeScript + Vite
* Tailwind CSS
* Recharts
* Lucide React

### Backend

* Node.js + Express + TypeScript
* Multer (file upload)
* Prisma ORM

### Database

* PostgreSQL

---

## 🚀 Getting Started

### Prerequisites

* Node.js (v18+)
* PostgreSQL

---

### 1️⃣ Database Setup

```bash
cd backend
echo "DATABASE_URL=postgresql://USER:PASSWORD@localhost:5432/intellisoc" > .env
```

---

### 2️⃣ Backend Setup

```bash
cd backend
npm install
npx prisma generate
npx prisma migrate dev --name init
npm run dev
```

---

### 3️⃣ Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

## 🌍 Real-World Impact

IntelliSOC helps security teams:

* ⚡ Detect attacks faster
* 🧠 Understand threat patterns
* 🛡️ Take immediate action

This project demonstrates how real-world SIEM tools operate in modern cybersecurity environments.

---

## 🚀 Future Enhancements

* Real-time log streaming (WebSockets)
* AI/ML-based anomaly detection
* Integration with threat intelligence APIs
* Role-based authentication

---

👥 Team Contributions
Vansh Tiwari
Lead – Cybersecurity Analysis & Threat Detection
Josh Yadav
Cybersecurity Research & Detection Logic
Keshav Gupta
Full Stack Development (Frontend & Backend Integration)


---

## 📝 License

This project is licensed under the MIT License.
