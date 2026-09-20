# DEPI Sales Prediction – XGBoost + EDA + Feature Engineering

A sales prediction pipeline built around a tuned XGBoost regressor on a retail sales dataset, with full exploratory data analysis and feature engineering.

## Dataset

- Source: Sales Dataset (Excel file)
- Original shape: 9,994 rows × 21 columns
- Target variable: Sales
- Features: Orders, Products, Customers, Dates, Sales, Profit, Discount

## Preprocessing

- Missing values: median for numeric columns, mode for categorical columns
- Dropped columns: Row ID, Order ID, Customer ID, Customer Name, Product ID, Product Name, Order Date, Ship Date
- One-Hot Encoding for categorical variables
- Log transformation (log1p) applied to Sales to reduce skewness
- RobustScaler applied to features before training

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

## Model

**XGBoost Regressor** (tuned), trained on the log-transformed target:
- n_estimators=1500, learning_rate=0.01, max_depth=4
- min_child_weight=5, subsample=0.7, colsample_bytree=0.7
- reg_alpha=1, reg_lambda=5

## Results

| Metric | Train | Test |
|--------|------:|-----:|
| RMSE | 0.1572 | 0.1948 |
| R² | 99.02% | **98.51%** |

## Technologies

- Python
- XGBoost
- Scikit-learn
- Pandas / NumPy
- Matplotlib / Seaborn

## How to Run

1. Clone the repository
2. Install requirements: pip install -r requirements.txt
3. Place the Sales Dataset (Excel file) in the same directory
4. Run the notebook in Jupyter or Google Colab

## Author
**Fatma Abdullah**
