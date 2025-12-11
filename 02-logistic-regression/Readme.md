# Logistic Regression — Classification Pipeline and Evaluation

This folder contains a focused walkthrough of applying logistic regression to a binary classification problem, covering the full pipeline from data inspection to model evaluation and probability-based predictions.

The intent is to reinforce how logistic regression is used in practice as an interpretable and reliable baseline for classification tasks.

---

## Overview

The notebook in this folder walks through an end-to-end classification workflow using logistic regression, starting from raw data and ending with evaluated predictions.

The emphasis is on understanding each step of the pipeline rather than optimizing aggressively.

---

## Workflow Covered

### 1. Data Loading and Exploration

The notebook begins with loading the dataset and performing basic exploratory analysis:
- inspecting feature distributions
- checking for missing values
- understanding the target variable distribution

Visualizations such as countplots, pairplots, and correlation heatmaps are used to explore relationships between features and the target.

---

### 2. Data Preparation

After exploration, the data is prepared for modeling:
- splitting the dataset into training and test sets
- scaling features to normalize the input space
- ensuring consistent preprocessing between training and test data

---

### 3. Logistic Regression with Cross-Validation

The model is trained using `LogisticRegressionCV` from scikit-learn:
- automatic selection of the optimal regularization strength (`C`)
- regularization applied to control model complexity
- probability-based predictions for classification

This setup reflects how logistic regression is typically applied as a baseline model in real-world settings.

---

### 4. Model Evaluation

Model performance is evaluated using multiple classification diagnostics:
- confusion matrix and corresponding visualizations
- ROC curve
- precision–recall curve

These metrics help analyze both classification accuracy and the trade-offs between false positives and false negatives.

---

### 5. Prediction and Interpretation

Finally, the trained model is used to:
- predict class labels on the test set
- estimate probabilities for individual samples
- interpret predictions in a practical, decision-oriented context

---

## Why logistic regression

Logistic regression remains widely used because it:
- is interpretable and easy to debug
- provides calibrated probability outputs
- serves as a strong baseline before more complex models

This notebook treats logistic regression as a core tool for understanding classification behavior, not just as a stepping stone to advanced models.

---

## Notes

This folder is part of a broader effort to revisit and consolidate Machine Learning fundamentals with an emphasis on clarity, correctness, and applied intuition.

Additional models and techniques build on this foundation in later sections.
