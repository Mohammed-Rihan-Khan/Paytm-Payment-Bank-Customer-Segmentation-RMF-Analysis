# Paytm Payment Bank Customer Segmentation: RMF Analysis
## Overview
This project implements customer segmentation for a banking institution using RFM (Recency, Frequency, Monetary) analysis and machine learning techniques. By analyzing transaction patterns, the model categorizes bank customers into distinct segments, enabling targeted marketing strategies and improved customer relationship management.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Features](#key-features)
- [Technical Implementation](#technical-implementation)
- [Results and Insights](#results-and-insights)
- [Installation and Usage](#installation-and-usage)
- [Requirements](#requirements)
- [Future Work](#future-work)

## Introduction
Customer segmentation is a vital strategy for banks to understand their diverse customer base and tailor services accordingly. This project utilizes RFM analysis, a powerful customer segmentation technique that evaluates customers based on three key dimensions:
- **Recency (R)**: How recently a customer has made a transaction
- **Frequency (F)**: How often a customer makes transactions
- **Monetary (M)**: How much money a customer spends on transactions

By scoring customers on these dimensions, banks can identify their most valuable customers, understand behavior patterns, and develop targeted marketing strategies.

## Dataset
The analysis uses the "bank_transactions.csv" dataset containing the following variables:
- **TransactionID**: Unique identifier for each transaction
- **CustomerID**: Unique identifier for each customer
- **CustomerDOB**: Customer's date of birth
- **CustGender**: Customer's gender
- **CustLocation**: Customer's location
- **CustAccountBalance**: Account balance at the time of transaction
- **TransactionDate**: Date of the transaction
- **TransactionTime**: Time of the transaction
- **TransactionAmount (INR)**: Transaction amount in Indian Rupees

## Methodology
The project follows these key steps:
1. **Data Preprocessing**: Cleaning, handling missing values, and transforming variables
2. **RFM Calculation**:
   - Recency: Days since last transaction
   - Frequency: Total number of transactions
   - Monetary: Total amount spent
3. **Feature Engineering**: Applying log transformation to handle skewness
4. **Clustering**: Using K-means algorithm with the optimal number of clusters
5. **Scoring**: Assigning RFM scores based on quartiles
6. **Segmentation**: Creating comprehensive customer segments based on RFM scores

## Key Features
- Comprehensive data cleaning and preprocessing
- Log transformation to handle skewed distributions
- Optimal cluster determination using the Elbow Method
- 3D visualization of customer segments
- Detailed RFM scoring system
- Strategic interpretation of customer clusters

## Technical Implementation
The project utilizes several advanced techniques:
- **Data Transformation**: Log transformation to normalize skewed distributions
- **Feature Scaling**: StandardScaler for normalizing feature ranges
- **Clustering Algorithm**: K-means with an optimized number of clusters
- **Visualization**: 2D and 3D scatter plots for cluster visualization
- **Quantile-based Scoring**: Dividing customers into quartiles for RFM scoring

## Results and Insights
The analysis identified four distinct customer segments:

### **Cluster 0: Low-Value, At-Risk Customers**
**Recency:** 58 days (moderate)

**Frequency:** ~1 transaction (very low)

**Monetary:** ₹67 (extremely low spending)

#### **Interpretation:**
Customers in this cluster are sporadic users who make very few transactions and spend the least amount. They are at risk of becoming inactive or completely disengaged from the banking services.

#### **Strategy:**
**📌 Reactivation Campaigns:** Provide special promotions, cashback, or rewards for transactions.

**📌 Personalized Outreach:** Offer reminders, alerts, or targeted financial products to keep them engaged.

**📌 Understanding Barriers:** Conduct surveys to analyze why these customers have low engagement.

### **Cluster 1: High-Engagement Customers**
**Recency:** 48 days (moderate)
**Frequency:** ~2 transactions (moderate)
**Monetary:** ₹1071 (high spending)
#### **Interpretation:**
This cluster consists of frequent users with high spending power, making them a valuable customer segment. These customers are actively using banking services and show strong potential for loyalty.

#### **Strategy:**
**📌 Exclusive Loyalty Programs:** Offer reward-based transactions, higher interest rates on savings, or exclusive investment opportunities.

**📌 Personalized Banking Services:** Provide dedicated relationship managers or financial advisors.

**📌 Cross-Selling Opportunities:** Introduce them to premium credit cards, loans, or wealth management services.

### **Cluster 2: Wealthy But Infrequent Users**
**Recency:** 66 days (moderate-high)
**Frequency:** ~1 transaction (very low)
**Monetary:** ₹719 (high spending)
#### **Interpretation:**
This segment consists of high-value customers who transact very infrequently. They may be using the bank for specific services but are not fully engaged.

#### **Strategy:**
**📌 Encourage More Frequent Transactions:** Offer benefits for repeated usage, such as transaction-based rewards.

**📌 Highlight Additional Services:** Introduce them to investment options, savings plans, or financial advisory.

**📌 Reduce Inactivity Risk:** Personalized follow-ups and special incentives for continued banking engagement.

### **Cluster 3: Young & Growing Customers**
**Recency:** 39 days (low, very recent transactions)
**Frequency:** ~1 transaction (low-moderate)
**Monetary:** ₹612 (moderate spending)
#### **Interpretation:**
This segment consists of recently active customers who are moderate spenders but have not yet reached high levels of engagement. They may include new customers or young professionals testing banking services.

#### **Strategy:
**📌 Onboarding Support:** Provide educational resources, app tutorials, and welcome offers.

**📌 Incentives for More Usage:** Cashback on first deposits, discounts on digital transactions, or promotional interest rates.

**📌 Personalized Customer Journey:** Offer targeted recommendations based on their banking behavior.

###**📌 Conclusion**
Applying K-Means clustering to Recency, Frequency, and Monetary (RFM) data has provided valuable insights into customer segmentation. The segmentation reveals four distinct customer types:

**1️⃣ At-Risk Customers** – Require re-engagement to prevent churn.

**2️⃣ High-Engagement Customers** – Need loyalty programs to maximize lifetime value.

**3️⃣ Wealthy But Infrequent Users** – Need incentives for higher transaction frequency.

**4️⃣ Growing Customers** – Require nurturing to develop long-term engagement.


Strategically implementing personalized banking offers, proactive customer service, and targeted marketing campaigns will help maximize customer retention, satisfaction, and long-term profitability in the banking sector.

## Installation and Usage
1. Clone the repository
2. Install required dependencies: `pip install -r requirements.txt`
3. Place your transaction data in the project directory or adjust the file path in the code
4. Run the Jupyter notebook or Python script: `python customer_segmentation.py`

## Requirements
- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- yellowbrick

## Future Work
- Implement more advanced clustering algorithms like DBSCAN or Hierarchical Clustering
- Incorporate additional customer attributes for more nuanced segmentation
- Develop a predictive model to forecast customer movement between segments
- Create an interactive dashboard for real-time monitoring of customer segments
- Design and implement targeted marketing campaigns based on segment insights
