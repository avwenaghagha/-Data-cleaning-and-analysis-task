# -Data-cleaning-and-analysis-task
MINI PROJECT
# Data Analysis Project - Sales Data

## Overview

This project analyzes sales data from a fictional company selling various products. The data includes information on sales transactions, product details, regions, and customer ratings. The analysis aims to provide insights into sales performance, regional trends, and data quality.

## Data Source

The data is stored in the `combined_analysis.xlsx` file, which contains the following sheets:

*   **Cleaned Data:** This sheet contains the cleaned and processed sales data, ready for analysis.
*   **Cleaning Steps:** This sheet documents the data cleaning steps performed to ensure data quality.
*   **Regional Analysis:** This sheet presents a summary of sales performance by region.
*   **Omitted Data:** This sheet lists the data points that were omitted or modified during the cleaning process, along with the reasons for the changes.

## Data Dictionary

### Cleaned Data Sheet

| Column Name           | Description                                                                  |
| --------------------- | ---------------------------------------------------------------------------- |
| Date                  | Date of the sales transaction (MM/DD/YY).                                    |
| ID                    | Unique identifier for each transaction.                                      |
| Name                  | Name of the customer.                                                        |
| Region                | Region where the sale occurred (North, East, West, South, Asgard).           |
| Rating                | Customer rating of the product/service (e.g., Good, Excellent, Average, Poor, Mischief, Worthy, Spy, Leader). |
| Product               | Name of the product sold.                                                    |
| Quantity              | Quantity of the product sold in the transaction.                             |
| Price Per Unit        | Price of each unit of the product (in USD).                                  |
| Price Per Unit Original | Original price of each unit of the product (in USD), before cleaning.       |
| Name Original         | Original name of the customer, before cleaning.                                |
| Total Value           | Total value of the transaction (Quantity \* Price Per Unit).                 |

## Data Cleaning Steps

The following data cleaning steps were performed to ensure data quality:

1.  **Removed duplicate ID entries:** Duplicate rows based on the `ID` column were removed to ensure each transaction is unique.
2.  **Cleaned Price Per Unit column:**
    *   Removed `$` signs from the `Price Per Unit` and 'Price Per Unit Original' columns.
    *   Converted the column to a numeric data type.
    *   Replaced `"inf"` values (representing infinity due to division by zero) with `NaN` (Not a Number) to handle missing or invalid price data.
3.  **Cleaned Name column:** Removed extra spaces from customer names to ensure consistency.
4.  **Added Total Value column:** Calculated the `Total Value` for each transaction by multiplying the `Quantity` by the `Price Per Unit`.

## Regional Analysis Summary

The `Regional Analysis` sheet provides a summary of sales performance by region. The key metrics include:

*   **Region:** The region where the sales occurred.
*   **Number of Products:** The number of unique products sold in each region.
*   **Total Quantity:** The total quantity of products sold in each region.
*   **Average Price:** The average price of products sold in each region.
*   **Total Sales Value:** The total sales value for each region.

*Key Findings:*

*   South region has the highest Total Sales Value (8049.9) and the highest Total Quantity (295)
*   North region has the lowest Total Sales Value (2399.85) and the lowest Total Quantity (105)

## Data Omission

During the cleaning process, certain data points were omitted or modified. Details of these changes are recorded in the `Omitted Data` sheet, including the reason for the omission and the action taken. Reasons for data omission include:

*   Duplicate ID
*   Invalid Price ("inf")
*   Name Formatting (Extra Spaces)

## Usage

This data and analysis can be used to:

*   Understand sales trends and patterns.
*   Identify top-performing regions and products.
*   Assess the impact of data quality issues on analysis results.


