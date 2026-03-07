# Cardiovascular Risk ML – FraminghamAI

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Hackathon: Byte2Beat](https://img.shields.io/badge/Hackathon-Byte2Beat-orange)](https://byte2beat.devpost.com/)

**Interactive 10-Year Cardiovascular Risk Assessment Tool** built for the **Byte2Beat** hackathon (March 2026).

Live Demo: **[https://yourusername.github.io/cardiovascular-risk-ml/](https://kaushar-b.github.io/cardiovascular-risk-ml/))**  


### The Problem
Cardiovascular disease (CVD) remains the **leading cause of death worldwide**, claiming millions of lives each year. Early identification of risk factors and understanding how they contribute to long-term outcomes can enable timely interventions, lifestyle changes, and medical follow-up, potentially saving lives.

Traditional risk assessment tools exist, but many lack modern machine learning power, clear explanations of **why** a risk score is given, or easy public access. This project bridges that gap.

### Our Approach – FraminghamAI
We built **FraminghamAI**: an end-to-end ML pipeline + interactive web calculator that assesses **10-year cardiovascular risk** using data from the legendary **Framingham Heart Study**.

#### Why Framingham?
The Framingham Heart Study (started 1948) is one of the most influential longitudinal studies in medical history. It followed thousands of participants over decades, identifying major CVD risk factors (high blood pressure, cholesterol, smoking, diabetes, age, etc.) and creating the original risk equations still used by clinicians today.

We used a clean, de-identified subset from Kaggle:  
→ https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset

This dataset is **unique** compared to smaller/static ones (e.g., UCI Heart Disease), it captures **longitudinal patterns** from real people, making it ideal for meaningful risk assessment and interpretability (key Byte2Beat goals).

### What We Built
- **ML Model** — XGBoost classifier trained to estimate 10-year CVD risk (binary outcome: developed event or not within follow-up)
- **Interpretability** — SHAP values explain which factors (e.g., systolic BP, age, smoking) drive the risk score the most — crucial for trust and clinical relevance
- **Performance** — Strong AUC-ROC (~0.91), balanced accuracy, precision/recall in notebook
- **Web Demo** — Fully static single-page app hosted on **GitHub Pages** (no server/backend needed)
  - Users input key risk factors (age, sex, cholesterol, BP, smoking, diabetes)
  - JavaScript calculates an approximate risk level (inspired by classic Framingham equations + our ML insights)
  - Visual bar + risk category (low/moderate/high) with guidance
- **Reproducibility** — One-click Colab notebook for training, evaluation, SHAP plots, and model export

### How the Web Demo Works
The live calculator runs **entirely in the browser** using vanilla JavaScript + Tailwind CSS:
1. User fills simple form with clinical values
2. JS computes a composite score (blending classic Framingham logic with our ML-derived feature weights)
3. Displays percentage risk + color-coded bar + plain-language interpretation
4. No data leaves your device, privacy-focused and instant

This makes it **practical** and scalable: anyone with a phone/browser can use it for awareness, education, or personal monitoring.

### Byte2Beat Alignment
This project directly targets the hackathon's core themes:
- **Creativity** → Modern ML + SHAP explanations + public web tool on top of gold-standard longitudinal data
- **Practicality** → Static site = zero-cost hosting, instant access, real-world motivation (people want quick self-checks)
- **Presentation** → Clean GitHub Pages demo + clear README + 3-page PDF report
- **Technical Complexity** → XGBoost, hyperparameter tuning, SHAP interpretability, reproducible pipeline

### Submission Materials (for Devpost)
- **PDF Report** (2–3+ pages): [report.pdf](file:///C:/Users/doveg/Desktop/Byte2Beat/FraminghamAI_Report_Kaushar.pdf) — problem framing, methods, evaluation, results
- **Reproducible Notebook**: [Colab link]((https://colab.research.google.com/drive/1yIxG-tbrjmAflik7jjlZSdKF6DIx28wn?usp=sharing)) — data prep, model training, SHAP analysis, export
- **Live Demo**: This GitHub Pages site

### Tech Stack
- Python: pandas, scikit-learn, xgboost, shap
- Frontend: HTML, Tailwind CSS, vanilla JavaScript
- Hosting: GitHub Pages


Built by **Kaushar B** for **Byte2Beat** — turning bytes into tools that help beat cardiovascular disease.
