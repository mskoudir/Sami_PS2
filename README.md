# **Advancing the Analysis of Racial Bias in Hiring Using Machine Learning**

## **Project Overview**
This repository investigates racial bias in hiring decisions through **machine learning** techniques, integrating fairness metrics and causal inference to create an **equitable and transparent** model pipeline. 

The research progresses through:
- **Problem Set 1 (PS1):** Initial exploration of bias using baseline models.
- **Problem Set 2 (PS2):** Advanced methods including hyperparameter tuning, fairness metrics, interpretability via SHAP, and causal inference using **Regression Discontinuity (RD)**.

---

## **Repository Structure**


### **1. `data/` Folder**
- **raw_data/**: Contains original or simulated data files.
- **processed_data/**: Stores any cleaned/encoded data ready for analysis.
- **README.md**: Details the data source, variable definitions, and any preprocessing steps.

### **2. `code/` Folder**
- **`ps2_main_analysis.ipynb`**:  
  - Hyperparameter tuning for Logistic Regression, Decision Tree, Random Forest, XGBoost, or a Neural Network.
  - Fairness metrics (Demographic Parity, Disparate Impact, Equalized Odds).
  - SHAP interpretability for model transparency.
- **`rd_analysis.ipynb`**:  
  - Placeholder for Regression Discontinuity design (e.g., specifying a policy threshold of 80).
  - Local linear regressions or polynomial methods to estimate the causal effect.
  - Placebo cutoffs or bandwidth sensitivity checks.
- **`README.md`**:  
  - Explains each notebook’s purpose.
  - Lists dependencies, usage instructions, and expected outputs.

---

## **System Requirements**

- **Python 3.9** or higher recommended
- **Operating System**: Windows, macOS, or Linux

---

## **Dependencies**

You can find most dependencies in `requirements.txt` or `code/README.md`, but the primary libraries include:

- **NumPy** and **pandas** for data manipulation
- **scikit-learn** for machine learning algorithms
- **seaborn** and **matplotlib** for data visualization
- **SHAP** for interpretability
- **statsmodels** for advanced statistical tests (especially in RD analysis)
- **TensorFlow** (or PyTorch) if using Neural Networks
- **xgboost** (optional) for gradient boosting

---

# Usage Instructions

## 1. Data Preparation
- Place the original Excel/CSV files in `data/raw_data/`.

## 2. Run the Main Analysis
- Open `code.py`.
- Execute each cell in order to reproduce the results:
  - **Data loading**
  - **Exploratory Data Analysis (EDA)**
  - **Hyperparameter tuning and model training**
  - **Fairness metric calculations**
  - **SHAP interpretability**

## 3. Causal Inference
- Open `code.py` (placeholder).
- Follow instructions to:
  - Simulate or load data with a threshold (e.g., skill score ≥ 80).
  - Perform local linear regression or other RD-based analyses.

## 4. View Results
Check the output from each notebook:
- **Performance metrics**
- **Fairness statistics**
- **SHAP plots**, etc.

---

# Expected Outputs

## 📊 Plots & Figures
- **EDA bar charts**
- **Classification reports**
- **SHAP summary plots**
- **Fairness bar charts**

## 📈 Metrics
- **Accuracy, Precision, Recall, F1-score**
- **Demographic Parity, Disparate Impact Ratio, partial Equalized Odds**

## 🎯 RD (if implemented)
- **Estimate of the policy threshold’s causal effect**
- **Placebo/bandwidth sensitivity checks**

---

# Contributors
- **Mohamed Sami Koudir** – Primary author, data analysis, code development, project structure.

---

# License
If you plan to open-source your project, add a license (e.g., MIT, Apache 2.0) here.*

---

# Citation / References
If you use or build upon this repository, please cite:

- Bertrand, M., & Mullainathan, S. (2004). *Are Emily and Greg more employable than Lakisha and Jamal?* American Economic Review, 94(4), 991–1013.
- Hardt, M., Price, E., & Srebro, N. (2016). *Equality of opportunity in supervised learning.* NeurIPS.
- Lundberg, S. M., & Lee, S.-I. (2017). *A unified approach to interpreting model predictions.* Advances in NeurIPS.
- Dwork, C., Hardt, M., Pitassi, T., Reingold, O., & Zemel, R. (2012). *Fairness through awareness.* ITCS.
- Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). *On the dangers of stochastic parrots.* FAccT.
