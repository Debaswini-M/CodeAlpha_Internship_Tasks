
# Task 2: Credit Scoring Model 

## Objective

Build a credit scoring model to **predict an individual’s creditworthiness** using past financial data. The focus is on applying classification models and evaluating them using appropriate performance metrics.

---

##  Problem Statement

Financial institutions need reliable models to assess the credit risk of individuals. This project uses customer financial history to predict whether a person will **default on their credit card payment next month**.

---

## 📊 Dataset

- **Source**: `Credit_Card_default.csv`
- **Features**:
  - Demographic: Age, Sex, Education, Marriage
  - Financial: Credit Limit, Payment History, Bill Amounts, Previous Payments
- **Target**: `DEFAULT` (1 = default, 0 = not default)

---

## 🛠️ Tools & Technologies

- **Language**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Models**:
  - Logistic Regression
  - Decision Tree Classifier
  - Random Forest Classifier

---

## Workflow

1. **Data Cleaning & Preprocessing**
   - Handled unknown categories in `MARRIAGE` and `EDUCATION`.
   - Normalized numerical features using `StandardScaler`.

2. **Model Training**
   - Trained Logistic Regression, Decision Tree, and Random Forest models.
   - Used `class_weight='balanced'` to handle class imbalance.

3. **Evaluation Metrics**
   - Accuracy
   - F1 Score
   - ROC-AUC
   - Confusion Matrix
   - Classification Report

4. **Visualization**
   - ROC Curves
   - Metric Comparison (Bar & Scatter Plots)

---

## 📈 Results

| Model              | Accuracy | F1 Score | ROC AUC  |
|--------------------|----------|----------|----------|
| Logistic Regression|   0.6938 |  0.4794  |  0.7277  | 
| Decision Tree      |   0.7258 |  0.3967  |  0.6136  |
| Random Forest      |  0.8138  |  0.4417  |  0.7632  |

> 📌 Note: Random Forest usually gives better generalization, but Logistic Regression often performs competitively on structured datasets with proper scaling.

---

## 📊 Plots

- ROC Curve for each model
- Bar and scatter plots comparing model performance

---

## Author
**Debaswini**

---

