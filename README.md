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

## 🛠️ Tools Used
- Python (Jupyter Notebook)
- Pandas, Seaborn, Matplotlib
- MySQL (Workbench)
- Excel (preview/validation)
- Git & GitHub (for version control)

## 📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is the process of analyzing and visualizing datasets to summarize their main characteristics, often using statistical graphics and plotting tools. EDA helps us understand patterns, detect anomalies, test hypotheses, and check assumptions.

In this project, EDA was performed using Python libraries like **Pandas**, **Seaborn**, and **Matplotlib** to uncover key insights from Walmart's sales data. The visualizations provided a deeper understanding of:

- **Revenue trends** across branches and product categories
- **Sales behavior** across different hours of the day
- **Customer preferences** for payment methods
- **Customer satisfaction** through average ratings
- **Correlations** between unit price, quantity, profit, and ratings

### Key EDA Objectives:
- Identify the branch with the highest revenue
- Analyze which product categories are most popular and profitable
- Examine peak shopping hours to understand customer buying patterns
- Study the relationship between quantity, pricing, and profit margin
- Visualize customer ratings by product category to evaluate satisfaction

These insights are critical for understanding business performance and can assist Walmart in making data-driven decisions for marketing, inventory management, and customer experience optimization.


