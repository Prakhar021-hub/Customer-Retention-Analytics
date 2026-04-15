# Customer Churn Prediction

Predicting customer churn using machine learning, with a focus on improving recall for at-risk customers.

---

##  Overview  

This project aims to identify customers who are likely to churn using a classification model built on structured customer data.  

Instead of optimizing only for accuracy, the focus is on improving **recall for churned customers**, since missing a churn case has a higher business impact than a false positive.

---

## Problem Statement  

Customer churn directly affects revenue. The goal is to build a model that can:

- Identify customers at risk of leaving  
- Help prioritize retention strategies  
- Balance detection (recall) with reliability (precision)  

---

##  Model Used  

**Random Forest Classifier**

Chosen for:
- Strong performance on tabular data  
- Ability to model non-linear relationships  
- Robustness against overfitting  

---

## Results  

| Metric   | Score   |
|----------|--------|
| Accuracy | 76.15% |
| ROC-AUC  | 0.838  |

### Classification Performance  

| Class          | Precision | Recall | F1-score |
|----------------|----------|--------|----------|
| Non-Churn (0)  | 0.91     | 0.75   | 0.82     |
| Churn (1)      | 0.53     | 0.78   | 0.64     |

---

## Key Takeaways  

- Recall for churn improved significantly (**0.78**), meaning most at-risk customers are now detected  
- Precision dropped (**0.53**), indicating more false positives  
- This trade-off is intentional — in churn prediction, **recall is more critical than precision**  

---

##  Visual Insights  

### Confusion Matrix  
- High detection of churn cases  
- Increase in false positives due to recall optimization  

### ROC Curve  
- AUC of ~0.84 shows strong class separability  

### Feature Importance  
Top drivers of churn:
- Tenure  
- Contract type  
- Internet service type  
- Monthly and total charges  

---

## Challenges  

- Class imbalance (fewer churned customers)  
- Precision–recall trade-off  
- Model sensitivity to dominant features  

---

##  Improvements in Progress  

- Applying **SMOTE** to handle class imbalance  
- Experimenting with **threshold tuning**  ( I did tried this in a seperate file but I was not very satisfied with the results, but there is a scope for improvement)
- Testing advanced models like **XGBoost / LightGBM**  (I am planning to experiment with these models too in the future)
- Enhancing feature engineering 

---

##  Why This Project Matters  

This project goes beyond basic model building by:

- Focusing on **business-relevant metrics (recall)**  
- Demonstrating **iteration and improvement**  
- Highlighting **trade-offs instead of hiding them**  

---

## Tech Stack  

- Python  
- Scikit-learn  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

##  Project Structure  

├── data/
├── notebooks/
├── model.py
├── utils/
├── README.md


---

## Future Scope  

- Deploy as a Streamlit web app  
- Add SHAP-based explainability  
- Build a real-time prediction pipeline  

---

##  Author  

**Prakhar Rajak**
