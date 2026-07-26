# ResumeIQ AI — ATS Resume Checker
## Live Demo

https://resumeiq-ai-pqc0.onrender.com/

ResumeIQ AI is an AI-powered ATS resume analysis platform that helps candidates improve their resumes by analyzing ATS compatibility, keyword matching, resume structure, and career category prediction.

The system uses Natural Language Processing (NLP) techniques and an Artificial Neural Network (ANN) based machine learning model to analyze resumes and provide actionable improvement suggestions.

---

## 🚀 Features

- Resume parsing from PDF, DOCX, and TXT files
- AI-powered ATS score calculation
- Job description keyword matching
- Resume section analysis
- Career category prediction
- Missing keywords and skill recommendations
- Resume improvement suggestions
- Fast REST API based architecture

---

## 🛠️ Tech Stack

### Frontend
- HTML
- CSS
- JavaScript

### Backend
- Python
- Flask
- REST API

### Machine Learning
- TensorFlow / Keras
- Artificial Neural Network (ANN)
- NLP-based resume analysis
- Resume classification model

### Libraries
- Pandas
- NumPy
- Scikit-learn

---

## 📂 Project Structure

📂 Project Structure

ResumeIQ-AI/
│
├── Backend/
│   ├── app.py
│   ├── index.html
│   ├── requirements.txt
│   ├── runtime.txt
│   └── resume_ann_model.keras
│
├── Data Preprocessing/
│   ├── ResumeIQ_AI.ipynb
│   └── Data Set.zip
│
├── Front end/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── .gitignore
├── README.md
---

## ⚙️ Installation & Setup

### Clone Repository

git clone <repository-url>

### Backend Setup

Go to backend folder:

cd backend

Install dependencies:

pip install -r requirements.txt

Place the trained model file:

resume_ann_model.keras

in the same folder as:

app.py

---

## ▶️ Running the Application

Start backend server:

python app.py

Production:

gunicorn -w 2 -b 0.0.0.0:5000 app:app

Backend runs on:

http://localhost:5000

---

# 🔗 API Documentation

## GET /health

Checks backend server status.

Response:

{
 "status": "ok",
 "model": "resume_ann_model.keras",
 "categories": 24,
 "input_dim": 5000
}

---

## POST /api/analyze

Analyzes resume with job description and generates ATS report.

Request:

multipart/form-data

Fields:

resume:
Resume file (PDF/DOCX/TXT)

job_description:
Job description text

jd_file:
Optional job description file

Example Response:

{
 "success": true,
 "ats_score": 78.4,
 "predicted_category": {
   "category": "Python Developer",
   "confidence": 72.3
 },
 "score_breakdown": {
   "keyword_match": 68,
   "sections": 85.7,
   "length": 90,
   "format": 100
 }
}

---

## POST /api/predict-category

Predicts the best career category from resume skills.

Example:

{
 "category": "Data Science",
 "confidence": 84.2
}

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

# 📊 ATS Score Calculation

ATS score is calculated using:

| Component | Weight |
|-----------|--------|
| Keyword Match | 60% |
| Resume Sections | 20% |
| Length | 10% |
| Format | 10% |

---

# 🧠 How It Works

1. User uploads resume.
2. Resume text is extracted.
3. NLP techniques analyze skills and keywords.
4. ANN model predicts suitable career category.
5. ATS score is generated.
6. Improvement suggestions are provided.

---

# 🎯 Use Cases

- Students preparing for placements
- Job seekers improving resumes
- Fresh graduates optimizing ATS scores
- Recruiters analyzing candidate profiles

---

# 🔮 Future Enhancements

- LLM based resume suggestions
- Resume rewriting assistant
- LinkedIn profile analysis
- More career categories
- Resume comparison system
- Automated resume improvement

---

# 📸 Screenshots

Add application screenshots here.

---

# 👨‍💻 Project Information

## ResumeIQ AI — ATS Resume Checker

An AI-powered resume analysis system designed to help candidates improve ATS compatibility, identify missing skills, and optimize resumes for better job opportunities.

---

## Author

Developed as an AI + Machine Learning based resume analysis project.
