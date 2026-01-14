# Diabetes 30-Day Readmission Prediction  
### TabTransformer + Federated Learning (FedAvg) + Explainable AI (SHAP & LIME)

## 📌 Project Overview
This project focuses on predicting **30-day hospital readmission** in diabetic patients using the **Diabetes 130-US Hospitals dataset (1999–2008)**.  
The core objective is to build a **high-performance, privacy-preserving, and interpretable AI system** suitable for real-world healthcare environments.

The system integrates:
- **TabTransformer** for advanced tabular data modeling  
- **Federated Learning (FedAvg)** to simulate multi-hospital collaboration without sharing raw patient data  
- **Explainable AI (SHAP & LIME)** to ensure clinical interpretability and trust  

---

## 🎯 Problem Statement
Hospital readmissions within 30 days are costly and clinically significant.  
Traditional ML models struggle with:
- High-cardinality categorical features
- Complex feature interactions
- Privacy constraints across hospitals
- Lack of interpretability

This project addresses all four challenges in a single end-to-end pipeline.

---

## 📊 Dataset
- **Name:** Diabetes 130-US Hospitals Dataset  
- **Records:** 101,766 patient encounters  
- **Hospitals:** 130 US hospitals  
- **Features:** 50 clinical attributes  
- **Target:** 30-day readmission (`<30` vs others)

---

## 🧠 Methodology
### 1. Data Preprocessing
- Missing value handling
- Label encoding for categorical features
- Feature scaling for numerical attributes
- Class imbalance handled using **SMOTE**

### 2. Baseline Model
- Centralized **TabTransformer**
- Attention-based embeddings for categorical features
- Binary classification head

### 3. Federated Learning
- 5 simulated hospital clients
- Local training on each client
- Global aggregation using **Federated Averaging (FedAvg)**
- No raw data sharing between clients

### 4. Explainable AI
- **SHAP:** Global feature importance
- **LIME:** Patient-level prediction explanations
---
## 🔄Workflow Pipeline
```text
Data Collection
      ↓
Preprocessing & Encoding
      ↓
SMOTE (Class Balancing)
      ↓
Centralized TabTransformer Training
      ↓
Federated Learning (FedAvg)
      ↓
Global Model Evaluation
      ↓
Explainability (SHAP + LIME)
```
---
## 📈 Model Performance Summary

| Metric    | Baseline | Federated |
|----------|----------|-----------|
| Accuracy | 0.8582   | 0.8934    |
| F1-Score | 0.1398   | 0.2419    |
| Recall   | 0.1033   | 0.1523    |
| ROC-AUC  | 0.6482   | 0.7678    |

➡️ Federated learning significantly improves **recall, F1-score, and AUC**, which are critical for clinical risk prediction.

---

## 🗂️ Project Structure
```text
📦 Diabetes-Readmission-Prediction
│
├── code/
│   └── code.ipynb                # Complete implementation (training, FL, XAI)
│
├── dataset/
│   ├── diabetic.csv              # Diabetes 130-US Hospitals dataset
│   └── ids_mapping.csv           # Feature ID mapping reference
│
├── evaluation/
│   └── (model evaluation results, plots, metrics)
│
├── report.docx                   # Final project report (IEEE format)
├── presentation.pptx             # Project presentation slides
└── README.md                     # Project documentation
```

---

## 🛠️ Technologies Used
- Python  
- PyTorch  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  
- SHAP  
- LIME  

---

## 🏥 Clinical Relevance
- Early identification of high-risk patients  
- Privacy-preserving multi-hospital collaboration  
- Transparent and explainable predictions  
- Supports clinical decision-making, not blind automation  

---

## 📌 Key Contributions
- First integration of **TabTransformer + Federated Learning + XAI** on this dataset  
- Demonstrates real-world feasibility of privacy-aware healthcare AI  
- Provides both global and local model interpretability  

---

## 📎 Note
This project is intended for **academic, research, and experimental purposes** and serves as a foundation for future real-world healthcare AI deployments.

---
