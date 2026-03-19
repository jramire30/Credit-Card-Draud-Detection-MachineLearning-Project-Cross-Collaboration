# Credit-Card-Draud-Detection-Machine-Learning-Project

## Objective
The goal of this project was to detect fraudulent credit card transactions using machine learning, with a focus on handling an imbalanced classification problem and evaluating model performance beyond simple accuracy.

## Project Context
This project was completed as part of a cross-collaborative sprint. It focused on applying machine learning methods to a real-world fraud detection problem where fraudulent transactions are rare but highly important to identify.

## Dataset
The dataset contains credit card transaction records labeled as fraudulent or non-fraudulent. Because fraud cases are much less common than legitimate transactions, this project required careful attention to class imbalance and evaluation metrics. Please note this Kaggle dataset has been PCA transformed.
- Credit card transaction dataset
- Binary target variable:
  - 0 → Non-fraud
  - 1 → Fraud
- Highly imbalanced dataset (fraud cases are rare)
- PCA Transformed

## Methodology
The workflow for this project included:

### 1. Data Preparation
- Cleaned and structured transaction data
- Separated features and target variable
- Performed train/test split to ensure proper evaluation

### 2. Handling Class Imbalance
- Recognized that fraud detection is an imbalanced classification problem
- Focused on evaluation metrics beyond accuracy

### 3. Modeling
Two models were implemented:
- Logistic Regression (baseline)
- Random Forest (ensemble model)

Random Forest was selected as the final model due to its ability to capture non-linear patterns and improve classification performance.

## Why Random Forest?
Random Forest was a strong choice for this problem because it can capture non-linear relationships, handle complex interactions between variables, and provide robust performance on classification tasks.

## Model Evaluation

Because of class imbalance, evaluation focused on:

- Precision
- Recall
- Precision-Recall Curve
- AUPRC (Area Under Precision-Recall Curve)

## Results
| Model | AUPRC |
|------|------|
| Logistic Regression | 0.741 |
| Random Forest | 0.862 |

Random Forest significantly outperformed Logistic Regression.

## Key Insights
- Fraud detection cannot be evaluated using accuracy alone
- Class imbalance makes recall especially important
- Random Forest provides a strong baseline for fraud classification
- The project highlighted the tradeoff between catching fraud and avoiding false alarms

## Challenges and Solutions
### Challenge 1: Severe class imbalance
Fraudulent transactions were much less common than non-fraudulent transactions, which made the problem difficult.

**Solution:** The project focused on appropriate evaluation metrics and model interpretation rather than relying only on overall accuracy.

### Challenge 2: Model evaluation
A model can appear highly accurate while still performing poorly at detecting fraud.

**Solution:** Precision, recall, and confusion matrix analysis were used to better understand real model performance.

## Visualizations

### Class Distribution
<img width="104" height="50" alt="image" src="https://github.com/user-attachments/assets/153f8ed2-ca17-4074-aa36-b77324cd1423" />

### Area Under the Curve Precision-Recall Curve (Fraud Detection) Method Performance
<img width="578" height="487" alt="image" src="https://github.com/user-attachments/assets/71a9618a-5130-40f0-975c-d54a6b8ee44b" />


### Confusion Matrix
<img width="441" height="195" alt="image" src="https://github.com/user-attachments/assets/615ae83d-f4f7-4570-9295-2b162c32e194" />
<img width="441" height="195" alt="image" src="https://github.com/user-attachments/assets/2b9a3ce3-0bc0-4be1-b9fc-900ddebe6490" />


## Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Repo Structure
```text
credit-card-fraud-detection-random-forest/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── credit_card_fraud_detection.ipynb
├── docs/
│   └── images/
└── reports/
