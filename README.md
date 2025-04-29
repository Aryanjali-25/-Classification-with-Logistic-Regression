# -Classification-with-Logistic-Regression
# Credit Card Fraud Detection using Logistic Regression

This project demonstrates a binary classification task using Logistic Regression on a synthetic credit card fraud dataset. The goal is to classify whether a transaction is fraudulent (1) or legitimate (0) based on various features.

---

## Dataset

The dataset is a synthetic version of credit card transaction data.  
Target column:label  
- 1 = Fraud  
- 0 = Not fraud

We removed non-useful columns such as:
- user_id, card_number, expiry_date, and cvv

Remaining features include:
- Risk scores, browser types, device types, and time-of-day indicators.

---

##  Steps Performed

### 1. Load and Clean the Data
- Load the CSV file into a DataFrame using pandas
- Drop irrelevant features
- Separate features (X) and target (y)

### 2. Split into Train and Test Sets
- Use train_test_split() with 80% training and 20% testing
- Stratified sampling ensures both sets have similar fraud proportions

### 3. Standardize Features
- Apply `StandardScaler` to normalize the numerical features
- This helps the Logistic Regression model converge faster and perform better

### 4. Train the Logistic Regression Model
- Fit the model using LogisticRegression() from scikit-learn
- Train on scaled features

### 5. Model Evaluation
- Predict classes and probabilities on test data
- Evaluate using:
  - Confusion Matrix
  - Classification Report(precision, recall, F1-score)
  - ROC Curve and AUC Score

### 6. Sigmoid Function
- Visualize how the Logistic Regression model converts inputs to probabilities using the sigmoid function

### 7. Tune the Classification Threshold
- Default threshold is 0.5
- Try custom thresholds like 0.3 to improve recall (important for fraud detection)
- Evaluate how the confusion matrix and metrics change with different thresholds

---

## Key Metrics

We focused on:
- Recall: How many frauds we catch
- Precision: How many of our fraud predictions are actually correct
- ROC-AUC: Overall classification ability across all thresholds

---
