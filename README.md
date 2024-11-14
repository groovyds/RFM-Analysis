# RFM-Analysis
We will be working on a retail dataset and perform an RFM Analysis and Purchase Propensity Model to predict future buying patterns


# CRM and RFM Analysis with Supervised and Unsupervised Machine Learning

This project aims to perform Customer Relationship Management (CRM) and Recency, Frequency, and Monetary (RFM) analysis to segment customers and predict purchase propensity using machine learning techniques. The analysis leverages advanced modeling methods and visualizations to extract actionable insights.

# Project Overview

This project:

1)Processes raw customer data to derive RFM scores.

2)Segments customers into actionable categories.

3)Implements machine learning (XGBoost and Logistic Regression) for purchase propensity prediction.

4)Visualizes key insights through interactive dashboards and plots.


# Dataset

The dataset contains the following columns:

- InvoiceNo: Invoice number (transaction ID).
- StockCode: Product code.
- Description: Product description.
- Quantity: Quantity of the product sold.
- InvoiceDate: Date of the invoice.
- UnitPrice: Price per product unit.
- CustomerID: Unique customer identifier.
- Country: Country of the customer.

# Data Preprocessing

1)**Missing Values**:

  Rows with missing CustomerID were dropped.

2)**Outliers**:

  Negative values in Quantity and UnitPrice were removed.
  Extreme outliers in Quantity and UnitPrice were addressed using the interquartile range (IQR) method.

3)**Feature Engineering**:

  RFM metrics (Recency, Frequency, Monetary) were derived.
  Time frames (e.g., the last 90 days) were used to align RFM values with the model's requirements.

# RFM Analysis

**Scoring:** RFM values were binned using qcut into 4 categories:

- R_Score: Based on Recency (recent transactions).
- F_Score: Based on Frequency (number of transactions).
- M_Score: Based on Monetary (total revenue generated).

**Customer Segmentation:**


Customers were segmented into categories such as "Champions," "Loyal Customers," "Potential Loyalists," etc., based on their RFM scores.
Interactive pie charts and bar charts were created to visualize segment distributions.

# Purchase Propensity

Models Used: XGBoost and Logistic Regression

1)XGBoost:

Trained on RFM scores for the last 90 days to predict customer purchase propensity.
Hyperparameters were tuned for optimal performance.
Metrics Used: AUC-ROC, Log-Loss.

2)Logistic Regression:

Implemented as a simpler alternative to XGBoost.
Provided comparable performance with reduced complexity.

**Steps:**


1)Feature Selection: Recency, Frequency, and Monetary.

2)Cross-Validation: 5-fold cross-validation for robust evaluation.

3)Visualization: ROC-AUC curves and feature importances plotted to assess model performance.

# Results

- Successfully segmented customers into meaningful categories.
- Developed models to predict purchase propensity with high accuracy.
- Derived actionable insights for targeted marketing strategies.

# Futurework

1) Enhanced Segmentation: Enrich the categories in segmentations further giving meaning to the "Others" segment potentially.
2) Additional Techniques like Customer Lifetime Value (CLV).
3) Additional Models: Compare other classification models such as Random Forest and Light Gradient Boosting models.
4) Time Series Analysis: Analyze customer behaviour trends over time
5) Dashboard: Create a user-friendly dashboard using Flask.

