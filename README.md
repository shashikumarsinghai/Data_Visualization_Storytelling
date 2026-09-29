# Advanced Data Visualization and Storytelling with Python

## Project Overview

This project explores the Superstore sales dataset using Python-based data analysis and visualization techniques.

The main goal is to transform transaction-level business data into a coherent visual story that can be understood by both technical and non-technical audiences.

The analysis examines business performance from multiple perspectives, including:

- Monthly sales and profit trends
- Product category performance
- Regional performance
- Transaction-level sales and profit relationships
- Profit distribution across categories
- Category and region profitability patterns

The project demonstrates how carefully selected visualizations can reveal patterns that may not be immediately visible from raw data or summary tables.

---

## Objectives

The main objectives of this project are:

- Analyze the Superstore dataset using Python.
- Prepare and clean the transaction data for visualization.
- Examine sales and profit trends over time.
- Compare sales, profit, and profit margins across product categories.
- Analyze regional differences in sales and profitability.
- Explore the relationship between transaction-level sales and profit.
- Examine the distribution of profit across product categories.
- Identify important category-region profitability patterns.
- Build a coherent visual narrative for a non-technical audience.
- Discuss potential business implications of the findings.

---

## Dataset

The project uses the **Superstore sales dataset**, which contains transaction-level information about customer orders, products, sales, quantities, discounts, and profits.

The original CSV contains 10,800 rows and 21 columns.

During data preparation, the dataset was found to contain a main transaction table followed by an appended returns-related section. For the business-performance analysis, the main transaction records were isolated, resulting in **9,994 transaction rows**.

The main variables used include:

- Order Date
- Ship Date
- Ship Mode
- Customer ID
- Customer Name
- Segment
- Country
- City
- State
- Region
- Product ID
- Category
- Sub-Category
- Product Name
- Sales
- Quantity
- Discount
- Profit

The transaction data covers orders from **January 2015 through December 2018**.

### Dataset Source

The Superstore dataset is publicly available and was obtained from a public GitHub dataset repository:

https://github.com/leonism/sample-superstore

---

## Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Plotly**
- **Jupyter Notebook**
- **VS Code**

---

## Data Preparation

The following preparation steps were performed:

1. Loaded the dataset using Pandas.
2. Inspected the dataset dimensions and column structure.
3. Identified the appended returns-related section.
4. Isolated the 9,994 main transaction records.
5. Checked for duplicate transaction rows.
6. Converted `Order Date` and `Ship Date` to datetime format.
7. Checked missing values.
8. Retained 11 missing `Postal Code` values because postal code was not required for the planned visual analysis.
9. Created time-based columns including:
   - Year
   - Month
   - Month Name
   - Year-Month
10. Created aggregated datasets for category and regional analysis.

---

## Overall Dataset Metrics

The cleaned transaction dataset contains:

| Metric | Value |
|---|---:|
| Total Sales | $2,297,200.86 |
| Total Profit | $286,397.02 |
| Total Quantity | 37,873 |
| Unique Orders | 5,009 |
| Transaction Rows | 9,994 |

---

## Visualizations

The project contains six final visualizations.

### 1. Monthly Sales and Profit Trend

File:

`visualizations/01_monthly_sales_profit_trend.png`

This visualization examines monthly sales and profit from 2015 through 2018.

A line chart was selected because the data represents an ordered time series. The visualization highlights fluctuations in business performance and demonstrates that sales and profit do not always move proportionally.

---

### 2. Category Performance

File:

`visualizations/02_category_performance.png`

This visualization compares:

- Sales
- Total Profit
- Profit Margin

across Technology, Furniture, and Office Supplies.

The analysis shows that Technology generates the highest total sales and profit, while Furniture generates substantial sales but has a considerably lower profit margin.

---

### 3. Regional Performance

File:

`visualizations/03_regional_performance.png`

This visualization compares:

- Sales by region
- Profit margin by region

across West, East, Central, and South.

The comparison demonstrates that regional sales volume does not necessarily correspond to regional profitability.

---

### 4. Sales vs Profit

File:

`visualizations/04_sales_vs_profit.png`

This scatter plot examines the relationship between transaction-level sales and profit.

Product categories are represented using different colors, while a regression line summarizes the overall direction of the relationship.

The visualization shows an overall positive association between sales and profit, while also revealing substantial variation and loss-making transactions.

---

### 5. Profit Distribution by Category

