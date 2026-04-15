# 🏥 Hospital App With AI Integration

A full-stack web application that digitizes and streamlines hospital operations — covering patient management, doctor scheduling, appointment booking, and AI-powered assistance — all in one unified platform.

---

## ✨ Key Features

* **Role-Based Access**: Separate dashboards and permissions for Patients, Doctors, and Admins.
* **Appointment Booking**: Patients can search for doctors and book appointments in real time.
* **Doctor Management**: Admins can manage doctor profiles, specializations, and availability.
* **Patient Records**: Securely store and retrieve patient history and medical records.
* **AI Integration**: Intelligent assistance for symptom checking, recommendations, or workflow automation.
* **Dockerized Deployment**: Fully containerized for consistent development and production environments.

---

## 🛠️ Tech Stack

### **Frontend**
* **Framework**: React (Vite)
* **Language**: TypeScript
* **Styling**: CSS Modules / Tailwind CSS

### **Backend**
* **Runtime**: Node.js
* **Framework**: Express.js
* **Language**: TypeScript
* **Database**: (MongoDB / PostgreSQL — configure via `.env`)
* **Authentication**: JWT

### **DevOps**
* **Containerization**: Docker & Docker Compose

---

## 📁 Project Structure

```
Hospital-App-With-AI-Integration/
├── backend/          # Express.js REST API (TypeScript)
├── frontend/         # React + Vite client (TypeScript)
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

* **Node.js** (v18+) and **npm**
* **Docker** & **Docker Compose** (for containerized setup)
* A running **MongoDB** or **PostgreSQL** instance (local or cloud)

---

### Option 1 — Docker (Recommended)

```bash
# Clone the repository
git clone https://github.com/SaqibOO7/Hospital-App-With-AI-Integration.git
cd Hospital-App-With-AI-Integration

# Build and start all services
docker-compose up --build
```

The app will be available at `http://localhost:3000` (or the port specified in your compose file).

---

### Option 2 — Manual Setup

#### 1. Clone the Repository

```bash
git clone https://github.com/SaqibOO7/Hospital-App-With-AI-Integration.git
cd Hospital-App-With-AI-Integration
```

#### 2. Backend Setup

```bash
cd backend
npm install

# Create environment file
cp .env.example .env
# Fill in your values (DB URI, JWT secret, AI API keys, etc.)

# Start the development server
npm run dev
```

#### 3. Frontend Setup

```bash
cd ../frontend
npm install

# Create environment file
cp .env.example .env
# Set VITE_API_URL=http://localhost:5000/api (or your backend port)

# Start the development server
npm run dev
```

The frontend will be available at `http://localhost:5173`.

---

## ⚙️ Environment Variables

### Backend (`backend/.env`)

| Variable | Description |
|---|---|
| `PORT` | Port for the backend server (e.g. `5000`) |
| `DB_URI` | Database connection string |
| `JWT_SECRET` | Secret key for signing JWT tokens |
| `AI_API_KEY` | API key for AI service integration |
| `NODE_ENV` | `development` or `production` |

### Frontend (`frontend/.env`)

| Variable | Description |
|---|---|
| `VITE_API_URL` | Base URL for the backend API |

---

## 🏗️ Architecture Overview

```
Client (React + TypeScript)
        │
        ▼
Backend API (Node.js / Express)
        │
        ├──▶ Database (MongoDB / PostgreSQL)
        │
        └──▶ AI Service / External API
```

1. **Frontend**: Handles all UI interactions — booking, dashboards, records — and communicates with the backend via REST API.
2. **Backend**: Acts as the API gateway, managing authentication, business logic, and database operations.
3. **AI Layer**: Integrated into the backend to power intelligent features (symptom analysis, recommendations, etc.).
