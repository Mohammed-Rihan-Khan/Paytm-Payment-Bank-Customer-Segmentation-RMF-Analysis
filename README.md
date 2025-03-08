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

### Cluster 0: At-Risk Customers
- **Characteristics**: Moderate recency (56 days), low frequency (1 transaction), moderate spending (INR 158)
- **Strategy**: Targeted re-engagement campaigns, personalized offers, and feedback collection

### Cluster 1: Promising Loyalists
- **Characteristics**: Moderate recency (48 days), moderate frequency (2 transactions), high spending (INR 3111)
- **Strategy**: Loyalty programs, personalized financial advice, and premium banking services

### Cluster 2: Potential Loyalists
- **Characteristics**: Moderate recency (58 days), low frequency (1 transaction), high spending (INR 2636)
- **Strategy**: Targeted marketing campaigns, dedicated relationship managers, and premium service offerings

### Cluster 3: New Customers
- **Characteristics**: Very recent (0 days), moderate frequency (1 transaction), moderate spending (INR 2385)
- **Strategy**: Personalized onboarding, educational resources, welcome incentives, and regular feedback collection

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
