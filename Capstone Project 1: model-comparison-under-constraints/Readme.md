# Model Comparison Under Constraints — Credit Card Fraud Detection

This folder contains a comparative classification study focused on how different machine learning models behave under **severe class imbalance** and **limited modeling freedom**.

Rather than optimizing performance, the goal of this project is to understand **model inductive bias, failure modes, and stability** in a realistic applied setting.

---

## Problem Overview

The task is to detect fraudulent credit card transactions using a highly imbalanced dataset:

- Total transactions: 284,807  
- Fraudulent transactions: 492 (~0.17%)

The feature set consists of PCA-transformed numerical variables, with no access to original domain features. This removes feature engineering as a lever and shifts focus to **model behavior**.

---

## Constraints

The following constraints were intentionally enforced:

- No feature engineering beyond scaling
- No resampling techniques (SMOTE, undersampling)
- No class weighting
- Same train–test split across models
- Default model configurations for baseline comparison

These constraints isolate the effect of **model choice**.

---

## Models Compared

The following classifiers were evaluated:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

All models were trained on the same scaled data and evaluated using identical metrics.

---

## Evaluation Metrics

Given the extreme class imbalance, accuracy is not a meaningful metric.

Model behavior was evaluated using:
- confusion matrices
- precision and recall for the fraud class
- Precision–Recall curves
- ROC curves (interpreted with caution)

---

## Sensitivity and Stability Analysis

A light sensitivity analysis was performed to assess model stability:

- Logistic Regression: varying regularization strength (`C`)
- KNN: varying number of neighbors (`k`)
- SVM: varying regularization parameter (`C`)

The goal was not optimization, but to observe how **small parameter changes affect behavior**.

---

## Key Observations

- Logistic Regression is highly stable but conservative, with limited recall under imbalance.
- KNN captures the most fraudulent transactions but is sensitive to hyperparameters.
- SVM provides a balance between recall and stability, adapting smoothly to regularization changes.
- Precision–Recall curves are more informative than ROC curves in this setting.
- Different models fail in different ways under the same constraints.

---

## Takeaway

This project demonstrates that model selection in imbalanced classification is not about choosing the model with the highest score, but about understanding **trade-offs, failure modes, and robustness**.

The same data and preprocessing can lead to very different outcomes depending on the model’s inductive bias.

---

## Notes

This project is part of a broader effort to revisit and consolidate classical machine learning fundamentals with an emphasis on applied reasoning and realistic constraints.
