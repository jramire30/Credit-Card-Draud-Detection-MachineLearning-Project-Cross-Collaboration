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

Business Decision

Risk Level	Threshold	Action
- 🟢 Low	< 0.30	Auto approve
- 🟡 Medium	0.30 – 0.90	Manual review
- 🔴 High	> 0.90	Auto block

## Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Product Integration: Algis (AI Fraud Detection System)

This machine learning model was developed as part of a cross-functional project to power **Algis**, an AI-driven fraud detection platform designed for financial institutions.

👉 View product design & demo:
- Figma Design: https://www.figma.com/design/rQaRzhwcaQZEe7OrjNPPCb/Cross-Collaboration---AIgis
- Prototype Demo: https://www.figma.com/proto/rQaRzhwcaQZEe7OrjNPPCb/Cross-Collaboration---AIgis

---

## What is Algis?

Algis is an AI-powered fraud detection system that helps financial analysts:

- Detect suspicious transactions in real time
- Assign fraud probability scores
- Prioritize high-risk transactions
- Reduce financial loss while maintaining customer trust

As shown in the project presentation :contentReference[oaicite:0]{index=0}, the system provides a centralized dashboard for monitoring fraud alerts and transaction activity.

---

## How the Model Fits into the Product

The Random Forest model developed in this project serves as the **core decision engine** of Algis.

### Model Output:
- Fraud probability score (0–1)
- Risk classification (Low / Medium / High)

### Product Usage:
- High-risk → Automatically flagged or blocked
- Medium-risk → Sent for manual review
- Low-risk → Approved automatically

---

## Product Features Powered by the Model

### 1. Dashboard Overview
Displays:
- Total transactions
- Fraud detected
- Alert volume insights
- Risk distribution (Low / Medium / High)

(Shown in dashboard wireframe in presentation :contentReference[oaicite:1]{index=1})

---

### 2. Transaction Monitoring System
- Real-time list of transactions
- Each transaction assigned a risk level
- Analysts can:
  - Approve
  - Block
  - Escalate

---

### 3. Transaction Detail View
Each transaction includes:
- Fraud probability score
- Transaction metadata (location, device, amount)
- Status (Approved / Under Review / Blocked)

---

### 4. Decision Support
The model enables:
- Faster fraud detection
- Reduced manual workload
- Data-driven decision making

---

## Target User

The primary user is a **Data Analyst or Fraud Analyst** working at a financial institution.

As defined in the project persona:
- Needs explainability and trust in AI decisions
- Requires tools for monitoring and auditing fraud detection
- Values efficiency and real-time insights

---

## Business Value

By integrating machine learning into the Algis platform:

- Reduces financial fraud losses
- Speeds up fraud detection workflows
- Improves precision in identifying fraud
- Enhances analyst productivity

---

## Future Improvements

- Real-time streaming model deployment
- Explainable AI (feature importance per transaction)
- Continuous model retraining
- Integration with banking APIs

---

## Final Takeaway

This project demonstrates not only the development of a machine learning model, but its integration into a real-world product.

The combination of:
- Data science (modeling)
- Product thinking (user workflows)
- UX design (dashboard + interactions)

creates a complete, production-ready fraud detection solution.
