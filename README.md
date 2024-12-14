# International-Debt-Analysis-Project

[![Everything Is AWESOME](https://img.youtube.com/vi/StTqXEQ2l-Y/0.jpg)](https://www.youtube.com/watch?v=StTqXEQ2l-Y "Everything Is AWESOME")

[![Report](https://img.youtube.com/vi/StTqXEQ2l-Y/0.jpg)](https://youtu.be/StTqXEQ2l-Y?si=QcOVBMMvl1hUjsd2 "Report")

# Table of contents 

- [Project Overview](#Project-Overview)
- [Dataset Description](#Dataset-Description)
- [Objectives](#Objectives)
- [SQL Queries and Results](#SQL-Queries-and-Results)
- [Project Structure](#Project-Structure)
- [Tools & Technologies](#Tools-&-Technologies)
- [Deliverables](#Deliverables)
- [How to Run](#How-to-Run)
- [Employment Search Purpose](#Employment-Search-Purpose)
- [Contribution Guidelines](#Contribution-Guidelines)
- [License](#License)

  
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

### Workflow

1. Data Loading: Load the dataset into a database management system (DBMS).

2. Exploratory Analysis: Perform initial exploration to understand data quality.

3. Query Execution: Write SQL queries to extract relevant insights.

4. Reporting & Visualization: Summarize findings and create visual representations.

## Tools & Technologies

- Database Management System: PostgreSQL / MySQL / SQLite

- Query Language: SQL

- Data Visualization: Power BI / Tableau / Excel (optional)

## Deliverables

- SQL scripts answering the project questions

- Analysis summary report

- Relevant visualizations (if applicable)

## How to Run

1. Clone the repository.

2. Set up the database and import the dataset.

3. Execute the provided SQL queries.

4. Review the output and reports.


## Employment Search Purpose

This project serves as a practical demonstration of my technical skills in data querying, financial analysis, and database management. It highlights my ability to extract actionable insights from complex datasets—skills highly relevant for data analyst and financial crime roles.

## Contribution Guidelines

- Fork the repository.

- Create a feature branch.

- Commit changes with clear messages.

- Submit a pull request.

## License

This project is licensed under the MIT License.



Disclaimer: This project is for educational and professional portfolio purposes, leveraging data provided by The World Bank.
