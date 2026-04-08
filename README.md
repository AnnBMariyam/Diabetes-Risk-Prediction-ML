# 🏥 Diabetes Risk Prediction — Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat-square)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Neural%20Network-red?style=flat-square&logo=tensorflow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> **Can machine learning reliably detect diabetes risk from routine health indicators?**
> This project answers that question by building and comparing four ML models on real patient data — with a Neural Network achieving **97.14% accuracy and 0.976 AUC-ROC**.

---

## 📌 Project Overview

Diabetes affects over 537 million adults worldwide, yet early detection remains a major challenge. This project applies supervised machine learning to classify diabetes risk using routine patient health indicators such as glucose level, BMI, age, blood pressure, and insulin levels.

Four machine learning models were trained, tuned, and rigorously compared across five evaluation metrics to identify the most effective approach for early diabetes detection — following a complete end-to-end data science workflow.

---

## 📂 Repository Structure

```
Diabetes-Risk-Prediction-ML/
│
├── dataset/              # Raw and processed dataset files
├── notebooks/            # Jupyter notebooks (EDA, modeling, evaluation)
├── images/               # Visualizations: confusion matrices, ROC curves, feature importance
├── report/               # Full project report (PDF)
└── README.md
```

---

## 📊 Dataset

- **Source:** [Diabetes Prediction Dataset — Kaggle (iammustafatz)](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)
- **Features:** Age, Gender, BMI, Glucose Level, Blood Pressure, Insulin, HbA1c Level, Smoking History
- **Target:** Binary classification — Diabetic (1) / Non-Diabetic (0)
- **Size:** 100,000 patient records

---

## 🔧 Tech Stack

| Area | Tools |
|---|---|
| Language | Python 3.8+ |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Deep Learning | TensorFlow, Keras |
| Environment | Jupyter Notebook |

---

## ⚙️ Workflow

```
Data Loading → EDA → Preprocessing → Feature Engineering → Model Training → Evaluation → Comparison
```

1. **Exploratory Data Analysis (EDA)** — Distribution analysis, correlation heatmaps, class balance check
2. **Preprocessing** — Missing value handling, categorical encoding, feature scaling (StandardScaler)
3. **Feature Engineering** — Selected most predictive health indicators based on correlation analysis
4. **Model Training** — Trained 4 models with consistent train/test splits for fair comparison
5. **Evaluation** — Assessed each model using Accuracy, Precision, Recall, F1-Score, and AUC-ROC
6. **Visualization** — Confusion matrices, ROC curves, and feature importance plots

---

## 🤖 Models Implemented

- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest Classifier
- Neural Network (Deep Learning — TensorFlow/Keras)

---

## 📈 Results

| Model | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|---|---|---|---|---|---|
| **Neural Network** | **0.9714** | **0.9588** | **0.6950** | **0.8058** | **0.9764** |
| Random Forest | 0.9708 | 0.9532 | 0.6915 | 0.8015 | 0.9637 |
| Logistic Regression | 0.9587 | 0.8639 | 0.6130 | 0.7171 | 0.9612 |
| SVM | 0.9614 | 0.9737 | 0.5626 | 0.7132 | 0.9056 |

### 🏆 Best Model: Neural Network
- Highest Accuracy (97.14%), F1-Score (0.8058), and AUC-ROC (0.9764)
- Random Forest was a close second — nearly identical accuracy with simpler interpretability

---

## 🔍 Key Insights

**Why was Recall the hardest metric to optimize?**
The dataset is highly imbalanced — diabetic cases are a minority class. Models naturally bias toward predicting the majority (non-diabetic) class, which inflates accuracy but hurts recall. In a healthcare context, **low recall is dangerous** — it means the model misses actual diabetic patients (false negatives), which is the costlier error.

**What this means in practice:**
- The Neural Network's recall of 0.695 means it correctly identified ~70% of all diabetic patients
- For clinical deployment, further tuning (class weighting, SMOTE oversampling) would be needed to push recall higher
- Random Forest offers a practical trade-off: nearly identical accuracy with more explainability — important in healthcare settings where doctors need to understand *why* a prediction was made

**Most predictive features:** HbA1c level and blood glucose level were the strongest predictors of diabetes risk, consistent with clinical evidence.

---

## 💡 Business / Clinical Implication

A model like this could assist healthcare providers in **flagging high-risk patients during routine checkups** — enabling earlier intervention before diabetes progresses. Rather than replacing clinical judgment, it serves as a decision-support tool to prioritize who needs further testing, potentially reducing diagnostic delays and long-term treatment costs.

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/AnnBMariyam/Diabetes-Risk-Prediction-ML.git
cd Diabetes-Risk-Prediction-ML

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter

# 3. Launch Jupyter Notebook
jupyter notebook notebooks/
```

---

## 👩‍💻 Author

**Ann B Mariyam**
MS Data Analytics — University of Illinois Springfield
[LinkedIn](https://www.linkedin.com/in/ann-b-mariyam-a238a7275/) | [GitHub](https://github.com/AnnBMariyam) | annbijumariyam02@gmail.com
