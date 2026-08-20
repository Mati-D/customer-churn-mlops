<p align="center">
  <img src="https://images.unsplash.com/photo-1520869562399-e772f042f422?q=80&w=1920&auto=format&fit=crop" width="100%" style="border-radius: 8px;" alt="Telecom Banner">
</p>

# 📉 Telecom Customer Churn Prediction & MLOps Pipeline

End-to-end Machine Learning pipeline focused on the early detection of customer cancellation (Churn) in telecommunications, prioritizing the optimization of business impact and experiment tracking with MLflow.

## 🎯 Key Results & Selection Criteria

Model performance was evaluated against class imbalance (~26.5% Churn). Although Random Forest achieved a higher overall Accuracy (79%), **Logistic Regression with class weight balancing** was selected for maximizing the actual capture of at-risk customers (Recall and ROC-AUC).

| Model | ROC-AUC | Recall (Churn) | Precision (Churn) | Business Impact |
| :--- | :---: | :---: | :---: | :--- |
| **Logistic Regression (Balanced)** | 0.8420 | 79% | 51% | Identifies 295 out of 374 at-risk customers |
| **Random Forest (Balanced)** | 0.8209 | 49% | 63% | Misses 51% of churning customers |

## 💡 Main Churn Drivers (SHAP Values)

* **Tenure:** The critical drop-off window is concentrated in the first 12 months of the contract.
* **Contract Type:** 1-year and 2-year contracts act as the main retention factor.
* **Value-Added Services:** Customers with *Online Security* and *Tech Support* show a significantly lower churn rate.

## 🛠️ Tech Stack

* **MLOps & Tracking:** MLflow
* **Modeling & Metrics:** Scikit-Learn
* **Explainability:** SHAP (SHapley Additive exPlanations)
* **Processing & Analysis:** Python, Pandas, Seaborn
