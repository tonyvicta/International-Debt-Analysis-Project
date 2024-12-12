# International-Debt-Analysis-Project

## Project Overview

I developed this project to showcase my proficiency in SQL and data analysis, focusing on international debt data collected by The World Bank. The dataset includes information about the amount of debt (in USD) owed by developing countries across various categories. Through SQL-based analysis, I explored global debt patterns, answered critical financial questions, and produced actionable insights.


## Dataset Description

Table Name: international_debt


| Column Name     | Description                            | Data Type |
|-----------------|----------------------------------------|-----------|
| `country_name`  | Name of the country                    | varchar   |
| `country_code`  | Code representing the country          | varchar   |
| `indicator_name`| Description of the debt indicator      | varchar   |
| `indicator_code`| Code representing the debt indicator   | varchar   |
| `debt`          | Value of the debt indicator (in USD)   | float     |


## Objectives

I conducted this project to demonstrate SQL query writing, data extraction, and analysis skills essential for data-driven decision-making in financial and business contexts. Key questions addressed include:


1. Distinct Countries: How many distinct countries are present in the dataset?

2. Highest Debt Country: Which country has the highest amount of debt?

3. Lowest Repayments: Which country has the lowest amount of repayments?
 
## SQL Queries and Results


### 1. Count Distinct Countries

```sql

SELECT COUNT(DISTINCT country_name) AS total_distinct_countries
FROM international_debt;

```
Result: 124 distinct countries


### 2. Country with the Highest Debt

```sql

SELECT country_name, SUM(debt) AS total_debt
FROM international_debt
GROUP BY country_name
ORDER BY total_debt DESC
LIMIT 1;

```

Result: Country: China, Total Debt: $285,793,494,734.2


### 3. Country with the Lowest Repayments

```sql

SELECT 
    country_name, 
	indicator_name,
	MIN(debt) AS lowest_repayment
FROM international_debt
WHERE indicator_code='DT.AMT.DLXF.CD'
GROUP BY country_name, indicator_name
ORDER BY lowest_repayment
LIMIT 1;

```

Result: Country: Timor-Leste, Total Repayments: $825,000


## Project Structure

### Repository Organization


international-debt-analysis/
├── data/          # Contains the dataset (CSV/SQL dump if applicable)
├── notebooks/     # SQL scripts or notebooks for analysis
├── reports/       # Analysis summaries and visualizations
├── docs/          # Documentation files
├── README.md      # Project overview
└── LICENSE        # Project license



