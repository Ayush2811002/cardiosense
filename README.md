

# Smart Health Monitoring and Assistance System

## Overview

Heart attack cases are increasing due to lifestyle, stress, and late detection. Many patients, especially in remote areas, lack timely medical help. Current monitoring tools are often expensive and disconnected from a patient’s medical history, leading to preventable emergencies.

**Smart Health Monitoring and Assistance System** bridges this gap with an affordable IoT-based health monitoring solution powered by AI, Conversational Assistant, and a Smart Health Card.

## Key Features

* **ECG & Pulse Recording:** Patients record vitals through an IoT device (ESP8266/ESP32).
* **Doctor & Patient Dashboards:** Patients get simple summaries and alerts; doctors get detailed historical reports.
* **AI Predictions (planned):** Analyze vitals + history to predict risk and notify caregivers.
* **Smart Health Card:** Securely stores lifetime medical records accessible to authorized doctors.
* **Conversational AI Assistant:** Chatbot with **Agora** integration for real-time voice/video consultations.
* **Seamless Access:** Login via Health ID + OTP; doctors can scan RFID card or use Patient ID.

## Current Flow

1. **Patient Registration** — Login via Health ID + mobile OTP, view vitals & history.
2. **Doctor Access** — Scan RFID Smart Card or enter Patient ID to view/update records.
3. **Monitoring & Alerts** — IoT device records ECG & pulse, syncs to Firebase Realtime Database.

## Tech Stack (Current)

* **Next.js** — Frontend + backend endpoints
* **Firebase Auth** — Health ID + OTP login
* **Firebase Realtime DB** — Store vitals, logs, and doctor updates
* **Agora** — Real-time voice/video consultations

## Goal

Provide affordable, accessible, and intelligent healthcare monitoring to reduce heart-attack fatalities via early detection, improved doctor-patient connectivity, and lifetime health tracking.

---

## Future Scope

* AI-driven health risk prediction models
* Real-time emergency alerts to family & hospitals
* Integration with wearables and hospital systems
* Support for other chronic diseases
* Government/insurance integrations using official Health IDs

---

## Contributors

Team Smart Health Monitoring and Assistance System — Hackathon Project

---

## How to run (dev)

1. Clone repo

```bash
git clone <repo-url>
cd smart-health-monitoring
```

2. Install frontend

```bash
cd frontend
npm install
npm run dev
```

3. Backend (Next.js API or Node.js)

```bash
cd backend
npm install
npm run dev
```

4. Configure Firebase

* Create a Firebase project, enable Authentication (phone/OTP) and Realtime Database.
* Add credentials to `.env.local`.

5. IoT Device

* Flash ESP32/ESP8266 with provided sketch; configure Wi‑Fi and Firebase/REST endpoint.

---

## Files included (suggested)

* `README.md` (this file)
* `frontend/` — Next.js app (UI + Agora integration)
* `backend/` — Next.js API routes or Node.js server (Firebase interactions)
* `iot/` — Arduino/ESP sketch and wiring docs
* `.github/workflows/ci.yml` — optional CI for linting/tests

---

## License

Add a license you prefer (MIT recommended for hackathons). Example: `LICENSE` with MIT text.

---

## .gitignore

(Place this file at the repository root as `.gitignore`)

```
# Node
node_modules/
.env
.env.local
.env.development.local
.env.test.local
.env.production.local

# Logs
logs
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Next.js
.next/
out/

# OS
.DS_Store
Thumbs.db

# Visual Studio Code
.vscode/

# Builds
dist/
```

---

## package.json (frontend sample)

(Place this as `frontend/package.json` — adjust scripts and deps as needed)

```json
{
  "name": "smart-health-monitoring-frontend",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  },
  "dependencies": {
    "next": "^13.5.0",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "firebase": "^9.23.0",
    "agora-rtc-sdk-ng": "^4.8.0"
  }
}
```

---

## Suggested commit message for your current commit

```
chore: initial commit — README, gitignore, frontend package.json samples for Smart Health Monitoring and Assistance System
```
