# Sales & Customer Insights

## Project Overview

This project involved analysing sales and customer data in Power BI to examine brand profitability, sales performance, and customer purchasing behaviour. I used Power Query to work with the data and developed dashboard visuals to present key performance indicators and explore differences across brands, customer groups, and purchasing categories.

The dashboards present key performance indicators and comparisons of brand profitability, monthly customer counts, and purchasing patterns by product colour and customer income level. The analysis highlights Apple's profit contribution and the share of purchase value attributed to white products, while providing a basis for exploring customer activity over the reporting period.

The project demonstrates my approach to turning sales data into visual analysis and communicating findings that can help a business identify areas for further investigation.

## Business Problem

Understanding sales performance requires more than looking at total revenue. Businesses also need to examine which brands contribute most to profitability, how customer activity changes over time, and how purchasing patterns differ across product categories and customer groups.

This project explores these areas through Power BI visualisations, using sales, cost, profit, and customer-related metrics to highlight differences in performance. The analysis provides a clearer view of the available data and identifies areas that may warrant further investigation.

## Project Objectives

The objectives of this project were to:

- Evaluate overall sales performance using revenue, cost, and profit metrics.
- Compare profitability and revenue contribution across brands.
- Examine monthly customer counts to identify differences in customer activity.
- Analyse purchasing patterns by product colour and customer income level.
- Present key performance indicators and visual comparisons in Power BI.
- Document key insights from the analysis to highlight notable patterns and areas for further investigation.

## Tools and Technologies

- **Microsoft Power BI:** Used to develop the sales and customer dashboards, present key performance indicators, and visualise sales, profitability, and customer performance.
- **Power Query:** Used to inspect data quality and distribution, filter rows, and standardise text capitalisation during data preparation.

 ## Data Preparation

I used Power Query to inspect the dataset before building the dashboards. My preparation work included reviewing column quality and data distribution, filtering out a row containing missing data, and standardising text capitalisation in fields such as region and gender.

For example, I changed `north` to `North` and `female` to `Female` to make the text values more consistent.

The data preparation was relatively limited, so the focus of the project was on presenting the available sales and customer data through visualisations and identifying meaningful patterns in the results.

## Dataset Overview

The project uses three tables: Customers, Products, and Sales. Together, these tables provide information about customer characteristics, product attributes, and sales transactions for the January–March 2023 reporting period.

### Customers

The Customers table contains customer identifiers, names, region, age, gender, income level, and signup date. These fields support analysis of customer counts and comparisons across customer groups.

### Products

The Products table contains product identifiers, product names, categories, brands, colours, and weights. These fields support comparisons of brand profitability and analysis of purchasing value by colour and product category.

### Sales

The Sales table contains sales identifiers, product and customer identifiers, quantity, sale date, sales amount, and unit cost. These fields support the analysis of sales performance, costs, and profitability.

## DAX Measures and Calculations

I created DAX calculations in Power BI to derive the financial and customer metrics used in the dashboard. These calculations supported the analysis of sales revenue, cost of goods sold, profit, customer counts, and sales activity.

### 1. Revenue

Calculates revenue by multiplying the sales amount by the quantity recorded.

```dax
Revenue = Sales[SalesAmount] * Sales[Quantity]
```

### 2. Total Sales Revenue

Aggregates revenue across the sales records.

```dax
Total Sales(rev) = SUM(Sales[Revenue])
```

### 3. Cost of Goods Sold (COGS)

Calculates the cost associated with each sales record using unit cost and quantity.

```dax
COGS = Sales[Unit Cost] * Sales[Quantity]
```

### 4. Total COGS

Calculates the total cost of goods sold.

```dax
Total COGS = SUM(Sales[COGS])
```

### 5. Profit

Calculates profit by subtracting total cost of goods sold from total sales revenue.

```dax
Profit = [Total Sales(rev)] - [Total COGS]
```

### 6. Total Customers

Counts distinct customer IDs to determine the number of unique customers.

