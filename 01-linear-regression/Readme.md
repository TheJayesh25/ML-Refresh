# Linear Regression — Feature Engineering and Elastic Net

This folder contains a small, focused walkthrough of applying linear regression to a real housing dataset, starting from data preparation and ending with a regularized regression model.

The intent is to demonstrate how linear regression is used responsibly in practice, with attention paid to data quality, preprocessing, and evaluation rather than just fitting a model.

---

## Contents

### 1. Feature Engineering and Data Preparation

The first notebook focuses entirely on preparing the dataset before modeling.

Key steps include:
- inspecting features with missing values
- understanding what missing data represents for different columns
- deciding when to drop rows, drop features, or keep values
- handling outliers thoughtfully instead of removing them blindly
- removing identifiers and features that do not contribute to learning

The outcome of this step is a cleaned, consistent dataset that is safe to pass into a regression model.

---

### 2. Linear Regression with Elastic Net

The second notebook applies linear regression to the prepared dataset using Elastic Net regularization.

This notebook covers:
- separating features and target variables
- train–test split with a held-out test set (10%)
- feature scaling using `StandardScaler`
- Elastic Net regression (L1 + L2 regularization)
- hyperparameter tuning using `GridSearchCV`
- evaluation on unseen data using MAE and RMSE

Elastic Net is used to balance bias and variance while keeping the model interpretable, making it a practical baseline for applied settings.

---

## Results

Performance on the unseen test set:
- Mean Absolute Error (MAE): approximately $14,195
- Root Mean Squared Error (RMSE): approximately $20,558

The goal here is not aggressive optimization, but to establish a strong, well-evaluated baseline model.

---

## Why this approach

Linear regression remains a valuable tool because it:
- surfaces data quality issues early
- forces careful handling of scaling and leakage
- provides interpretable baselines for applied ML and research work

This folder intentionally separates data preparation from modeling to reflect how real-world ML pipelines are built.

---

## Notes

These notebooks are part of a broader effort to revisit and consolidate Machine Learning fundamentals with an emphasis on clarity, correctness, and practical intuition.

Further sections will build on this foundation.
