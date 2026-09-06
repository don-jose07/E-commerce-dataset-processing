# E-commerce Data Processing and Analysis

This repository contains a Jupyter Notebook that processes and analyzes e-commerce data from three distinct CSV files: `Orders.csv`, `Customers.csv`, and `Products.csv`.

## Project Overview

The main goal of this project is to create a clean, comprehensive, and meaningful dataset by integrating information from various sources and enriching it with new, derived features. The processed dataset is then exported for further analysis or reporting.

## Key Operations Performed

1.  **Data Loading**: All three datasets (`Orders`, `Customers`, `Products`) are loaded into pandas DataFrames.
2.  **Data Merging**: Related information is combined using `pd.merge()`:
    *   `Orders` and `Customers` are merged on `Customer_ID`.
    *   The resulting DataFrame is then merged with `Products` on `Product_ID`.
3.  **DateTime Operations**: The `Order_Date` column is converted to datetime objects, and several time-based features are extracted, including:
    *   `Order_Month`
    *   `Order_Day`
    *   `Order_DayOfWeek`
    *   `Order_Hour`
    *   `Order_Year`
4.  **Feature Engineering with `apply()`**: A new column, `Total_Price`, is calculated using `DataFrame.apply()` by multiplying `Quantity` and `Unit_Price` for each order item.
5.  **`concat()` Demonstration**: The notebook also includes a demonstration of `pd.concat()` to illustrate how DataFrames can be combined vertically.
6.  **Data Export**: The final processed and enriched dataset is exported to a new CSV file named `processed_ecommerce_dataset.csv`.

## Repository Contents

*   `Orders.csv`: Contains order-related information.
*   `Customers.csv`: Contains customer details.
*   `Products.csv`: Contains product details.
*   `processed_ecommerce_dataset.csv`: The final, integrated, and processed dataset (output).
*   `e-commerce_data_processing.ipynb`: The Jupyter Notebook containing all the code and analysis steps.
