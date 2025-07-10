# 🛒 Walmart Data Analysis

This is a guided end-to-end data analysis project using Walmart sales data. The goal is to preprocess raw sales data, clean it using Python, load it into MySQL, and perform detailed Exploratory Data Analysis (EDA) to uncover insights.

---

## 📁 Dataset Overview

- **Source**: [Kaggle - Walmart 10k Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
- **File Used**: `walmart_cleaned_dataset.csv`
- **Total Records**: 10,000+
- **Original Columns**:
  - `invoice_id`
  - `Branch`
  - `City`
  - `category`
  - `unit_price`
  - `quantity`
  - `date`
  - `time`
  - `payment_method`
  - `rating`
  - `profit_margin`
- **New Column Added**:
  - `Total_Amount = unit_price × quantity`

---

## 🧹 Data Cleaning (Python)

The dataset was cleaned using **Pandas**:
- Removed currency symbols (`$`) from `unit_price` and other relevant fields
- Converted `unit_price` and other columns to numeric format
- Converted `date` to `datetime` and `time` to `datetime.time`
- Converted `quantity` to integer after handling missing values
- Removed duplicates and handled missing data
- Created `Total_Amount` as a new field for transaction value

```python
# Example cleaning steps:
df['unit_price'] = df['unit_price'].replace(r'[\$,]', '', regex=True).astype(float)
df['quantity'] = df['quantity'].fillna(1).astype(int)
df['date'] = pd.to_datetime(df['date'], format='%d/%m/%y')
df['time'] = pd.to_datetime(df['time'], format='%H:%M:%S').dt.time
df['Total_Amount'] = df['unit_price'] * df['quantity']

🛠️ Tools Used
Python (Jupyter Notebook)
Pandas, Seaborn, Matplotlib
MySQL (Workbench)
Excel (preview/validation)
Git & GitHub (for version control)

