# 🧠 Employee Engagement Classification Project

This project aims to classify employee engagement levels using supervised machine learning techniques. It includes two approaches:

- ✅ A **PyCaret-based notebook** that handles automatic model comparison, SMOTE balancing, and detailed model evaluation.
- ✅ A **Scikit-learn notebook** that builds a manual pipeline inspired by the best model found in PyCaret (LightGBM), using the Random Forest Classifier.

---

## 📂 Project Contents

- [`EmployeeEngagement_PyCaret.ipynb`](https://github.com/w0435723/BIA_Repository/blob/main/Applied%20Data%20Science/EmployeeEngagement_PyCaret.ipynb)  
  → Automated classification and model tuning using PyCaret

- [`EmployeeEngagement_ScikitLearn.ipynb`](https://github.com/w0435723/BIA_Repository/blob/main/Applied%20Data%20Science/EmployeeEngagement_ScikitLearn.ipynb)  
  → Manual implementation in Scikit-learn based on PyCaret results

- 🔗 [View Employee_Profile_Report.html](https://w0435723.github.io/BIA_Repository/Employee_Profile_Report.html)    
  → Full data profile using [YData Profiling](https://github.com/ydataai/ydata-profiling), published via GitHub Pages  
  
---

## 📊 Data Source

- Dataset: **Company Employees**  
- 📥 Source: [Kaggle Dataset by Abdallah Wagih](https://www.kaggle.com/datasets/abdallahwagih/company-employees/data)

---

## 🧾 Final Model Comparison: Scikit-learn vs. PyCaret

| Metric        | Scikit-learn (Random Forest) | PyCaret (LightGBM)      |
|---------------|------------------------------|--------------------------|
| Accuracy      | 0.9855                       | 0.9903                   |
| Recall        | 0.9903                       | 0.9903                   |
| Precision     | 0.9903                       | 0.9903                   |
| F1 Score      | 0.9903                       | 0.9903                   |
| AUC           | 1.00                         | 0.9935 (avg)             |
| Confusion Matrix | Slightly less accurate on 'Medium' | Stronger balance |

---

## 🧠 Final Summary

Both the PyCaret and Scikit-learn models demonstrated exceptional classification performance for predicting employee engagement levels. The PyCaret LightGBM model slightly edged out the Random Forest model in terms of accuracy and class balance, as seen in the confusion matrix. However, the Scikit-learn model still achieved nearly perfect results, including an AUC of 1.00 and F1-score of 0.99. Overall, both models are viable for deployment, and the slight differences could be attributed to internal optimizations of the respective algorithms.

---


 
