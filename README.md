# Credit Card Fraud Detection using Machine Learning

## Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. Fraud detection is a critical task for financial institutions as fraudulent transactions can lead to significant financial losses. The goal of this project is to build and compare machine learning models that can accurately identify fraudulent transactions.

The dataset used in this project contains real credit card transactions made by European cardholders in September 2013. It is highly imbalanced, with only a small percentage of transactions being fraudulent.

---

## Dataset Information

* Total Transactions: **284,807**
* Normal Transactions: **284,315**
* Fraudulent Transactions: **492**
* Fraud Percentage: **0.17%**

### Dataset Features

The dataset contains **31 columns**:

| Feature  | Description                                           |
| -------- | ----------------------------------------------------- |
| Time     | Time elapsed since the first transaction              |
| V1 – V28 | Features transformed using PCA for privacy protection |
| Amount   | Transaction amount                                    |
| Class    | Target variable (0 = Normal, 1 = Fraud)               |

Due to privacy reasons, the original transaction features were transformed using **Principal Component Analysis (PCA)**.

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

* Fraud vs Normal transaction distribution
* Transaction amount distribution
* Fraud vs transaction amount comparison
* Correlation heatmap of features

Key insight:
The dataset is extremely **imbalanced**, which makes fraud detection a challenging machine learning problem.

---

## Data Preprocessing

The following preprocessing steps were applied:

1. Checking for missing values
2. Feature scaling using **StandardScaler**
3. Splitting data into **training and testing sets**
4. Handling class imbalance using **class weights**

---

## Machine Learning Models

Two models were trained and evaluated:

### 1. Logistic Regression

A simple and interpretable linear model used for binary classification.

### 2. Random Forest

An ensemble learning method that builds multiple decision trees and combines their predictions for improved performance.

---

## Model Evaluation Metrics

Models were evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC Curve and AUC Score

These metrics are important for imbalanced datasets where accuracy alone can be misleading.

---

## Model Performance Comparison

| Model               | Accuracy | Precision | Recall   | F1 Score |
| ------------------- | -------- | --------- | -------- | -------- |
| Logistic Regression | High     | Moderate  | Moderate | Moderate |
| Random Forest       | Higher   | Higher    | Higher   | Higher   |

Random Forest performed better overall, especially in **recall and F1-score**, which are critical for fraud detection.

---

## Results and Insights

* The dataset is highly imbalanced, with only **0.17% fraud transactions**.
* Random Forest captured complex patterns better than Logistic Regression.
* Evaluation metrics like **Recall and F1-score** are more important than accuracy in fraud detection problems.

---

## Tools and Technologies

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## Project Structure

```
credit-card-fraud-detection/
│
├── creditcard_fraud_detection.ipynb
├── README.md
```

---

## How to Run the Project

1. Clone the repository

```
git clone https://github.com/yourusername/credit-card-fraud-detection.git
```

2. Open the notebook in **Google Colab** or **Jupyter Notebook**

3. Upload the dataset file `creditcard.csv`

4. Run all cells to reproduce the results

---

## Future Improvements

* Use advanced techniques such as **SMOTE for class imbalance**
* Try deep learning models for fraud detection
* Deploy the model as a **fraud detection API**

---
