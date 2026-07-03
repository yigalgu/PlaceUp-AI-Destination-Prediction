# ✈️ PlaceUp AI: Destination Prediction & ROI Simulator

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yigalgu/PlaceUp-AI-Destination-Prediction/blob/main/PlaceUp_Data_Challenge.ipynb)

## 📌 Project Overview
This project provides an End-to-End Machine Learning solution for **PlaceUp**, an international travel company. The core business problem was high user churn rate due to generic, non-personalized destination recommendations. 
This project builds an AI-driven recommendation engine that predicts a user's initial travel destination based on demographic and device data, enabling real-time personalization.

## 🚀 Key Features & Methodology
1. **Robust Data Preprocessing (EDA):** Handled extreme outliers (e.g., negative ages) and missing values using median imputation to ensure data integrity.
2. **Strict Pipeline to Prevent Data Leakage:** Applied Stratified Train-Test Splitting (80/20) and performed One-Hot Encoding *after* the split to avoid target leakage.
3. **Smart KPIs & Business Alignment:** Proved that traditional `Accuracy` is a misleading metric for highly imbalanced data (where NDF - No Destination Found - is the majority). Shifted focus to `F1-Score` and `Diversity` to ensure the model actually recommends profitable destinations (like US or FR).
4. **Model Benchmarking:** Compared a Baseline Logistic Regression model against an Advanced Random Forest Classifier equipped with `class_weight='balanced'`.
5. **Interactive Business ROI Simulator:** Built a dynamic UI dashboard (using `ipywidgets`) that translates classification errors and successes into **estimated monthly net profit ($)**.
6. **Model Explainability (XAI):** Extracted Feature Importances, proving that the user's `Age` accounts for >60% of the model's decision-making process.
7. **Production-Ready API Simulation:** Packaged the model into a functional Object-Oriented pipeline simulating a real-time Backend-Frontend interaction, complete with a smart **Fallback Mechanism** and dynamic marketing copy generation.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (RandomForest, LogisticRegression)
* **Data Visualization:** Matplotlib, Seaborn
* **Interactive UI:** ipywidgets, JSON, HTML

## ⚠️ Important Note for GitHub/GitLab Viewers
This notebook contains highly interactive components (Sliders, Dynamic HTML Dashboards). GitHub's static rendering does not support `ipywidgets`. 
To experience the full interactive ROI simulator and the Production API Dashboard, please click the **Open In Colab** badge at the top of this page or download the notebook to run it locally.