```dax
Total Customers = DISTINCTCOUNT(Customers[CustomerID])
```

### 7. Total Order

Counts the rows in the Sales table.

```dax
Total Order = COUNTROWS(Sales)
```
## Dashboard Analysis

### 1. Sales Overview
![Sales Overview Dashboard](assets/sales-customr-sales-overview.%20jpg.png)

This dashboard brings together sales and profitability metrics to examine financial performance across the business. I used KPI cards to present total sales, total cost, profit, and customer count, providing a high-level view of the results before examining differences across brands.

The brand-level visuals compare revenue and profit across Apple, Lenovo, Samsung, HP, Asus, and Dell. These comparisons help show how financial contribution differs between brands and provide context for the key insights recorded in the dashboard.

### 2. Customer Overview
![Customer Overview Dashboard](assets/sales-customer-overview.%20jpg.png)

This dashboard focuses on customer activity and purchasing behaviour during the January–March 2023 reporting period. I used visualisations to examine monthly customer counts, compare purchasing value across product colours, and explore profit across different customer income levels.

The monthly customer analysis highlights changes in customer activity over the period, while the colour and income-level visuals provide additional perspectives on purchasing patterns. I also documented key observations in the dashboard's Key Insights panel, including the share of purchase value attributed to white products and the month with the lowest customer count.

## Key Findings

- **Brand profitability:** Apple recorded the highest profit among the brands analysed, at approximately 197K.

- **Purchasing patterns by colour:** White products accounted for 39.22% of total purchase value, representing a notable share of purchasing activity.

These findings highlight differences in brand profitability and purchasing patterns within the dataset.

## Recommendations

- **Review brand profitability:** Investigate the factors contributing to Apple's higher profit to better understand the differences in profitability across brands.
- **Explore purchasing patterns:** Examine why white products account for a substantial share of total purchase value and whether this pattern varies across product categories.
- **Analyse a longer reporting period:** Include additional months of data to determine whether the observed sales and purchasing patterns remain consistent over time.

## Limitations and Considerations

- **Limited reporting period:** The analysis covers January to March 2023. A longer reporting period would be needed to assess whether the observed patterns persist over time or reflect seasonal changes.
- **Descriptive analysis:** The dashboards highlight differences in sales, profitability, and purchasing behaviour but do not establish the reasons behind those differences.
- **Scope of customer analysis:** The customer insights are based on the available customer attributes and sales data. Additional information could help explain purchasing decisions and differences between customer groups.
- **Profitability interpretation:** The profit calculation is based on the revenue and cost fields used in the project. It should not be interpreted as overall business net profit without considering other operating expenses.

## Skills Demonstrated

- **Data preparation:** Used Power Query to inspect data quality, review column distributions, filter rows, and standardise text values.
- **Data modelling and calculations:** Worked with customer, product, and sales tables and created DAX calculated columns and measures for revenue, cost, profit, customer count, and sales record count.
- **Dashboard development:** Built Power BI dashboards using KPI cards and visualisations to compare sales performance, brand profitability, and customer purchasing behaviour.
- **Data analysis:** Identified patterns in brand profitability and purchasing value across product colours.
- **Insight communication:** Documented key observations in the dashboard's Key Insights panel and translated the findings into recommendations for further investigation.
  
## Project Files

The project repository contains the Power BI report and supporting dashboard screenshots used to present the analysis.

- **Power BI report (.pbix):** Contains the data model, Power Query preparation steps, DAX calculations, and dashboard visualisations.
- **Dashboard screenshots:** Provide a preview of the Sales Overview and Customer Overview dashboards.

## Conclusion

This project gave me practical experience using Power Query to prepare data and Power BI to analyse sales performance, brand profitability, and customer purchasing behaviour. By creating two dashboards and documenting key findings, I practised presenting business metrics in a visual format and identifying patterns that may support further investigation.

The project also strengthened my ability to communicate analytical findings clearly, connecting dashboard visuals to observations rather than presenting figures without context.



  
