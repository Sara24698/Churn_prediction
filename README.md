# 📉 Customer Churn Prediction  

Predicting which customers are likely to leave is one of the most impactful applications of machine learning in business.  
This project applies **advanced data analysis** and **classification algorithms** to identify high-risk customers and guide effective retention strategies.  

---

## 🧠 Project Overview  

This notebook explores the problem of **customer churn prediction** using multiple machine learning models —  
**Logistic Regression**, **Random Forest**, and **XGBoost** — to detect which customers are most likely to leave a service.  

The project covers the complete ML workflow:
1. **Data preprocessing** and feature selection 🧹  
2. **Exploratory Data Analysis (EDA)** 🔍  
3. **Model training and evaluation** ⚙️  
4. **Comparison of predictive performance** 📊  
5. **Churn probability estimation and business insights** 💼  

---

## 📦 Technologies Used  

- **Python 3**
- **Pandas**, **NumPy** — data handling  
- **Matplotlib**, **Seaborn** — visualization  
- **Scikit-learn** — preprocessing, model training, metrics  
- **XGBoost** — gradient boosting classification  

---

## ⚙️ Data Processing  

To enhance model performance and avoid redundancy, strongly correlated features (e.g., call minutes and number of calls) were removed.  
All features were then **standardized** to ensure that each contributes equally to the model’s learning process.

---

## 🤖 Modeling & Evaluation  

Three supervised learning algorithms were trained and compared:

| Model | Key Characteristics | AUC | F1-score (Churn) | Accuracy |
|-------|---------------------|-----|------------------|-----------|
| **Logistic Regression** | Simple, interpretable baseline | ~0.88 | ~0.49 | ~0.88 |
| **Random Forest** | Ensemble, captures non-linearities | ~0.92 | ~0.82 | ~0.96 |
| **XGBoost** | Gradient boosting, best performance | **0.92** | **0.85** | **0.96** |

📈 **XGBoost achieved the best balance between precision (0.93), recall (0.78), and overall accuracy (96%)**, making it the optimal choice for deployment.

---

## 🧩 Business Insights  

The model identified several factors strongly associated with churn:

- 📞 **Frequent customer service calls** → sign of dissatisfaction  
- 🌍 **International plan subscribers** → higher churn likelihood  
- 💰 **Higher total charges (especially daytime)** → losing high-value clients  
- 🗺️ **Regional variations** → some states/area codes show elevated churn  

**High-risk profile:**  
Customers with an international plan, multiple service calls, and higher total charges — especially in certain regions — are significantly more likely to leave.

---

## 🎯 Strategy Optimization  

Using the XGBoost model, the top 500 customers with the highest churn probabilities were selected for targeted retention.  

- Among these **top 500**, **42.2% actually churned**, compared to **14.1% ± 2.9%** in random outreach.  
- This means the model-based strategy is **3× more effective** than random selection.  


---

## 💡 Key Takeaways  

- Predictive analytics can dramatically improve **customer retention strategies**.  
- **XGBoost** provided the best trade-off between interpretability and predictive power.  
- The approach enables **efficient resource allocation** — focusing on the customers who matter most.  


