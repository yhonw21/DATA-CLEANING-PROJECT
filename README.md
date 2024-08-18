# Data Cleaning Script for Layoffs Table (MySQL)

This script cleans and prepares a table named "layoffs" for further analysis. Here's a breakdown of the key steps:

## Duplicate Removal:

Creates a copy of the original table ("layoffs_staging").
Identifies duplicates based on specific columns (company, industry, etc.).
Creates a new table ("layoffs_staging2") and excludes duplicates.

## Data Standardization:

Trims leading/trailing spaces from text fields (e.g., company names).
Standardizes industry categories (e.g., "Cryptocurrency" to "Crypto").
Cleans and formats date entries for consistency.

## Handling Null Values:

Identifies rows with missing values in specific columns.
Uses existing data from the same company (if available) to fill null values in the "industry" field.
Optionally, you can choose to delete rows with significant null values (commented out in the script).

## Removing Unnecessary Column:

Drops the temporary "row_num" column added for duplicate identification.


*Note*: This script provides a basic framework for data cleaning. Depending on your specific data and analysis goals, you might need to adjust the logic and add further cleaning steps.
