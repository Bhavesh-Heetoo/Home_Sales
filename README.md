# Home_Sales
Module 22 Challenge

# Module 22 Challenge

## Overview
This project analyzes home sales data using **PySpark and SparkSQL**. It involves reading data from an AWS S3 bucket, creating temporary tables, running queries, caching tables, partitioning data, and comparing query execution times.

## Steps Performed
1. **Load Data**: Read `home_sales_revised.csv` into a PySpark DataFrame.
2. **Create Temporary Table**: Register the DataFrame as `home_sales`.
3. **Run SQL Queries**:
   - Average price of four-bedroom homes by year.
   - Average price of three-bedroom, three-bathroom homes by year built.
   - Average price of homes with specific conditions (size, floors, etc.).
   - Average price per view rating (filtered for prices ≥ $350,000).
4. **Cache Table & Measure Performance**: Compare cached vs. uncached query times.
5. **Partition & Save as Parquet**: Store data partitioned by `date_built`.
6. **Re-run Queries on Parquet Data**: Measure performance impact.
7. **Uncache Table**: Verify successful uncaching.

## Key Findings
- **Caching significantly reduces query execution time**.
- **Parquet performance depends on dataset size and partition filtering**.
- **Filtering by `date_built` improves partitioned query performance**.

## How to Run
1. Clone the repository.
2. Open `Home_Sales.ipynb` in Google Colab.
3. Run cells sequentially to execute the analysis.
4. Compare performance metrics before and after caching/partitioning.

