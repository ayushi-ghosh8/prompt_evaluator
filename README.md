# 🚀 Prompt Evaluation & Experimentation System

AI-powered platform for evaluating, optimizing, comparing, and monitoring Large Language Model (LLM) prompts using FastAPI, React, Docker, Jenkins, SonarQube, and Prometheus.

---

# 📌 Project Overview

The **Prompt Evaluation & Experimentation System** is a full-stack AI prompt analysis platform designed to:

- Evaluate prompts using deterministic metrics
- Compare prompts and models
- Optimize prompts
- Perform A/B testing
- Monitor application metrics using Prometheus
- Demonstrate a complete DevOps workflow

The project integrates modern AI engineering with DevOps practices including CI/CD, monitoring, containerization, and deployment.

---

# ✨ Features

## 🔹 Prompt Evaluation

Evaluate prompts using deterministic metrics such as:

- Clarity
- Specificity
- Ambiguity
- Instruction Quality
- Keyword Relevance
- Conciseness

---

## 🔹 Prompt Optimization

Generate optimization suggestions for weak prompts.

---

## 🔹 A/B Prompt Testing

Compare:

- Prompt A vs Prompt B
- Side-by-side scores
- Regression detection
- Winner recommendation

---

## 🔹 Multi-Model Comparison

Compare responses from:

- Groq
- Gemini
- HuggingFace

Metrics include:

- Latency
- Quality Score
- Best Model Recommendation

---

## 🔹 Prompt Versioning & History

Supports:

- Saving prompts
- Loading previous versions
- Tracking prompt changes

---

## 🔹 Feedback Capture

Supports:

- Thumbs up/down
- User comments
- Backend feedback storage

---

## 🔹 Security Features

Includes:

- Prompt injection detection
- Input validation
- Safe fallback responses
- API key validation

---

# 🧩 Tech Stack

| Category         | Technology      |
| ---------------- | --------------- |
| Frontend         | React + Vite    |
| Backend          | FastAPI         |
| Database         | MongoDB         |
| Containerization | Docker          |
| CI/CD            | Jenkins         |
| Static Analysis  | SonarQube       |
| Monitoring       | Prometheus      |
| Deployment       | Vercel + Render |

---

# 🏗️ System Architecture

- Frontend deployed on **Vercel**
- Backend deployed on **Render**
- MongoDB used for storing prompts, feedback, and metrics
- Prometheus used for continuous monitoring
- Jenkins used for CI/CD automation
- SonarQube used for static code analysis

---

# 🔄 CI/CD/CM Pipeline

The project demonstrates:

## CI — Continuous Integration

- GitHub code integration
- Jenkins automated pipeline
- Backend validation
- Frontend build
- Docker image build
- SonarQube analysis

## CD — Continuous Deployment

- Frontend deployment on Vercel
- Backend deployment on Render

## CM — Continuous Monitoring

- Prometheus metrics collection
- Backend health monitoring
- API request monitoring

---

# 📂 Project Structure

```text
Prompt_Evaluator/
│
├── backend/
│   ├── api/
│   ├── models/
│   ├── main.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── nginx.conf
│   └── Dockerfile
│
├── jenkins/
│   └── Dockerfile
│
├── Jenkinsfile
├── docker-compose.yml
├── prometheus.yml
└── README.md
```

---

# ⚙️ Local Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/ayushi-ghosh8/prompt_evaluator.git

cd prompt_evaluator
```

---

# 🖥️ Backend Setup

```bash
cd backend
```

## Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv

source venv/bin/activate
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run Backend

```bash
uvicorn main:app --reload --port 8000
```

Backend available at:

```text
http://localhost:8000
```

FastAPI Docs:

```text
http://localhost:8000/docs
```

---

# 🎨 Frontend Setup

```bash
cd frontend
```

## Install Dependencies

```bash
npm install
```

## Run Frontend

```bash
npm run dev
```

Frontend available at:

```text
http://localhost:5173
```

---

# 🔐 Environment Variables

Create `.env` inside `backend/`

```env
GROQ_API_KEY=your_groq_key
GOOGLE_API_KEY=your_google_key
HUGGINGFACE_API_KEY=your_huggingface_key
MONGO_URI=your_mongodb_uri
```

If API keys are unavailable, the system uses safe mock responses.

---

# 🐳 Docker Setup

## Build & Run Entire Stack

```bash
docker compose up --build
```

---

# 🌐 Docker Service URLs

| Service      | URL                        |
| ------------ | -------------------------- |
| Frontend     | http://localhost:3000      |
| Backend      | http://localhost:8000      |
| FastAPI Docs | http://localhost:8000/docs |
| MongoDB      | mongodb://localhost:27017  |
| Prometheus   | http://localhost:9090      |
| Jenkins      | http://localhost:8080      |
| SonarQube    | http://localhost:9000      |

---

# ☁️ Deployment

| Component | Platform |
| --------- | -------- |
| Frontend  | Vercel   |
| Backend   | Render   |

---

# 📊 Prometheus Monitoring

Prometheus collects FastAPI metrics from:

```text
/metrics
```

Metrics include:

- HTTP requests
- Request latency
- API throughput
- Backend health
- Error rates

Prometheus Dashboard:

```text
http://localhost:9090
```

---

# 🔄 Jenkins CI/CD Pipeline

The Jenkins pipeline automates:

- GitHub checkout
- Backend validation
- Frontend build
- Docker build
- SonarQube analysis

Pipeline stages:

1. Checkout
2. Backend Validation
3. Frontend Build
4. SonarQube Analysis
5. Docker Build
6. Cleanup

Jenkins Dashboard:

```text
http://localhost:8080
```

---

# 🔍 SonarQube Analysis

SonarQube performs:

- Static code analysis
- Bug detection
- Vulnerability scanning
- Security hotspot analysis
- Code smell detection

SonarQube Dashboard:

```text
http://localhost:9000
```

---

# 📌 Important API Endpoints

| Endpoint             | Description        |
| -------------------- | ------------------ |
| POST `/api/analyze`  | Evaluate prompt    |
| POST `/api/optimize` | Optimize prompt    |
| POST `/api/compare`  | Compare models     |
| POST `/api/ab-test`  | A/B prompt testing |
| POST `/api/feedback` | Submit feedback    |
| GET `/metrics`       | Prometheus metrics |

---

# 🧪 Example DevOps Workflow

```text
Developer pushes code to GitHub
            ↓
Jenkins Pipeline Triggered
            ↓
Backend + Frontend Validation
            ↓
SonarQube Static Analysis
            ↓
Docker Build Process
            ↓
Deployment to Render & Vercel
            ↓
Prometheus Continuous Monitoring
```

---

# ✅ Current Status

| Feature               | Status |
| --------------------- | ------ |
| FastAPI Backend       | ✅     |
| React Frontend        | ✅     |
| MongoDB Integration   | ✅     |
| Docker Compose        | ✅     |
| Jenkins CI/CD         | ✅     |
| SonarQube Analysis    | ✅     |
| Prometheus Monitoring | ✅     |
| Render Deployment     | ✅     |
| Vercel Deployment     | ✅     |

---

# 📌 Future Improvements

- Kubernetes deployment
- Automated testing pipeline
- Alerting system
- User authentication
- AI-powered analytics dashboard
- Advanced observability

---

# 📄 License

This project is developed for academic and educational purposes.
