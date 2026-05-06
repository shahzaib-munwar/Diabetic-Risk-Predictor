#  Diabetes Risk Prediction

A machine learning web app that predicts the likelihood of diabetes based on 8 clinical measurements. Built with **Random Forest** and **Gradio**, deployed 


## About the Project

**Diabetes Risk Prediction** is a free, open‑source tool that helps individuals assess their risk of diabetes using only basic health information. The model is trained on the Pima Indians Diabetes Dataset and achieves ~80% accuracy. Users interact with a clean web interface, enter 8 numbers (glucose, BMI, age, etc.), and instantly receive a prediction with a confidence percentage.

This project is intended for **educational and research purposes** – to demonstrate how machine learning can be applied to healthcare problems.

## Problem Statement

- **537 million** adults worldwide have diabetes (IDF 2024)
- **1 in 2** people with diabetes are undiagnosed
- Early detection can prevent complications: blindness, kidney failure, heart disease, stroke
- Many people lack access to affordable, non‑invasive screening

Our model offers a **free, instant, private** risk assessment.

## Dataset

**Pima Indians Diabetes Dataset** (UCI / Kaggle)

| Property | Details |
|----------|---------|
| Source | National Institute of Diabetes and Digestive and Kidney Diseases |
| Samples | 768 |
| Features | 8 clinical measurements |
| Target | 0 = non‑diabetic, 1 = diabetic |
| Population | Female Pima Indians (Arizona, USA) |

**Preprocessing:**  
- Zeros in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI` are physiologically impossible → replaced with column medians.
- Feature scaling using `StandardScaler`.

## Model Performance

| Metric | Value |
|--------|-------|
| Accuracy | 79.9% |
| ROC‑AUC | 0.85 |
| Cross‑validation (5‑fold) | 78.3% ± 0.04 |
| Precision (diabetic class) | 0.70 |
| Recall (diabetic class) | 0.62 |

**Top 5 most important features:**
1. Glucose (24%)
2. BMI (15%)
3. Age (13%)
4. Pregnancies (11%)
5. Diabetes Pedigree Function (10%)

## Features

- ✅ **Real‑time prediction** – no waiting, no API key
- ✅ **Confidence score** – probability of being diabetic
- ✅ **Example cases** – one‑click test inputs
- ✅ **Clean, responsive UI** – works on mobile and desktop
- ✅ **Model persistency** – trained model saved and reused
- ✅ **Batch prediction** (optional) – CSV input/output

## Tech Stack

| Layer | Technology |
|-------|-------------|
| Language | Python 3.9+ |
| ML framework | scikit‑learn (Random Forest) |
| Data handling | pandas, numpy |
| Web UI | Gradio |
| Deployment | Hugging Face Spaces |
| Serialization | joblib |
| Version control | Git / GitHub |

## Installation & Local Setup

### Prerequisites
- Python 3.9 or higher
- pip

### Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/diabetes-prediction.git
cd diabetes-prediction
