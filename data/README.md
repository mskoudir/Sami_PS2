# **Raw Data: Hiring Discrimination Dataset**

## **Overview**
This folder contains the **original dataset** used for the hiring discrimination analysis. The dataset is stored in an **Excel file** (`.xlsx`) format and includes various demographic and hiring-related variables.

## **File Description**
### **1. `220831_STATE_OF_HIRING_DISCRIMINATION.xlsx`**
- This dataset contains **callback rates** for different demographic groups based on a hiring study.
- The data originates from an **audit study on employment discrimination**, examining disparities in callback rates between majority and minority applicants.

---

## **Dataset Structure**
The dataset consists of the following key columns:

| Column Name               | Description |
|---------------------------|-------------|
| **ground**                | Basis of discrimination (e.g., race, gender, nationality). |
| **study**                 | The specific study from which the data originates. |
| **treatment_group_high**   | The group subject to potential discrimination. |
| **control_group**          | The reference (majority) group for comparison. |
| **callback_maj**           | Callback rate for the majority group. |
| **callback_min**           | Callback rate for the minority group. |
| **effect_category**        | Categorized effect of discrimination (e.g., significant bias, no bias). |

---

## **Preprocessing Steps**
Before using this dataset for analysis, the following **preprocessing steps** are applied in `ps2.py`:

1. **Load the Excel file**:
   ```python
   import pandas as pd
   xls = pd.ExcelFile("data/raw_data/220831_STATE_OF_HIRING_DISCRIMINATION.xlsx")
   df = xls.parse('register')

2. **Drop missing values**:
  ```python
  df = df.dropna()
  ```
3. **Encode categorical variables**:   
  ```python
  df["effect_category_encoded"] = df["effect_category"].astype("category").cat.codes
  df["treatment_group_encoded"] = df["treatment_group_high"].astype("category").cat.codes
  df["control_group_encoded"] = df["control_group"].astype("category").cat.codes
  ```
4. **Compute callback rate difference**:
  ```python
df["callback_diff"] = df["callback_maj"] - df["callback_min"]
  ```
5. **Save the cleaned dataset**:
```python
df.to_csv("data/processed_data/applicants_cleaned.csv", index=False)
This version properly formats your code snippets within Markdown. Let me know if you need any adjustments! 🚀
  ```
