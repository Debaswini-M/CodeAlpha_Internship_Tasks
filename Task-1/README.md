#  Task 1: Disease Prediction from Medical Data



---

## 📌 Objective
The goal of this project is to **predict the presence of heart disease** using a medical dataset by applying machine learning classification models.

---

## 📊 Dataset Description

- **Source:** UCI Machine Learning Repository – Heart Disease Dataset
- **Target Variable:** Presence of heart disease (binary/multiclass)
- **Features Used:**
  - Age, Sex, Chest Pain Type (cp), Resting Blood Pressure (trestbps)
  - Cholesterol, Fasting Blood Sugar (fbs), Rest ECG (restecg)
  - Max Heart Rate Achieved (thalch), Exercise Induced Angina (exang)
  - ST depression (oldpeak), Slope, Number of Vessels (ca)
  - Thalassemia (thal)

---

## ⚙️ Tools & Libraries

- **Programming Language:** Python
- **Libraries Used:**
  - `pandas`, `numpy` – data handling
  - `matplotlib` – data visualization
  - `scikit-learn` – ML modeling and evaluation
  - `xgboost` – advanced boosting model

---

## 🧠 ML Models Used

| Model                  | Notes                                     |
|-----------------------|-------------------------------------------|
| Logistic Regression    | Baseline classifier with balanced class weights |
| Support Vector Machine | Non-linear classifier with probability outputs |
| Random Forest          | Ensemble decision trees with balanced weights |
| XGBoost                | Gradient boosting classifier with max depth control |

---

## 🧼 Preprocessing Steps

1. **Data Cleaning**
   - Removed irrelevant columns: `id`, `dataset`
   - Replaced zero values with `NaN` in medically impossible fields
2. **Imputation**
   - Used **median** for continuous features (`chol`, `trestbps`, etc.)
   - Used **mode** for binary/categorical features (`fbs`, `exang`)
3. **Encoding**
   - Applied **Ordinal Encoding** to binary columns (`sex`, `fbs`, `exang`)
   - (Optional) One-Hot Encoding available for future extension
4. **Feature Scaling**
   - StandardScaler applied to all numerical features
5. **Train-Test Split**
   - 80.1/19.9 stratified split to preserve target distribution

---

## 📈 Evaluation Metrics

Each model was evaluated using:

- **Accuracy**
- **ROC AUC Score (macro, one-vs-rest)**
- **Classification Report** (Precision, Recall, F1-score)

---

## 📊 Model Comparison (Sample Result)

| Model               | Accuracy | ROC AUC |
|--------------------|----------|---------|
| Logistic Regression | 0.80     | 0.93    |
| Random Forest       | 1.00     | 1.00    |
| SVM                 | 0.90     | 0.79    |
| XGBoost             | 1.00     | 1.00    |

>  Note: Actual values may vary per execution due to random state and data splits.

---

## 📉 Visualization

Bar plot comparison between **Accuracy** and **ROC AUC** for all models was included using `matplotlib`, helping visualize performance across classifiers.

---

## Author
**Debaswini**

---

