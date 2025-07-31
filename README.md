# Credit Risk Prediction

## 🧠 Task Objective

The goal of this project is to develop a classification model that can predict whether a loan applicant is likely to **default on a loan**. This type of prediction helps financial institutions make data-driven decisions when approving or rejecting loan applications.

---

## 🔍 Approach

### 1. **Data Cleaning**
- Loaded the Loan Prediction dataset (CSV)
- Identified and handled **missing values** appropriately
  - Replaced nulls in numerical features with median values
  - Filled missing categorical values with mode
- Removed extra whitespaces in column names for consistency

### 2. **Feature Engineering**
- Used **Label Encoding** for binary categorical columns:  
  - `gender`, `married`, `education`, `self_employed`, `loan_status`
- Applied **One-Hot Encoding** to `dependents` and `property_area`

### 3. **Model Training**
- Selected **Logistic Regression** and **Decision Tree Classifier** for initial models
- Split data into training and testing sets (80/20 split)
- Trained models using Scikit-learn

### 4. **Model Evaluation**
- Used:
  - **Accuracy Score**
  - **Confusion Matrix**
  - **Classification Report** (Precision, Recall, F1-score)

---

## 📊 Results and Insights

### 🔹 Model Performance
- **Accuracy (Logistic Regression):** ~77%
- **Accuracy (Decision Tree):** ~80% (may vary depending on the split and depth)
- Confusion matrix showed decent balance between predicting defaulters and non-defaulters

### 🔹 Key Insights
- Applicants with **lower income**, **shorter loan terms**, and **low CIBIL scores** are more likely to default
- **Self-employed** individuals had slightly higher default rates
- **Education** and **property area** had less predictive power compared to financial metrics

---

## 🚀 Next Steps (Optional Enhancements)

- Test more complex models like Random Forest, XGBoost
- Perform cross-validation for more reliable performance estimates
- Use grid search or randomized search for hyperparameter tuning

---

## 📁 Project Structure

```text
credit-risk-prediction/
│
├── loan_data.csv
├── credit_risk_model.py
├── README.md
└── requirements.txt
