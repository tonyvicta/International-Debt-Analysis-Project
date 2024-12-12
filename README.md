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

....'

SELECT COUNT(DISTINCT country_name) AS total_distinct_countries
FROM international_debt;

.....















