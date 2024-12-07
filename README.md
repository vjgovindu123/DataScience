# Comprehensive Data Analysis with Pandas, NumPy, and Python

## Objective
This project performs in-depth data analysis on an e-commerce dataset to extract actionable insights. It uses **Pandas**, **NumPy**, **custom Python functions**, and **visualization tools** to achieve the objectives outlined below.

---

## Dataset
The project uses the `ecommerce_data_advanced.csv` file with the following structure:

# ecommerce_data_advanced.csv

| OrderID | Product         | Category     | Price | Quantity | CustomerID | OrderDate   | Rating | Discount | City          | Country | ReturnStatus | PaymentMethod |
|---------|-----------------|--------------|-------|----------|------------|-------------|--------|----------|---------------|---------|--------------|---------------|
| 1       | Laptop          | Electronics  | 800   | 1        | 1001       | 2024-10-01  | 4.5    | 0.10     | New York      | USA     | Returned     | Credit Card   |
| 2       | Phone           | Electronics  | 500   | 2        | 1002       | 2024-10-03  | 4.2    | 0.15     | Los Angeles   | USA     | Completed    | PayPal        |
| 3       | Chair           | Furniture    | 150   | 3        | 1003       | 2024-10-10  | 4.0    | 0.05     | Toronto       | Canada  | Completed    | Debit Card    |
| 4       | Headphones      | Electronics  | 100   | 4        | 1004       | 2024-10-12  | 3.8    | 0.20     | New York      | USA     | Returned     | Credit Card   |
| 5       | Desk            | Furniture    | 200   | 1        | 1005       | 2024-10-15  | 4.7    | 0.10     | London        | UK      | Completed    | Credit Card   |
| 6       | Gaming Console  | Electronics  | 300   | 1        | 1006       | 2024-10-20  | 4.6    | 0.05     | Chicago       | USA     | Completed    | PayPal        |
| 7       | Sofa            | Furniture    | 500   | 2        | 1007       | 2024-10-25  | 4.4    | 0.15     | Toronto       | Canada  | Completed    | Debit Card    |

## Key Tasks

### 1. Data Preparation
- **Load the dataset** and convert date columns to datetime format.
- Handle missing data:
  - Drop rows with more than 2 missing values.
  - Fill numerical columns using interpolation.
  - Replace missing categorical values with `"Unknown"`.

### 2. Advanced Data Transformations
- **EffectivePrice Calculation:**  
  `EffectivePrice = Price × Quantity × (1 − Discount)`
- **CustomerType Classification:**
  - `Premium`: EffectivePrice > 1000
  - `Standard`: EffectivePrice between 500-1000
  - `Economy`: EffectivePrice < 500

### 3. Data Insights and Queries
- Total revenue, average rating, and unique customers per **Category**.
- City with the **highest total revenue**.
- Products with ratings **below their category average**.
- Total refund amount for **Returned orders**.

### 4. Advanced Analysis with NumPy
- **Moving Average:** Add a `PriceMovingAvg` column using a window size of 3.
- **Simulate Inflation:** Apply 5% inflation to product prices and store as `InflatedPrice`.

### 5. Custom Functions
- `simulate_discount(discount)`:
  - Simulates a new `EffectivePrice` with the given discount.
  - Returns the top 3 products with the highest simulated prices.
- `analyze_customer(customer_id)`:
  - Returns:
    - Number of orders.
    - Total spending.
    - Percentage of returned orders.

### 6. Visualization
- **Line Plot:** Revenue trends over time.
- **Heatmap:** Revenue contributions by **City** and **Category**.
- **Histogram:** Distribution of product ratings.

### 7. Export
- Save the final dataset as `ecommerce_final.csv`.
- Generate a `summary.txt` file containing:
  - Total revenue.
  - Number of orders.
  - Most frequently used payment method.

---

## Outputs
### Transformed Dataset
File: `ecommerce_final.csv`

### Summary File
File: `summary.txt`

Content:
- Total revenue.
- Total number of orders.
- Most frequently used payment method.

### Visualizations
- Line plot for revenue trends.
- Heatmap for city/category revenue contributions.
- Histogram of product ratings.

---

## Requirements
- Python 3.9 or higher
- Libraries:
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn

### Installation
Install the required libraries using:
```bash
pip install pandas numpy matplotlib seaborn
