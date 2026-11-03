# Customer Churn Prediction

## Project Overview

This project uses Machine Learning to predict whether a telecom customer is likely to leave the company (Churn).

The goal is to analyze customer behavior, identify patterns associated with churn, and build classification models that help detect customers who are at risk of leaving.

## Dataset

- **Source:** IBM Telco Customer Churn Dataset
- **Rows:** 7,043
- **Columns:** 21
- **Target Variable:** `Churn`

The target variable is binary:
- `0`: No Churn
- `1`: Churn

## Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Project Workflow

1. Data Loading and Understanding
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Data Preprocessing
   - One-Hot Encoding
   - Feature Scaling
   - Train-Test Split
5. Model Training and Comparison
   - Logistic Regression
   - Balanced Logistic Regression
   - Random Forest
   - Balanced Random Forest
6. Feature Importance Analysis
7. Hyperparameter Tuning using GridSearchCV
8. Threshold Optimization
9. Final Model Evaluation

## Final Model

The selected model is **Logistic Regression with class_weight="balanced"**, using a classification threshold of **0.55**.

The threshold was selected using the validation set to balance Precision and Recall while prioritizing churn detection.

## Final Test Results

| Metric | Score |
|---|---:|
| Accuracy | 75% |
| Precision (Churn) | 52% |
| Recall (Churn) | 75% |
| F1-score (Churn) | 62% |

### Confusion Matrix

```text
[[780, 255],
 [ 93, 281]]
```

The model correctly identified 281 out of 374 customers who churned.

## Key Findings

- Customers with shorter tenure showed higher churn rates.
- Month-to-month contract customers had higher churn rates.
- Higher monthly charges were associated with higher churn rates.

## Project Structure

```text
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction_Final.ipynb
└── README.md
```

## How to Run

1. Clone this repository.
2. Open the notebook using Jupyter Notebook or Google Colab.
3. Install the required libraries if needed.
4. Run the notebook cells in order.

## Future Improvements

- Experiment with additional classification algorithms.
- Improve model performance through feature engineering.
- Explore more advanced techniques for handling class imbalance.
- Deploy the model as a prediction API.