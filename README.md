# 📉 Telecom Customer Churn Prediction & MLOps Pipeline

Pipeline end-to-end de Machine Learning enfocado en la detección temprana de cancelación de clientes (*Churn*) en telecomunicaciones, priorizando la optimización del impacto de negocio y el seguimiento de experimentos con MLflow.

## 🎯 Resultados Clave & Criterio de Selección

Se evaluó el rendimiento de los modelos frente al desbalance de clases (~26.5% de Churn). A pesar de que **Random Forest** obtuvo un mayor *Accuracy* general (79%), se seleccionó **Regresión Logística con balanceo de pesos** por maximizar la captura real de clientes en riesgo (**Recall** y **ROC-AUC**).

| Modelo | ROC-AUC | Recall (Churn) | Precision (Churn) | Impacto de Negocio |
| :--- | :---: | :---: | :---: | :--- |
| **Logistic Regression (Balanced)** | **0.8420** | **79%** | 51% | **Identifica a 295 de 374 clientes en riesgo** |
| Random Forest (Balanced) | 0.8209 | 49% | 63% | Deja escapar al 51% de los clientes que cancelan |

## 💡 Drivers Principales de Cancelación (SHAP Values)

1. **Antigüedad (`tenure`):** La ventana crítica de abandono se concentra en los primeros 12 meses de contrato.
2. **Modalidad de Contratación:** Los acuerdos a 1 y 2 años actúan como el principal factor de retención.
3. **Servicios de Valor Agregado:** Clientes con *Online Security* y *Tech Support* presentan significativamente menor tasa de baja.

## 🛠️ Stack Tecnológico

* **MLOps & Tracking:** MLflow
* **Modelado & Métricas:** Scikit-Learn
* **Explicabilidad:** SHAP (SHapley Additive exPlanations)
* **Procesamiento & Análisis:** Python, Pandas, Seaborn