File:

`visualizations/05_profit_distribution_by_category.png`

This box plot examines transaction-level profit distributions across product categories.

The visualization helps compare the typical range and variation of profit between categories. Extreme outliers are omitted from the final display for readability while remaining part of the underlying dataset.

---

### 6. Category and Region Profitability

File:

`visualizations/06_category_region_profit.png`

This heatmap combines product category and geographical region to examine total profit across category-region combinations.

The visualization reveals that Furniture has greater regional variation and records negative total profit in the Central region.

---

## Key Findings

The analysis produced several important findings:

1. Monthly sales and profit fluctuate considerably throughout the 2015–2018 period.

2. Technology generates approximately **$836,154 in sales** and **$145,455 in profit**, with a profit margin of **17.40%**.

3. Furniture generates approximately **$741,999 in sales** but only **$18,451 in profit**, resulting in a profit margin of approximately **2.49%**.

4. The Central region generates more sales than the South region but has a lower profit margin:
   - Central: **7.92%**
   - South: **11.93%**

5. Transaction-level sales and profit show an overall positive association, but considerable variation exists between individual transactions.

6. The dataset contains both profitable and loss-making transactions.

7. Furniture in the Central region records approximately **-$2,871 in total profit**, making it the only negative category-region combination identified in the analysis.

---

## Business Implications

The findings suggest several areas that could be investigated further:

- Evaluate profitability alongside sales volume.
- Investigate the relatively low profitability of the Furniture category.
- Examine regional differences in profit margins.
- Investigate transactions producing negative profit.
- Analyze category-region combinations with unusually low profitability.
- Explore the possible influence of discounts, sub-categories, products, shipping characteristics, and other transaction attributes.

These observations identify areas for further investigation rather than establishing causal explanations.

---

## Project Structure

```text
Data_Visualization_Storytelling/
│
├── data/
│   └── superstore.csv
│
├── notebooks/
│   └── Data_Storytelling.ipynb
│
├── visualizations/
│   ├── 01_monthly_sales_profit_trend.png
│   ├── 02_category_performance.png
│   ├── 03_regional_performance.png
│   ├── 04_sales_vs_profit.png
│   ├── 05_profit_distribution_by_category.png
│   └── 06_category_region_profit.png
│
├── report/
│
├── .gitignore
├── README.md
└── requirements.txt
```

# How to Run the Project

## 1. Clone the Repository

```
git clone <repository-url>
```

## 2. Navigate to the Project


```
cd Data_Visualization_Storytelling
```

## 3. Create a Virtual Environment

```
python -m venv .venv
```

## 4. Activate the Environment

### Windows PowerShell

```
.venv\Scripts\Activate.ps1
```

## 5. Install Dependencies

```
pip install -r requirements.txt
```

## 6. Open the Notebook

Open:

```
notebooks/Data_Storytelling.ipynb
```

Run the notebook cells in order.

---

# Limitations

-  The analysis is descriptive and does not establish causal relationships. 
-  The dataset contains an appended returns-related section that was excluded from the main transaction analysis. 
-  Eleven missing Postal Code values were retained because postal code was not required for the planned visualizations. 
-  The analysis focuses primarily on sales and profit. 
-  The underlying causes of profitability differences were not investigated in detail. 
-  Extreme transaction-level observations were omitted from the final box-plot display for readability. 
-  Additional analysis of discounts, sub-categories, products, customers, and shipping characteristics could provide deeper insights. 

---

# Conclusion

This project demonstrates how Python-based data visualization can transform raw transaction data into a coherent visual narrative.

By combining time-series analysis, categorical comparisons, regional analysis, scatter plots, distribution analysis, and heatmaps, the project provides multiple perspectives on sales and profitability.

The analysis demonstrates that sales volume alone does not provide a complete picture of business performance.

Examining profit, profit margins, transaction-level variation, and category-region combinations provides additional context for understanding business performance and identifying areas for further investigation.

---

# Future Improvements

Potential future improvements include:

-  Interactive dashboards using Plotly. 
-  Deeper sub-category analysis. 
-  Product-level profitability analysis. 
-  Discount and profitability analysis. 
-  Customer segment analysis. 
-  Shipping and delivery analysis. 
-  Interactive filtering by region and category. 
-  Additional statistical analysis. 
-  Automated report generation. 

---

# License

This project is created for educational and internship purposes.


```