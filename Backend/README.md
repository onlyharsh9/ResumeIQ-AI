# ResumeIQ AI — Backend API

Backend module of ResumeIQ AI built using Flask REST API.

This service handles resume processing, ATS score generation, keyword analysis, and career category prediction using a trained machine learning model.

---

## Tech Stack

- Python
- Flask
- TensorFlow / Keras
- Pandas
- NumPy
- Scikit-learn
- NLP-based text processing

---

## Backend Structure

backend/

├── app.py
├── resume_ann_model.keras
├── requirements.txt
└── README.md

---

## Setup

### Install Dependencies

Run:

pip install -r requirements.txt


### Model Setup

Place the trained model file:

resume_ann_model.keras

in the same directory as:

app.py

---

## Run Server

Start Flask server:

python app.py


Production:

gunicorn -w 2 -b 0.0.0.0:5000 app:app


Server URL:

http://localhost:5000

---

# API Endpoints

## 1. Health Check

### GET /health

Checks whether backend service is running.

Response:

{
  "status": "ok",
  "model": "resume_ann_model.keras"
}

---

## 2. Resume Analysis

### POST /api/analyze

Analyzes uploaded resume and generates ATS report.

Request Type:

multipart/form-data


Parameters:

resume:
Resume file (PDF/DOCX/TXT)

job_description:
Job description text

jd_file:
Optional job description file


Response Example:

{
  "success": true,
  "ats_score": 78.4,
  "predicted_category": {
    "category": "Software Engineer",
    "confidence": 84.2
  },
  "score_breakdown": {
    "keyword_match": 68,
    "sections": 85.7,
    "length": 90,
    "format": 100
  }
}

---

## 3. Career Category Prediction

### POST /api/predict-category

Predicts career category from resume only.


Parameter:

resume:
Resume file


Response Example:

{
  "category": "Data Scientist",
  "confidence": 84.2
}

---

## 4. Categories

### GET /api/categories

Returns all supported career categories.

---

# ATS Score Components

Keyword Match:
60%

Resume Sections:
20%

Length:
10%

Format:
10%

---

# Supported Career Categories

- Software Engineer
- Data Scientist
- Data Analyst
- Machine Learning Engineer
- AI Engineer
- Backend Developer
- Frontend Developer
- Full Stack Developer
- DevOps Engineer
- Cloud Engineer
- Cyber Security Engineer
- Business Analyst
- Product Manager
- UI/UX Designer
- QA Engineer
- Electrical Engineer

---

# Model Information

Model Type:
Artificial Neural Network (ANN)

Purpose:
Resume career category prediction

Input:
Processed resume text features

Output:
Predicted career category with confidence score

---

# Environment

Recommended Python Version:

Python 3.10+

Required packages are listed in:

requirements.txt

---

# Backend Module

ResumeIQ AI backend provides APIs required for resume analysis, ATS scoring, and AI-based career prediction.