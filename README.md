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

