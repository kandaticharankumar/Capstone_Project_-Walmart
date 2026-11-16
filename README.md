# Walmart Retail Sales Time-Series & Macroeconomic Impact Analysis

An end-to-end exploratory data analysis (EDA) and time-series decomposition project evaluating **6,435 weekly sales records across 45 Walmart retail stores**, examining store-level seasonality and macroeconomic sensitivity (`Unemployment`, `CPI`, `Fuel_Price`, `Temperature`, and `Holiday_Flag`).

## Analytical Workflow

```text
Walmart Dataset (6,435 rows, 45 Stores)
        │
        ▼
Data Cleaning & Datetime Indexing (pd.to_datetime -> Date Index)
        │
        ├───────────────────────────────────────────┐
        ▼                                           ▼
Store-Level Time-Series Analysis         Macroeconomic Correlation Study
(Weekly Sales & seasonal_decompose)      (Weekly_Sales vs. Unemployment Rate)
        │                                           │
        ▼                                           ▼
Trend, Seasonal & Residual Components    Top Affected Stores (Store 38: -0.79, Store 44: -0.78)
```

## Key Findings from the Analysis
- **Dataset Coverage:** Processed `6,435` clean weekly observations with zero missing values across `45` stores (`Store`, `Date`, `Weekly_Sales`, `Holiday_Flag`, `Temperature`, `Fuel_Price`, `CPI`, `Unemployment`).
- **Time-Series Seasonal Decomposition:** Applied additive/multiplicative `seasonal_decompose` (`period=12`) on store-level weekly revenue to separate underlying multi-year trends from recurring seasonal spikes[cite: 13].
- **Unemployment Sensitivity by Store:** Grouped transactions by `Store` to compute correlation coefficients between `Weekly_Sales` and `Unemployment`, revealing strong negative correlations in specific branches[cite: 13]:
  - **Store 38:** `r = -0.785`[cite: 13]
  - **Store 44:** `r = -0.780`[cite: 13]
  - **Store 39:** `r = -0.385`[cite: 13]

## Tech Stack
- **Data Manipulation:** Python, Pandas, NumPy[cite: 13]
- **Statistical & Time-Series Modeling:** Statsmodels (`seasonal_decompose`)[cite: 13]
- **Data Visualization:** Matplotlib, Seaborn[cite: 13]
