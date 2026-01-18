# Counterfactual Explanations for Stroke Prediction

This project applies **counterfactual explanations** to a clinical stroke dataset to interpret machine learning predictions and to **detect data artifacts and clinically implausible patterns** that are not revealed by standard exploratory data analysis.

Rather than focusing solely on model accuracy, the project demonstrates how counterfactual explanations can be utilized as a **diagnostic tool** to enhance model reliability and clinical plausibility.

---

## Project Objectives

- Predict stroke occurrence using machine learning models  
- Interpret model predictions using **counterfactual explanations**  
- Use counterfactuals to detect **implausible patterns and rare outliers**  
- Improve data quality and interpretability beyond standard statistical analysis  

---

## Dataset Overview

The dataset contains demographic, clinical, and lifestyle-related features commonly associated with stroke risk, including:

- Demographics: age, gender, marital status, residence type  
- Medical history: hypertension, heart disease  
- Clinical measurements: BMI, average glucose level  
- Lifestyle factors: smoking status  
- Target variable: **stroke (0 = No, 1 = Yes)**  

---

## Models Used

Tree-based machine learning models are used due to their robustness to outliers and compatibility with counterfactual explanation methods:

- Decision Tree–based models  
- Ensemble methods (e.g., Random Forest)  

---

## Explainable AI Technique: Counterfactual Explanations

**Counterfactual explanations** identify the minimal changes to input features required to change a model’s prediction.

In this project, counterfactuals are used for:

- **Local interpretation** of individual predictions  
- **Identifying unrealistic or contradictory model behavior**  
- **Detecting rare but influential outliers** that standard data analysis fails to reveal  

Unlike global feature importance or distribution-based analysis, counterfactual explanations expose **decision-level inconsistencies** and highlight cases where the model relies on **clinically implausible relationships**.

---

## Counterfactuals as a Diagnostic Tool

Analysis of counterfactual explanations revealed:

- Instances where reducing average glucose levels increased predicted stroke risk, contradicting medical knowledge  
- Non-stroke cases with extremely high BMI values that distorted counterfactual recommendations  

These patterns were not apparent through standard exploratory analysis alone and motivated **targeted data cleaning** to improve clinical plausibility and interpretability.

---

## Repository Structure

```text
.
├── digitalProject.ipynb     # Main analysis and counterfactual explanations
├── README.md                # Project overview
└── data/                    # Dataset (if included or linked)
