# Walmart Sales Capstone Project

This project analyzes Walmart sales data to understand store performance, seasonal patterns, and the impact of holidays, temperature, fuel prices, CPI, and unemployment on weekly sales.

## Project Overview

The notebook `Capstone_Project_(Walmart).ipynb` explores the Walmart sales dataset and performs data cleaning, exploratory data analysis, and time-based sales analysis for individual stores.

The objective is to answer questions such as:

- Which stores perform best?
- How does holiday sales differ from regular weeks?
- What are the relationships between sales and external factors?
- How do sales change over time for a selected store?

## Dataset

The project uses a Walmart sales dataset with weekly sales records across multiple stores.

Columns in the dataset:

- Store
- Date
- Weekly_Sales
- Holiday_Flag
- Temperature
- Fuel_Price
- CPI
- Unemployment

## Notebook Contents

The notebook includes:

- Loading and inspecting the dataset
- Checking for missing values
- Converting the `Date` column to datetime format
- Setting `Date` as the index for time series analysis
- Selecting a specific store by ID
- Grouping and viewing weekly sales records
- Visual and exploratory analysis of sales trends

## How to Run

### In Google Colab

1. Upload the dataset file to your Colab environment.
2. Make sure the file is named:
   `Walmart DataSet.csv`
3. Update the loading cell if necessary:

```python
import pandas as pd

df = pd.read_csv('/content/Walmart DataSet.csv')
```

4. Run the notebook cells in order.

## Example Analysis

The notebook includes logic to select a store by ID and inspect its weekly sales:

```python
a = int(input("Enter the store id:"))
store = df[df.Store == a]
sales = pd.DataFrame(store.Weekly_Sales.groupby(store.index).sum())
```

This allows the user to analyze any store from 1 to 45.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## Project Goals

- Clean and prepare the dataset
- Analyze the effect of business and external variables on revenue
- Build insight-driven understanding of sales behavior
- Provide a capstone-style exploratory data analysis project

## Notes

This project is intended as a learning and analysis exercise. It focuses on data exploration and business insight generation rather than deployment or production systems.

## Repository Structure

```text
.
├── Capstone_Project_(Walmart).ipynb
├── Walmart DataSet.csv
├── README.md
```

## Future Improvements

Possible extensions for this project include:

- Building a predictive sales model
- Comparing stores using statistical summaries
- Adding time series forecasting
- Creating dashboards for business reporting
- Automating report generation

## License

This project is for educational and portfolio use.
