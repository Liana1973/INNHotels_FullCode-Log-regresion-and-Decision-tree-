
# 🏨 INN Hotels Booking Cancellation Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Decision%20Tree-green)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Type](https://img.shields.io/badge/Type-Classification-orange)

---

## 📊 Project Overview

This project focuses on predicting hotel booking cancellations using Machine Learning.  
The goal is to help INN Hotels reduce revenue loss by identifying high-risk bookings in advance.

📌 Dataset: 36,275 hotel bookings  
📌 Problem Type: Binary Classification  
📌 Target Variable: booking_status (Canceled / Not_Canceled)

---

## 🎯 Business Goal

Reduce cancellation-driven revenue loss by:
- Identifying risky bookings early
- Improving pricing strategies
- Optimizing room allocation
- Enhancing customer targeting

---

## 🎯 Objective

- Analyze booking patterns and customer behavior
- Identify key factors influencing cancellations
- Build a machine learning model to predict cancellations
- Improve hotel decision-making regarding pricing, availability, and customer targeting

---

## 📊 Dataset Description

The dataset contains **36,275 hotel bookings** with 19 features describing customer behavior and booking details.

### Target Variable:
- `booking_status`
  - 1 → Canceled
  - 0 → Not Canceled

### Key Features:
- lead_time
- market_segment_type
- avg_price_per_room
- no_of_special_requests
- repeated_guest
- arrival_month
- room_type_reserved
- and others

---

## 🧹 Data Preprocessing

- Removed irrelevant column: `Booking_ID`
- Handled outliers in `avg_price_per_room` using IQR capping
- Encoded target variable (Canceled = 1, Not_Canceled = 0)
- Verified no missing values or duplicates

---

## 📈 Exploratory Data Analysis (EDA)

### Key Insights:

- 📅 **Seasonality:**  
  Peak bookings occur in **August–October**, while winter months show lower demand.

- 🌍 **Market Segment:**  
  Online bookings dominate and have the highest cancellation rate.

- 💰 **Price Impact:**  
  Higher-priced bookings are more likely to be canceled.

- ⏳ **Lead Time:**  
  Longer lead times significantly increase cancellation probability.

- ⭐ **Special Requests:**  
  More special requests strongly reduce cancellation probability.

- 👥 **Loyal Customers:**  
  Repeated guests almost never cancel.

- 👨‍👩‍👧 Family Size:**  
  Medium-sized families show higher cancellation rates than large stable groups.

---

## 🤖 Machine Learning Model

### Model Used:
- Decision Tree Classifier

### Optimization:
- Cost Complexity Pruning (`ccp_alpha`)
- Post-pruning applied to reduce overfitting
- Best model selected using **F1-score**

---

## 📊 Model Performance

### Training Set:
- Accuracy: **0.91**
- Precision: **0.83**
- Recall: **0.93**
- F1-Score: **0.88**

### Test Set:
- Accuracy: **0.86**
- Precision: **0.76**
- Recall: **0.84**
- F1-Score: **0.80**

- # 📊 Model Results & Evaluation

## 🧠 Confusion Matrix (Test Set)

The confusion matrix shows how well the model distinguishes between canceled and non-canceled bookings.

👉 Key goal: maximize recall for canceled bookings (class = 1)


---

## 📌 Key Findings

- The model generalizes well with acceptable overfitting gap
- Recall remains strong on unseen data, which is critical for detecting cancellations
- Post-pruned Decision Tree improves interpretability and stability
- Business-critical patterns were successfully captured

---

## 🏨 Business Impact

This model helps INN Hotels to:

- Predict high-risk bookings early
- Reduce revenue loss from cancellations
- Optimize pricing and discount strategies
- Improve room allocation and staffing decisions
- Identify customer segments with high cancellation risk

---

## 📉 Conclusion

The post-pruned Decision Tree provides a strong balance between:
- Predictive performance
- Generalization ability
- Interpretability

It is the most suitable model for practical hotel operations where transparency and early cancellation detection are important.

---

## 🛠️ Tools & Libraries

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Statsmodels

---

## 📌 Author

Data Analytics Project — INN Hotels Cancellation Prediction  
