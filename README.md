Prompt Evaluation & Experimentation System
📌 Project Overview

The Prompt Evaluation & Experimentation System is a full-stack AI prompt analysis platform designed to evaluate, compare, optimize, and monitor prompts used with Large Language Models (LLMs).

The project combines:

FastAPI backend
React + Vite frontend
MongoDB database
Docker containerization
Jenkins CI/CD pipeline
SonarQube static code analysis
Prometheus monitoring
Grafana observability dashboards

This project demonstrates a modern DevOps + AI workflow with automated builds, monitoring, and deployment.

🚀 Features
🔹 Prompt Evaluation

Evaluate prompts using deterministic metrics such as:

clarity
specificity
ambiguity
instruction quality
keyword relevance
conciseness
🔹 Prompt Optimization

Generate optimization suggestions for weak prompts.

🔹 A/B Prompt Testing

Compare:

Prompt A vs Prompt B
side-by-side scores
regression detection
winner recommendation
🔹 Multi-Model Comparison

Compare responses from:

Groq
Gemini
HuggingFace

Metrics include:

latency
quality score
best model recommendation
🔹 Prompt Versioning & History
save prompts
load previous versions
track regression changes
🔹 Feedback Capture

Supports:

thumbs up/down
user comments
backend storage for analysis
🔹 Security Features
prompt injection detection
safe fallback responses
API key validation
🧩 Tech Stack
Category	Technology
Frontend	React + Vite
Backend	FastAPI
Database	MongoDB
Containerization	Docker
CI/CD	Jenkins
Code Analysis	SonarQube
Monitoring	Prometheus
Visualization	Grafana
🏗️ System Architecture
GitHub Repository
        ↓
Jenkins CI/CD Pipeline
        ↓
Build + Validation
        ↓
SonarQube Static Analysis
        ↓
Docker Compose Deployment
        ↓
Frontend + Backend + MongoDB
        ↓
Prometheus Metrics Collection
        ↓
Grafana Monitoring Dashboard
📂 Project Structure
Prompt_Evaluator/
│
├── backend/
│   ├── api/
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
├── Jenkinsfile
├── docker-compose.yml
├── prometheus.yml
└── README.md
⚙️ Local Setup
1️⃣ Clone Repository
git clone https://github.com/ayushi-ghosh8/prompt_evaluator.git

cd prompt_evaluator
🖥️ Backend Setup
cd backend

python3 -m venv venv

source venv/bin/activate
Windows
venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt

Run backend:

uvicorn main:app --reload --port 8000

Backend available at:

http://localhost:8000

FastAPI docs:

http://localhost:8000/docs
🎨 Frontend Setup
cd frontend

npm install

npm run dev

Frontend available at:

http://localhost:5173
🔐 Environment Variables

Create .env inside backend:

GROQ_API_KEY=your_groq_key
GOOGLE_API_KEY=your_google_key
HUGGINGFACE_API_KEY=your_huggingface_key

If API keys are unavailable, the system uses safe mock responses.

🐳 Docker Setup
Build & Run Entire Stack
docker compose up --build
🌐 Docker Service URLs
Service	URL
Frontend	http://localhost:3000

Backend	http://localhost:8000

FastAPI Docs	http://localhost:8000/docs

MongoDB	mongodb://localhost:27017
Prometheus	http://localhost:9090

Grafana	http://localhost:3001

Jenkins	http://localhost:8080

SonarQube	http://localhost:9000
📊 Prometheus Monitoring

Prometheus collects FastAPI metrics from:

/metrics

Metrics include:

HTTP requests
request latency
endpoint activity
backend health
📈 Grafana Dashboards

Grafana visualizes:

API traffic
request count
monitoring graphs
Prometheus metrics

Default login:

Username	Password
admin	admin
🔄 Jenkins CI/CD Pipeline

The Jenkins pipeline automates:

GitHub checkout
backend validation
frontend build
SonarQube analysis
deployment verification

Pipeline stages:

Checkout
Backend Validation
Frontend Build
SonarQube Analysis
Cleanup
🔍 SonarQube Analysis

SonarQube performs:

static code analysis
bug detection
vulnerability scanning
code smell analysis
maintainability analysis

Project dashboard:

http://localhost:9000
🐳 Docker Compose Services

The project runs:

frontend container
backend container
mongodb container
prometheus container
grafana container
jenkins container
sonarqube container

using a single command:

docker compose up --build
📌 Important API Endpoints
Endpoint	Description
POST /api/analyze	Evaluate prompt
POST /api/optimize	Optimize prompt
POST /api/compare	Compare models
POST /api/ab-test	A/B prompt testing
POST /api/feedback	Submit feedback
GET /api/prompt-history	Fetch history
POST /api/prompt-history	Save prompt
GET /metrics	Prometheus metrics
🧪 Example DevOps Workflow
Developer pushes code to GitHub
            ↓
Jenkins pipeline triggers automatically
            ↓
Backend + Frontend build validation
            ↓
SonarQube performs code analysis
            ↓
Docker containers deployed
            ↓
Prometheus collects metrics
            ↓
Grafana visualizes monitoring dashboards

✅ Current Status
Feature	Status
FastAPI Backend	✅
React Frontend	✅
MongoDB Integration	✅
Docker Compose	✅
Jenkins CI/CD	✅
SonarQube Analysis	✅
Prometheus Monitoring	✅
Grafana Dashboard	✅

📌 Future Improvements
Kubernetes deployment
automated testing pipeline
alerting system
advanced analytics dashboard
user authentication
cloud deployment
AI-based prompt recommendations