# Applied Machine Learning Fundamentals

This repository documents a structured refresh of core Machine Learning concepts with a strong focus on practical intuition, data quality, and applied usage.

The goal is not to collect models, but to understand how they behave in real pipelines. Each notebook is intentionally small and focused, building concepts step by step instead of jumping to complex architectures.

---

## Motivation

Machine Learning is often approached model-first. In practice, most performance gains come from:
- clean and well-understood data
- sensible preprocessing and feature engineering
- choosing the right level of model complexity
- evaluating models correctly on unseen data

This repository revisits ML fundamentals with those priorities in mind.

---

## What this repository covers

The projects here progress gradually from core concepts to more applied settings.

Topics include:
- Linear and logistic regression
- Feature scaling and data leakage
- Regularization techniques (L1, L2, Elastic Net)
- Hyperparameter tuning using cross-validation
- Model evaluation using appropriate metrics
- Handling missing data and basic feature engineering

Later sections will build on this foundation with more advanced methods while keeping the same data-centric mindset.

---

## Repository structure

```text
ml-foundations-refresh/
│
├── 01-linear-regression/
│   ├── feature_engineering.ipynb
│   ├── linear_regression_elastic_net.ipynb
│   ├── DATA/
│       ├──AMES_Final_DF.csv
│       ├──Ames_Housing_Data.csv
│       ├── Ames_NO_Missing_Data.csv
│       ├── Ames_outliers_removed.csv
│       ├── Ames_Housing_Feature_Description.txt
│   ├── README.md
│
├── 02-logistic-regression/
│   ├── logistic_regression.ipynb
│   ├── DATA/
│       ├──heart.csv
│   ├── README.md
│
├── 03-k-nearest-neighbors (knn)/
│   ├── knn.ipynb
│   ├── DATA/
│       ├──sonar.all-data.csv
│   ├── README.md
│
├── 04-Support-vector-machines/
│   ├── SVM.ipynb
│   ├── DATA/
│       ├──wine_fraud.csv
│   ├── README.md
│
└── README.md
```

---

## Each folder focuses on a single concept or technique and contains:
- a notebook with clean, readable code
- a short README explaining the intent of the exercise

---

## Example project
- Linear Regression with Elastic Net
- This project applies linear regression to a real housing dataset.
- ### Key steps include:
    - separating features and target variables
    - train test split with held-out data
    - feature scaling using StandardScaler
    - Elastic Net regularization to balance bias and variance
    - GridSearchCV to tune hyperparameters
    - evaluation using MAE and RMSE on unseen data

---

The intent is to demonstrate how classical models are used responsibly in applied settings, rather than to optimize scores aggressively.

---

## Tools and libraries

1. Python
2. NumPy
3. pandas
4. scikit-learn
5. Matplotlib
6. Seaborn

---

## How to use this repository

If you are revisiting ML fundamentals:
- start from the earliest folders
- read the notebooks in orderfocus on understanding why each step exists

## If you are skimming:

- check the section READMEs
- inspect evaluation choices and preprocessing decisions

## Notes

This repository is a work in progress. New sections will be added incrementally as concepts are revisited and consolidated.

The emphasis throughout remains the same:
clarity, correctness, and practical intuition over complexity.

---

## License
This project is intended for learning and reference purposes.
