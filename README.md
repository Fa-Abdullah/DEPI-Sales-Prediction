# DEPI Sales Prediction – 8 ML Models + EDA + Feature Engineering

Full sales prediction pipeline (Regression) using 8 different models with comprehensive EDA and feature engineering.

## 📊 Dataset

- Sales dataset (Excel)
- Features: Orders, Products, Customers, Dates, Sales, Profit, Discount
- Target: `Sales` (log‑transformed)

## 🧹 Preprocessing

- Handle missing values (median for numeric, mode for categorical)
- Drop unnecessary columns (IDs, Names, Dates)
- One‑Hot Encoding for categorical variables
- Log transformation (`log1p`) for Sales (reduces skewness)

## 📈 Exploratory Analysis

- Sales distribution (before & after log)
- Missing values heatmap
- Correlation heatmap
- Average Sales by Category
- Average Profit by Segment
- Profit boxplot (outlier check)

## ⚙️ Feature Engineering

- **Profit Margin** = Profit / Sales
- **Sales_log** = log1p(Sales)

## 🤖 Models (8 total)

1. Linear Regression
2. XGBoost (tuned)
3. Decision Tree
4. Random Forest
5. KNN
6. SVM
7. Ridge Regression (with Polynomial Features)
8. Lasso Regression (with Polynomial Features)

