# Credit-Card-Draud-Detection-Machine-Learning-Project

## Objective
The goal of this project was to detect fraudulent credit card transactions using machine learning, with a focus on handling an imbalanced classification problem and evaluating model performance beyond simple accuracy.

## Project Context
This project was completed as part of a cross-collaborative sprint. It focused on applying machine learning methods to a real-world fraud detection problem where fraudulent transactions are rare but highly important to identify.

## Dataset
The dataset contains credit card transaction records labeled as fraudulent or non-fraudulent. Because fraud cases are much less common than legitimate transactions, this project required careful attention to class imbalance and evaluation metrics.

## Methodology
The workflow for this project included:

- Loading and cleaning the dataset
- Exploring class imbalance and transaction patterns
- Preparing features for modeling
- Training machine learning classifiers
- Using Random Forest as a primary model
- Evaluating the model using metrics such as precision, recall, and confusion matrix

## Why Random Forest?
Random Forest was a strong choice for this problem because it can capture non-linear relationships, handle complex interactions between variables, and provide robust performance on classification tasks.

## Results
The project successfully demonstrated how machine learning can be used to identify fraudulent transactions. Because fraud detection is an imbalanced classification problem, evaluation focused on metrics such as:

- Precision
- Recall
- Confusion Matrix
- Classification performance on the minority class

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
![Class Distribution](docs/images/class_distribution.png)

### Confusion Matrix
![Confusion Matrix](docs/images/confusion_matrix.png)

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
