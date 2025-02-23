# **Hiring Bias Analysis using Machine Learning (PS2)**

## **Project Overview**
This repository contains a Python script, `code.py`, that builds upon **Problem Set 1 (PS1)** by introducing **machine learning fairness auditing, interpretability, and predictive modeling**. The primary focus is on analyzing **hiring discrimination** using machine learning models.

### **Key Features in PS2**
- **Hyperparameter Tuning**: Using `GridSearchCV` for **Logistic Regression, Decision Trees, Random Forest, and XGBoost**.
- **Fairness Metrics**: Evaluation of **Demographic Parity, Disparate Impact Ratio, and Equalized Odds**.
- **Model Interpretability**: SHAP explanations applied to **Random Forest (TreeExplainer)** and **Neural Networks (KernelExplainer)**.
- **Neural Networks**: Implementation of a **feedforward network with dropout**.
- **Regression Discontinuity (Placeholder)**: A plan for causal inference to measure **policy-based hiring effects**.

---

## **1. `code/` Folder**
- **`code.py`**  
  - **Loads and preprocesses data** from an Excel file.  
  - **Trains multiple models** with hyperparameter tuning (Logistic Regression, Decision Tree, Random Forest, XGBoost).  
  - **Evaluates fairness** using Demographic Parity, Disparate Impact Ratio, Equalized Odds.  
  - **Uses SHAP for interpretability** (TreeExplainer for Random Forest).  
  - **Trains a Neural Network** with dropout layers.  

---

# System Requirements
- **Python 3.9** or higher  
- **Operating System**: Windows, macOS, or Linux  

---

# Dependencies
Install dependencies using the **`requirements.txt`** file or manually install key libraries:

```bash
pip install shap tensorflow scikit-learn pandas numpy matplotlib seaborn xgboost

