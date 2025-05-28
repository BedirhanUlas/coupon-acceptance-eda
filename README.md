
# Will the Customer Accept the Coupon?

## 🎯 Objective
The purpose of this project is to analyze behavioral patterns in accepting driving-related coupons based on various contextual and demographic factors. The goal is to identify characteristics that influence a customer's likelihood to accept a coupon, using visualizations and exploratory data analysis.

## 📦 Dataset
- **Source**: UCI Machine Learning Repository
- **Data Collection**: Conducted through Amazon Mechanical Turk
- **Features**: 
  - Contextual (weather, time, destination, passenger)
  - Demographic (age, income, occupation, education)
  - Coupon types (bar, restaurant, coffee house, etc.)
  - Target variable: `Y` (1 = accepted, 0 = rejected)

## 🛠️ Tools & Libraries
- Python 3
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📊 Project Highlights
- Performed missing value analysis and imputation using mode for categorical features.
- Visualized distributions of target and feature variables.
- Focused on **bar coupons** to investigate patterns of acceptance:
  - Drivers under age 30 and those who frequent bars were more likely to accept.
  - Marital status and presence of kids affected acceptance rate.
- Conducted independent investigation on **coffee house coupons**, revealing similar behavioral patterns among specific demographic groups.

## 📈 Key Insights
- Drivers who frequently visit bars or coffee houses are more likely to accept coupons related to those venues.
- Younger drivers and those not accompanied by children tend to accept offers more.
- Income and occupation also show correlation with coupon acceptance in certain categories.

## 📁 Repository Contents
- `notebook.ipynb`: Full analysis in Jupyter Notebook format
- `coupons.csv`: Dataset used
- `README.md`: Project overview and documentation

## ✅ Status
This project was developed as part of the UC Berkeley Machine Learning Certificate program — Assignment 5.1: “Will the Customer Accept the Coupon?”
