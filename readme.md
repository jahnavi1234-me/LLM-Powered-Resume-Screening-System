#  AI Resume–Job Fit Evaluator (LLM-Based)

An end-to-end Generative AI system that evaluates the compatibility between a resume and a job description using a Large Language Model (LLM).

This project extends a traditional ML baseline model (implemented separately) and demonstrates how LLMs can be used for intelligent resume screening.

---

##  Project Overview

This system:

* Uses a local LLM (**Mistral via Ollama**) for resume-job evaluation
* Generates a **match score (0–100)**
* Identifies **missing skills**
* Provides a short **AI-generated explanation**
* Includes a **Streamlit web application** for interactive use

---

##  Problem Statement

Automated resume screening is often rule-based or keyword-based.

This project explores:

> Can a Large Language Model reason about resume-job fit better than traditional ML models?

---

##  Project Architecture

Resume + Job Description
→ Prompt Engineering
→ Local LLM (Mistral via Ollama)
→ Structured JSON Output
→ Score + Missing Skills + Explanation
→ Streamlit UI

---

## 📂 Folder Structure

```
project-root/
│
├── app.py
│
|
|── train.py
|── predict.py
│── evaluate.py
│── llm_utils.py
│
├── data/
│   ├── raw/
│   │   └── resume_data.csv
│   └── processed/
│       ├── resume_data_processed.csv
│       ├── new_resumes.csv
│       └── unseen_prediction.csv
│
├── prompts/
│   └── resume_result.csv
│
├── notebooks/
│
├── requirements.txt
└── README.md
```

---

##  Dataset

Dataset used:

* Resume–Job Description Fit dataset from HuggingFace
* Contains resume text, job descriptions, and labels (Fit / No Fit)

---

 

##  Model Output Format

The LLM returns structured JSON:

```
{
  "match_score": 85,
  "missing_skills": ["SQL", "Docker"],
  "explanation": "The candidate has strong ML and Python skills but lacks backend deployment experience."
}
```

---

##  Evaluation

The project includes:

* Training pipeline
* Prediction on unseen resumes
* Accuracy-based evaluation

---

## Technologies Used

* Python
* Streamlit
* Pandas
* Ollama
* Mistral (LLM)
* Scikit-learn

---


---

##  Future Improvements

* Add RAG-based skill retrieval
* Add ML vs LLM performance comparison
* Add deployment (Render / AWS / HuggingFace Spaces)

---

##  Author

Jahnavi besabathini
Aspiring Generative AI Engineer


<img width="1920" height="1080" alt="Screenshot (203)" src="https://github.com/user-attachments/assets/ee42b343-9192-4787-baa6-6c62df26d8b4" />
<img width="1920" height="1080" alt="Screenshot (202)" src="https://github.com/user-attachments/assets/77a7623c-dbb4-4ae9-9777-8f9b5349e6c4" />
<img width="1920" height="1080" alt="Screenshot (201)" src="https://github.com/user-attachments/assets/0fcdbe6c-9ae9-4494-a69f-a0add1a51809" />



