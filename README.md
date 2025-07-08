# CSAT Insight – Predicting Customer Satisfaction Using Machine Learning

## 📌 Project Overview

This project aims to predict **Customer Satisfaction (CSAT)** based on customer support data using supervised machine learning techniques. The goal is to proactively identify **dissatisfied customers** and uncover the key drivers of low satisfaction to help improve service quality.

---

## 📊 Dataset

The dataset used in this project is a **real-world, masked dataset from Flipkart customer support interactions**. It includes anonymized support records with features such as:

- `Issue Category` and `Sub-Category`
- `Agent Shift` and `Experience`
- `Time taken to respond`
- Final `CSAT Score` (1 to 5)

For the purpose of this project, the CSAT scores were converted into a **binary classification**:
- `0` → Dissatisfied (CSAT ≤ 3)
- `1` → Satisfied (CSAT ≥ 4)

This transformation helps focus the model on detecting **at-risk customer interactions** where proactive intervention is most impactful.

## ⚙️ Techniques Used

- **Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn**
- **Data Cleaning & Feature Engineering**
  - Extracted response time from timestamps
  - Encoded categorical features
  - Mapped experience from tenure bucket
- **SMOTE** for class imbalance handling
- **Random Forest Classifier** for prediction
- **GridSearchCV** for hyperparameter tuning
- **Evaluation** with accuracy, precision, recall, F1-score

---

## 📈 Results

| Metric         | Value (Class 0) |
|----------------|-----------------|
| **Accuracy**   | 70%             |
| **Recall**     | 36%             |
| **Precision**  | 25%             |
| **F1-Score**   | 29%             |

The model was successful in identifying a significant portion of **dissatisfied customers**, providing valuable insights for proactive support actions.

---

## 💡 Key Insights

- **Longer response times** are correlated with low satisfaction
- Certain **issue types** (e.g., login issues, disconnections) have higher dissatisfaction rates
- **Agent shifts** (especially morning/night) show slightly lower CSAT performance
- **Classification models** outperformed regression in predicting useful business outcomes

---

## 🧠 Business Strategies Suggested

- Reduce average response time through automated triaging
- Improve agent training in high-risk issue categories
- Balance staffing across shifts for consistent service quality
- Use model predictions to flag and follow up with at-risk customers

---
