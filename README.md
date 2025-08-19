# Customer-Churn-Prediction
📊 Applied ML project predicting customer churn for a video streaming service. Built logistic regression & decision tree models with oversampling to improve sensitivity. Insights help reduce churn by targeting at-risk customers.


# Predictive Analytics for Customer Churn  

This project applies **machine learning** to predict customer churn in a video streaming service. Using anonymized subscription data, we built interpretable models (logistic regression and decision tree) to identify at-risk customers and recommend retention strategies.  

---

## 📌 Objectives  
- Predict customer churn based on account, usage, and billing features.  
- Improve model **sensitivity** (recall for churned customers).  
- Provide actionable insights to help reduce customer loss.  

---

## 📊 Dataset  
We used the **Kaggle Predictive Analytics for Customer Churn Dataset**.  
- **24,378 records** of anonymized customers.  
- Target variable: `Churn (1 = churned, 0 = not churned)`.  
- Features include:  
  - **Numerical:** AccountAge, MonthlyCharges, TotalCharges, ViewingHoursPerWeek, AverageViewingDuration, SupportTicketsPerMonth, ContentDownloadsPerMonth, UserRating.  
  - **Categorical:** SubscriptionType, PaymentMethod, ContentType, DeviceRegistered, GenrePreference, Gender, PaperlessBilling, etc.  

---

## 🔍 Approach  
1. **Data Exploration:** Distribution checks, correlation heatmaps, churn histograms.  
2. **Feature Engineering:** One-hot encoding for categorical variables, scaling numerical features.  
3. **Modeling:**  
   - Logistic Regression (baseline + oversampled)  
   - Decision Tree (CART, tuned via GridSearch)  
4. **Oversampling:** Balanced the dataset (50/50 churn vs non-churn) to boost sensitivity.  
5. **Evaluation:** Accuracy, Precision, Recall (Sensitivity), ROC-AUC.  

---

## 📈 Results  
- **Baseline Logistic Regression:** Accuracy 0.83, Precision 0.57, Sensitivity 0.12  
- **Oversampled Logistic Regression:** Accuracy 0.68, Precision 0.32, Sensitivity 0.70, AUC = 0.75  
- **Oversampled Decision Tree:** Accuracy 0.64, Precision 0.29, Sensitivity 0.69, AUC = 0.72  

✅ **Best Model:** Oversampled Logistic Regression → best tradeoff between interpretability & predictive power.  

---

## 💡 Key Insights  
- Customers most likely to churn are:  
  - **New accounts** (low AccountAge)  
  - **Low engagement** (low viewing hours, short durations, few downloads)  
  - **High monthly charges**  
- Reducing churn requires:  
  - Early engagement strategies for new users.  
  - Personalized discounts for high-charge accounts.  
  - Features that encourage **longer viewing & content interaction**.  

---

## 🛠️ Tools & Technologies  
- **Python:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **ML Models:** Logistic Regression, Decision Trees (CART)  
- **Techniques:** Oversampling, GridSearchCV, ROC Curve Analysis  

---

## ⚙️ How to Run This Project  

### 1. Clone the Repository  
```bash
git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction
