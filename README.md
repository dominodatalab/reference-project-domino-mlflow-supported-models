# Domino MLflow Models

This project contains examples of various MLflow supported models such as XGBoost, Sklearn, PyTorch, TensorFlow, and custom Pyfunc models. These include code snippets to register the model to MLflow, register training sets to Domino, and configuring prediction data capture.

The assets included in the project are:

* **domino-mlflow-model-sklearn-imm.ipynb** - a notebook that trains a sklearn linear regression model on the California Housing Prices dataset and does the following:

    * Registers the training data used as a training set
    * Creates a pyfunc model wrapper class that configures a model with prediction data capture to capture the numerical prediction responses
    * Register the linear regression model in MLflow

**domino-mlflow-model-xgboost-imm.ipynb** - a notebook that trains a xgboost classifier model on the Iris dataset and does the following:

    * Registers the training data used as a training set
    * Creates a pyfunc model wrapper class that configures a model with prediction data capture to capture the categorical prediction responses
    * Register the classifier model in MLflow
    
* **domino-mlflow-model.ipynb** - a notebook that has examples of how to register xgboost, sklearn, tensorflow, and pytorch models to mlflow.


## Model API

You can test the Model API using the following observation:

### Housing Prices Regression (sklearn)

{
  "data": [
    [8.3252, 41.0, 6.984127, 1.023810, 322.0, 2.555556, 37.88, -122.23],
    [8.3014, 21.0, 6.238137, 0.971880, 2401.0, 2.109842, 37.86, -122.22]
  ]
}

### Iris Classification (xgboost)

{
  "data": [
    [5.1, 3.5, 1.4, 0.2],
    [4.9, 3.0, 1.4, 0.2]
  ]
}