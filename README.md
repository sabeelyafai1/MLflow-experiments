# 🍷 MLflow Experiment Tracking with DagsHub  
A complete end-to-end Machine Learning lifecycle project using **MLflow**, **DagsHub**, and **ElasticNet regression** on the Wine Quality dataset.

This project demonstrates:

- ML experiment tracking  
- Model metrics logging  
- Model registry & versioning  
- Remote tracking using **DagsHub**  
- Reproducible ML pipeline with parameters (alpha, l1_ratio)  
- Artifact logging  

---

## 📌 Project Overview

This project trains an **ElasticNet regression model** on the red wine quality dataset.  
It tracks all experiments using **MLflow**, and logs metrics/artifacts to a **remote DagsHub MLflow server**.

### 🔥 Key Features
- Tracks *parameters, metrics, models, artifacts*
- Remote MLflow tracking using DagsHub
- ElasticNet Regression Model
- Model versioning & experiment comparison
- Full project reproducibility

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3.10** | Programming |
| **MLflow** | Experiment Tracking |
| **DagsHub** | Remote MLflow + Model Registry |
| **scikit-learn** | Machine Learning |
| **pandas / numpy** | Data processing |

---

## 📁 Project Structure





## ML FLow experiements

MLFLOW_TRACKING_URI=https://dagshub.com/sabeelyafai1/MLflow-experiments.mlflow \
MLFLOW_TRACKING_USERNAME=sabeelyafai1 \
python script.py


import dagshub
dagshub.init(repo_owner='sabeelyafai1', repo_name='MLflow-experiments', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

