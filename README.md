# Customer Churn Prediction

A machine learning project to predict customer churn using Logistic Regression, SVC, KNN, and Decision Tree.

## Dataset
Kaggle customer churn dataset (440k rows, train/test split provided separately)

## What I found
- Caught a data leakage bug — CustomerID had -0.84 correlation with Churn because the synthetic dataset assigned IDs in a way that encoded the target. Removing it dropped accuracy from 96% to 87% but made the model honest.
- Fixed a silent encoding bug where 'Standard' subscription type was mapped incorrectly, turning 149k rows into NaN.
- Learned why train_test_split gives inflated results vs evaluating on a genuinely separate test file.

## Results (honest — separate test file)
| Model | Accuracy |
|-------|----------|
| Logistic Regression | 58% |
| SVC | 58% |

## Tools
Python, scikit-learn, pandas, seaborn, matplotlib
