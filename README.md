# DEPI Sales Prediction – 8 ML Models + EDA + Feature Engineering

Sales prediction pipeline using 8 regression models on a retail sales dataset.

## Dataset

- Source: Sales Dataset (Excel file)
- Target variable: Sales
- Features: Orders, Products, Customers, Dates, Sales, Profit, Discount

## Preprocessing

- Missing values: median for numeric columns, mode for categorical columns
- Dropped columns: Row ID, Order ID, Customer ID, Customer Name, Product ID, Product Name, Order Date, Ship Date
- One-Hot Encoding for categorical variables
- Log transformation (log1p) applied to Sales to reduce skewness

## Feature Engineering

- Profit Margin = Profit / Sales
- Sales_log = log1p(Sales)

## Exploratory Data Analysis

- Sales distribution before and after log transformation
- Missing values heatmap
- Correlation heatmap
- Average sales by category
- Average profit by segment
- Profit boxplot for outlier detection

## Models

1. Linear Regression
2. XGBoost (tuned)
3. Decision Tree
4. Random Forest
5. KNN
6. SVM
7. Ridge Regression with Polynomial Features
8. Lasso Regression with Polynomial Features


