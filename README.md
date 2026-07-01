# Loan Approval Prediction using Machine Learning

## Project Overview

This project predicts whether a loan application will be approved or rejected using Machine Learning techniques. The workflow includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and performance evaluation.

The goal is to identify the most effective model for loan approval prediction and analyze the impact of feature engineering on model performance.

---

## Dataset

The dataset contains information about loan applicants, including:

* Income
* Education Level
* Employment Status
* Loan Amount
* Loan Term
* Credit Score
* Residential Assets
* Commercial Assets
* Luxury Assets
* Bank Assets
* Loan Status (Target Variable)

Target Variable:

* Approved → 1
* Rejected → 0

---

## Project Workflow

### 1. Data Loading

* Imported dataset using Pandas.
* Performed initial inspection of rows, columns, and data types.

### 2. Exploratory Data Analysis (EDA)

* Dataset overview
* Missing value analysis
* Loan approval distribution
* Correlation analysis
* Feature understanding

### 3. Data Preprocessing

* Converted categorical variables into numerical values.
* Encoded:

  * Education
  * Self Employment Status
  * Loan Status

### 4. Feature Engineering

Created a new feature:

```python
total_assets = residential_assets_value +commercial_assets_value +luxury_assets_value +bank_asset_value
```

This feature represents the total wealth/assets owned by an applicant.

### 5. Train-Test Split

* Training Data: 80%
* Testing Data: 20%

### 6. Feature Scaling

Applied StandardScaler for Logistic Regression.

### 7. Machine Learning Models

The following models were trained and evaluated:

* Logistic Regression
* Logistic Regression (Scaled Features)
* Decision Tree Classifier
* Random Forest Classifier

### 8. Model Evaluation

Performance measured using:

* Accuracy Score
* Classification Report
* Confusion Matrix
* Model Comparison Table

---

## Results

A comparison was performed between:

* Original Features
* Engineered Features (including Total Assets)

The impact of feature engineering was analyzed across all models.

| Model                        | Evaluation Metric |
| ---------------------------- | ----------------- |
| Logistic Regression          | 0.818501          |
| Logistic Regression (Scaled) | 0.908665          |
| Decision Tree                | 0.981265          |
| Random Forest                | 0.983607          |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Project Structure

```text
Loan_Approval_Prediction/
│
├── loan_approval.ipynb
├── loan_approval_dataset.csv
├── README.md
├── requirements.txt
```

---


