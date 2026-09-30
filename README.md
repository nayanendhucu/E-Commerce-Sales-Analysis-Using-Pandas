# E-Commerce Sales Analysis Using Pandas

## Overview

This project demonstrates practical data analysis using Python and Pandas on an e-commerce sales dataset.

The analysis focuses on exploring product categories, prices, quantities, customer activity, regional performance, ratings, order dates, and sales trends. It demonstrates core Pandas techniques commonly used in exploratory data analysis and business analytics.

## Dataset

The project uses a local Excel dataset:

```text
pandas_task.xlsx
```

The dataset contains e-commerce order information including:

* Customer
* Category
* Price
* Quantity
* Region
* Rating
* OrderDate

The dataset was provided separately from the notebook.

## Objective

The main objective is to practice and demonstrate essential Pandas operations for analyzing structured sales data.

The project explores:

* Product categories
* Pricing
* Regional distribution
* Customer purchasing behavior
* Product ratings
* Order dates
* Total sales
* High-value orders
* Sales performance by category and region
* Sales trends over time

## Technologies Used

* Python
* Pandas
* Matplotlib
* Excel

## Analysis Workflow

```text
Excel Dataset
      |
Data Loading
      |
Initial Exploration
      |
Filtering and Conditional Analysis
      |
Feature Creation
      |
Date-Time Processing
      |
Grouping and Aggregation
      |
Sorting and Ranking
      |
Pivot Table Analysis
      |
Sales Trend Visualization
```

## Pandas Operations Demonstrated

### Data Exploration

The notebook performs basic dataset exploration using:

```python
df.head()
```

It also examines unique product categories and regional distributions.

### Conditional Filtering

Examples include identifying:

* Electronics products with ratings of 4 or above
* East-region orders above a specified price
* Orders with quantity of at least 3 or price below 100

### Sales Calculation

A total price column is created using:

```python
df['TOTAL PRICE'] = df['Quantity'] * df['Price']
```

This provides the total sales value for each order.

### Date-Time Analysis

Order dates are converted into Pandas datetime format:

```python
df['OrderDate'] = pd.to_datetime(df['OrderDate'])
```

The notebook extracts:

* Order month
* Weekday

This allows sales to be analyzed according to time-related patterns.

### Grouping and Aggregation

The project uses `groupby()` to analyze:

* Total sales by category
* Average rating by region
* Quantity purchased by customer
* Total sales by region
* Average customer order value
* Quantity by region and category

### Sorting and Ranking

The dataset is sorted to identify:

* Highest-value orders
* Top-rated products

### Pivot Table

A Pandas pivot table is created to compare total sales across categories and regions.

```python
pd.pivot_table(
    df,
    values='TOTAL PRICE',
    index='Category',
    columns='Region',
    aggfunc='sum'
)
```

### Sales Trend Visualization

Daily sales are plotted using Matplotlib to visualize changes in total sales over time.

## Key Analysis Questions

The notebook answers questions such as:

1. What product categories are present?
2. What is the average product price?
3. How many orders belong to each region?
4. Which Electronics products have high ratings?
5. Which East-region orders have prices above 1,000?
6. Which orders have high quantities or low prices?
7. Which category generates the highest total sales?
8. Which region generates the highest total sales?
9. Which customer purchased the highest quantity?
10. Which orders have the highest total value?
11. Which products have the highest ratings?
12. Which weekday generates the highest sales?
13. Which region-category combinations have the highest quantities?
14. What is the average total order value by customer?
15. Which customer appears most frequently in the dataset?

## Skills Demonstrated

* Python Data Analysis
* Pandas
* DataFrame Operations
* Conditional Filtering
* Boolean Indexing
* Feature Creation
* Date-Time Manipulation
* GroupBy Operations
* Aggregation
* Sorting
* Ranking
* Pivot Tables
* Matplotlib Visualization
* Basic Business Analysis

## Project Structure

```text
E-Commerce-Sales-Analysis-Pandas/
│
├── pandas_analysis.ipynb
├── pandas_task.xlsx
└── README.md
```

## Conclusion

This project demonstrates fundamental Pandas techniques through a practical e-commerce sales analysis workflow. It provides hands-on experience with data exploration, transformation, aggregation, customer analysis, regional analysis, time-based analysis, and basic visualization.

The project serves as a foundation for progressing toward more advanced data analysis projects involving larger datasets, statistical analysis, visualization dashboards, and predictive modeling.

## Author

**Nayanendhu CU**

GitHub: `nayanendhucu`

LinkedIn: `nayanendhu-unnikrishnan`
