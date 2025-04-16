# 🧠 Employee Engagement Modeling with AutoGluon

This project explores two machine learning workflows using **AutoGluon**:

1. **Regression Modeling** — Predicting Overtime Hours
2. **Classification Modeling** — Predicting Employee Engagement Level (High vs Medium)

> 📂 **Data Source**: [Company Employees Dataset from Kaggle](https://www.kaggle.com/datasets/abdallahwagih/company-employees/data)

---

## 📘 Notebooks Overview

### 1. 🧮 `EmployeeEngagement_AutoGluon_Regression.ipynb`

- **Target Variable**: `OvertimeHours`
- **Task**: Regression
- **Goal**: Predict how many overtime hours an employee is likely to work.
- **Best Model**: `WeightedEnsemble_L2`
- **Validation RMSE**: `28.84`

📌 *Why Regression?*  
OvertimeHours is a continuous numerical variable, making regression the appropriate method for prediction.

📊 **Top Features**:
- `JobRate`
- `SickLeaves`
- `UnpaidLeaves`

---

### 2. 🧩 `EmployeeEngagement_AutoGluon_Classification.ipynb`

- **Target Variable**: `EngagementLevel` (High, Medium)
- **Task**: Binary Classification
- **Goal**: Predict whether an employee is **Highly Engaged** or **Moderately Engaged**.
- **Best Model**: `WeightedEnsemble_L2`
- **Validation Accuracy**: `99.52%`

📌 *Why Classification?*  
Engagement level is categorical (High, Medium, Low). The "Low" class was merged with "Medium" due to class imbalance, turning it into a binary classification task.

📊 **Classification Metrics**:
| Metric        | Score     |
|---------------|-----------|
| Accuracy      | 99.52%    |
| F1-Score (High)| 0.99     |
| ROC AUC       | 0.99      |

---

## 📊 Final Model Comparison Table

| Notebook Type     | Best Model           | Metric Used      | Score     |
|-------------------|----------------------|------------------|-----------|
| Regression        | WeightedEnsemble_L2  | RMSE             | 28.84     |
| Classification    | WeightedEnsemble_L2  | Accuracy         | 99.52%    |

---

## 🔍 Key Insights

- Regression and classification solve **very different problems**.
  - Regression predicts **how much** (e.g., overtime hours).
  - Classification predicts **what category** (e.g., High vs Medium engagement).
- The best models in both tasks were **ensemble models**, combining strengths from multiple learners like `NeuralNetFastAI`, `KNN`, and `LightGBM`.

---

## 📁 Folder Structure

```
📦 EmployeeEngagement
├── 📁 AutogluonModels
├── 📓 EmployeeEngagement_AutoGluon_Regression.ipynb
├── 📓 EmployeeEngagement_AutoGluon_Classification.ipynb
└── 📄 README.md
```

---

## ✅ How to Reuse Trained Models

To load any saved model:

```python
from autogluon.tabular import TabularPredictor

predictor = TabularPredictor.load("AutogluonModels/ag-20250416_031523")  # Replace with your folder
```

---

## 💬 Contact

For questions, suggestions, or collaborations, feel free to connect!
