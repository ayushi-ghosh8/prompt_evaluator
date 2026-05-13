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

This project demonstrates a modern DevOps + AI workflow with automated builds, monitoring, and deployment.

🚀 Features
🔹 Prompt Evaluation

Evaluate prompts using deterministic metrics such as:

Clarity
Specificity
Ambiguity
Instruction quality
Keyword relevance
Conciseness
🔹 Prompt Optimization

Generate optimization suggestions for weak prompts.

🔹 A/B Prompt Testing

Compare:

Prompt A vs Prompt B
Side-by-side scores
Regression detection
Winner recommendation
🔹 Multi-Model Comparison

Compare responses from:

Groq
Gemini
HuggingFace

Metrics include:

Latency
Quality score
Best model recommendation
🔹 Prompt Versioning & History
Save prompts
Load previous versions
Track regression changes
🔹 Feedback Capture

Supports:

Thumbs up/down
User comments
Backend storage for analysis
🔹 Security Features
Prompt injection detection
Safe fallback responses
API key validation
🧩 Tech Stack
Category	Technology
Frontend	React + Vite
Backend	FastAPI
Database	MongoDB Atlas
Containerization	Docker
CI/CD	Jenkins
Code Analysis	SonarQube
Monitoring	Prometheus
Deployment	Vercel + Render
🏗️ System Architecture
GitHub Repository
        ↓
Jenkins CI/CD Pipeline
        ↓
Build + Validation
        ↓
SonarQube Static Analysis
        ↓
Docker Compose Local Deployment
        ↓
Frontend + Backend + MongoDB
        ↓
Prometheus Metrics Collection
📂 Project Structure
Prompt_Evaluator/
│
├── backend/
│   ├── api/
│   ├── db/
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
⚙️ Local Setup
1️⃣ Clone Repository
git clone https://github.com/ayushi-ghosh8/prompt_evaluator.git

cd prompt_evaluator
🖥️ Backend Setup
cd backend

Create virtual environment:

python -m venv venv

Activate virtual environment:

Windows
venv\Scripts\activate
Linux / Mac
source venv/bin/activate

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

Install dependencies:

npm install

Run frontend:

npm run dev

Frontend available at:

http://localhost:5173
🔐 Environment Variables

Create .env inside backend/

GROQ_API_KEY=your_groq_key
GOOGLE_API_KEY=your_google_key
HUGGINGFACE_API_KEY=your_huggingface_key
MONGO_URI=your_mongodb_uri

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

Jenkins	http://localhost:8080

SonarQube	http://localhost:9000
☁️ Cloud Deployment
Component	Platform
Frontend	Vercel
Backend	Render
Database	MongoDB Atlas
📊 Prometheus Monitoring

Prometheus collects FastAPI metrics from:

/metrics

Metrics include:

HTTP requests
Request latency
Endpoint activity
Backend health
🔄 Jenkins CI/CD Pipeline

The Jenkins pipeline automates:

GitHub checkout
Backend validation
Frontend build
SonarQube analysis
Deployment verification
Pipeline Stages
Checkout
Backend Validation
Frontend Build
SonarQube Analysis
Cleanup
🔍 SonarQube Analysis

SonarQube performs:

Static code analysis
Bug detection
Vulnerability scanning
Code smell analysis
Maintainability analysis

Project dashboard:

http://localhost:9000
🐳 Docker Compose Services

The project runs:

Frontend container
Backend container
MongoDB container
Prometheus container
Jenkins container
SonarQube container

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
✅ Current Status
Feature	Status
FastAPI Backend	✅
React Frontend	✅
MongoDB Integration	✅
Docker Compose	✅
Jenkins CI/CD	✅
SonarQube Analysis	✅
Prometheus Monitoring	✅
Cloud Deployment	✅
📌 Future Improvements
Kubernetes deployment
Automated testing pipeline
Alerting system
Advanced analytics dashboard
User authentication
AI-based prompt recommendations
