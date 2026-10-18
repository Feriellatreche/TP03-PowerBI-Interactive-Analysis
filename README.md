# TP03 – Interactive Data Analysis and Visualization Using Power BI

## 1. Project Overview

This project focuses on interactive data analysis and visualization using Microsoft Power BI Desktop. It uses the large CSV dataset prepared for TP02 to explore financial trading records, examine data quality, and create an interactive dashboard.

The project covers data import, data inspection, data cleaning and preparation using Power Query, data visualization, interactive filtering, and preparation of the final deliverables.

## 2. Project Objectives

The main objectives of this practical assignment are to:

- Import the dataset used in TP02 into Power BI.
- Inspect the dataset structure, columns, data types, missing values, errors, and duplicate rows.
- Use Power Query to assess data quality and prepare the data for analysis.
- Create different types of visualizations to analyze closing prices and trading volume.
- Build an interactive dashboard using slicers.
- Test how filtering affects the charts and the KPI card.
- Save the Power BI report and capture a screenshot of the completed dashboard.

## 3. Dataset Description

The project uses the file `combined_over_5gb.csv`, prepared during TP02.

### Dataset characteristics

| Property | Description |
|---|---|
| File format | CSV |
| File size | Approximately 5.20 GB |
| Number of rows | 98,777,445 |
| Number of columns | 7 |
| Domain | Financial market trading data |

### Dataset columns

| Column | Description |
|---|---|
| `trade_time` | Date and time of the trading record |
| `open` | Opening price |
| `high` | Highest price recorded |
| `low` | Lowest price recorded |
| `close` | Closing price |
| `vol` | Trading volume |
| `amount` | Trading amount |

These columns provide the information needed to analyze closing-price trends and trading volume over time.

## 4. Data Import and Inspection

The CSV dataset was imported into Power BI Desktop. The table structure was inspected, including the column names and data types.

The following data types were checked:

- `trade_time`: Date/Time
- `open`: Decimal Number
- `high`: Decimal Number
- `low`: Decimal Number
- `close`: Decimal Number
- `vol`: Whole Number
- `amount`: Decimal Number

The column names were understandable and descriptive, so renaming was not necessary.

## 5. Data Cleaning and Preparation

Power Query Editor was used to inspect the data quality and prepare the dataset for visualization.

### 5.1 Missing Values and Errors

The Column Quality feature was used to examine the inspected columns. It reported:

- Valid values: 100%
- Empty values: 0%
- Errors: 0%

These results indicate that the inspected columns showed no missing values or errors according to the Column Quality results.

### 5.2 Duplicate Rows

A duplicate-checking operation was completed. The reported result was zero duplicate rows.

Therefore, no duplicate rows were identified by the completed check, and removing duplicates was not necessary based on that result.

### 5.3 Data Types and Column Names

The data types were checked and found appropriate for the intended analysis. The original column names were clear and meaningful, so no renaming was required.

The data preparation stage focused on verifying data quality and suitability rather than applying unnecessary transformations.

## 6. Dashboard Design and Data Visualization

An interactive dashboard was created in Power BI Desktop using five visual elements.

### 6.1 KPI Card – Average Closing Price

A Card visual was created to display the average value of the `close` column.

**Purpose:** To provide a clear summary indicator of the average closing price. The card also responds to the selected month in the slicer.

### 6.2 Horizontal Bar Chart – Average Closing Price by Month

A horizontal bar chart was created to compare the average closing price across months.

- Category axis: Month derived from `trade_time`
- Value: Average of `close`

**Purpose:** To make monthly comparisons of average closing prices easier.

### 6.3 Vertical Column Chart – Average Closing Price by Month

A vertical column chart was created to display the average closing price for each month.

- Category axis: Month derived from `trade_time`
- Value: Average of `close`

**Purpose:** To compare monthly average closing prices using vertical columns.

### 6.4 Column Chart – Total Trading Volume Over Time

A column chart was created to display trading volume over time.

- Category axis: Month derived from `trade_time`
- Value: Sum of `vol`

**Purpose:** To compare the total trading volume across the displayed periods.

This chart was used as the alternative to a map, consistent with the assignment's visualization requirement.

### 6.5 Line Chart – Average Closing Price Trend by Month

A line chart was created to illustrate changes in the average closing price over time.

- Horizontal axis: Month derived from `trade_time`
- Vertical value: Average of `close`

**Purpose:** To visualize the monthly trend in average closing prices.

## 7. Interactive Filtering with Slicers

A slicer based on the trading date/month was added to make the dashboard interactive.

Different month selections were tested to verify the behavior of the dashboard.

The tests confirmed that:

- The charts responded to the selected month.
- Selecting another month updated the displayed visualizations.
- The average closing-price Card also changed according to the selected filter.

These tests demonstrated that the dashboard supports interactive exploration of the data.

## 8. Final Dashboard and Deliverables

The dashboard was arranged in Power BI Desktop to present the visualizations clearly.

The following deliverables were prepared:

1. **Power BI report (`.pbix`):** The saved report containing the dashboard and its visualizations.
2. **Dashboard screenshot (`.png`):** A screenshot of the completed dashboard.
3. **Project documentation (`README.md`):** This file, describing the dataset, methodology, visualizations, and interactive filtering.

## 9. Conclusion

This practical assignment demonstrated how Power BI can be used to inspect, prepare, analyze, and visualize a large financial trading dataset. Power Query was used to assess data quality, verify data types, and check for duplicate rows. Five visual elements were created to summarize average closing prices and total trading volume. A month slicer enabled interactive filtering, and its effect on both the charts and the KPI Card was tested successfully. The Power BI report was saved, and a screenshot was prepared as part of the final submission.

## 10. Tools and Technologies

- **Microsoft Power BI Desktop:** Data visualization and dashboard development.
- **Power Query Editor:** Data inspection, quality assessment, and preparation.
- **CSV:** Source dataset format.
- **GitHub:** Project documentation and submission repository.
