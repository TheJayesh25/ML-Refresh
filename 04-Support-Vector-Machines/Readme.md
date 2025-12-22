# Support Vector Machines (SVM) — Wine Fraud Detection

This folder contains an applied Support Vector Machine (SVM) classification project focused on detecting fraudulent wine samples in a highly imbalanced dataset.

The intent of this notebook is to understand how SVMs behave in practice when faced with limited signal strength and strong class imbalance, rather than to maximize performance metrics.

---

## Overview

The project uses a wine dataset where the target variable represents wine quality, labeled as **Fraud** or **Legit**.

A key challenge in this dataset is class imbalance:
- fraudulent samples make up a very small percentage of the data
- fraud prevalence differs across wine types (red vs white)

This makes the task a realistic example of a difficult classification problem where modeling choices alone may not be sufficient.

---

## Workflow Covered

### 1. Problem Framing and Data Inspection

The notebook begins by:
- loading the wine fraud dataset
- inspecting the structure and feature set
- examining class distribution and imbalance
- analyzing fraud prevalence by wine type

This step establishes realistic expectations before modeling.

---

### 2. Exploratory Analysis

Exploratory analysis includes:
- visualizing class imbalance
- comparing fraud rates across wine types
- examining correlations between numeric features and the target variable

The goal here is to assess whether the available features contain strong signals for fraud detection.

---

### 3. Data Preparation

Before applying SVM:
- features and labels are separated
- the dataset is split into training and test sets
- features are scaled using `StandardScaler`

Feature scaling is essential for SVMs, as distance from the decision boundary directly affects classification.

---

### 4. SVM Modeling and Hyperparameter Tuning

The model is built using `SVC` from scikit-learn.

Hyperparameters tuned using `GridSearchCV` include:
- regularization strength (`C`)
- kernel type
- kernel coefficient (`gamma`)

Cross-validation is used to evaluate parameter combinations systematically.

---

### 5. Model Evaluation

Model performance is evaluated on unseen test data using:
- confusion matrix
- classification report
- precision and recall metrics

Results highlight the difficulty of detecting fraudulent samples given the available features and class imbalance.

---

## Key Takeaways

This project reinforces several important applied ML concepts:
- class imbalance can dominate model behavior and evaluation
- strong performance is not guaranteed even with advanced models
- poor results can indicate limitations in data rather than modeling approach
- honest evaluation is critical in applied machine learning

---

## Notes

This notebook is part of a broader effort to revisit and consolidate Machine Learning fundamentals with a focus on clarity, correctness, and realistic expectations.

Subsequent sections in the repository build on these ideas with different models and problem settings.
