# TP03 – Interactive Data Analysis and Visualization Using Power BI

## 1. Project Overview

This project focuses on interactive data analysis and visualization using Microsoft Power BI Desktop. It uses the large CSV dataset prepared for TP02 to explore financial trading records, examine data quality, and create an interactive dashboard.

The project covers data import, data inspection, data quality assessment using Power Query, data visualization, interactive filtering, and preparation of the final deliverables.

A lightweight version of the Power BI report was created specifically for preview and upload to GitHub because the original report file was too large for standard GitHub file uploads.

## 2. Project Objectives

The main objectives of this practical assignment are to:

- Import the dataset used in TP02 into Power BI.
- Inspect the dataset structure, columns, data types, missing values, errors, and duplicate rows.
- Use Power Query to assess data quality and prepare the data for analysis.
- Create different types of visualizations to analyze closing prices and trading volume.
- Build an interactive dashboard using slicers.
- Test how filtering affects the charts and the KPI Card.
- Save the Power BI report and capture a screenshot of the completed dashboard.
- Prepare a lightweight preview version of the report for publication on GitHub.

## 3. Dataset Description

The project uses the file `combined_over_5gb.csv`, prepared during TP02.

### Original Dataset Characteristics

| Property | Description |
|---|---|
| File format | CSV |
| File size | Approximately 5.20 GB |
| Number of rows | 98,777,445 |
| Number of columns | 7 |
| Domain | Financial market trading data |

### Dataset Columns

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

**Note:** The original CSV dataset is not included in this GitHub repository because of its large size.

## 4. Data Import and Inspection

The original CSV dataset was imported into Power BI Desktop. The table structure was inspected, including the column names and data types.

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

Power Query Editor was used to inspect data quality and prepare the dataset for visualization.

### 5.1 Missing Values and Errors

The Column Quality feature was used to examine the inspected columns. It reported:

- Valid values: 100%
- Empty values: 0%
- Errors: 0%

These results indicate that the inspected columns showed no missing values or errors according to the Column Quality results.

### 5.2 Duplicate Rows

A duplicate-checking operation was completed on the original dataset. The reported result was zero duplicate rows.

Therefore, no duplicate rows were identified by the completed check.

### 5.3 Data Types and Column Names

The data types were checked and found appropriate for the intended analysis. The original column names were clear and meaningful, so no renaming was required.

The data preparation stage focused on verifying data quality and suitability rather than applying unnecessary transformations.

## 6. Dashboard Design and Data Visualization

The Power BI dashboard contains five visual elements.

### 6.1 KPI Card – Average Closing Price

A Card visual was created to display the average value of the `close` column.

**Purpose:** To provide a summary indicator of the average closing price. The Card responds to the month selected in the slicer.

### 6.2 Horizontal Bar Chart – Average Closing Price by Month

A horizontal bar chart was created to compare average closing prices across months.

- Category axis: Month derived from `trade_time`
- Value: Average of `close`

**Purpose:** To make monthly comparisons of average closing prices easier.

### 6.3 Vertical Column Chart – Average Closing Price by Month

A vertical column chart was created to display average closing prices by month.

- Category axis: Month derived from `trade_time`
- Value: Average of `close`

**Purpose:** To compare monthly average closing prices using vertical columns.

### 6.4 Column Chart – Total Trading Volume Over Time

A column chart was created to display trading volume over time.

- Category axis: Month derived from `trade_time`
- Value: Sum of `vol`

**Purpose:** To compare total trading volume across the displayed periods.

This chart was used as the alternative to a map for the visualization requirement.

### 6.5 Line Chart – Average Closing Price Trend by Month

A line chart was created to illustrate changes in average closing prices over time.

- Horizontal axis: Month derived from `trade_time`
- Vertical value: Average of `close`

**Purpose:** To visualize the monthly trend in average closing prices.

## 7. Interactive Filtering with Slicers

A slicer based on the trading date/month was added to make the dashboard interactive.

Different month selections were tested to verify the behavior of the dashboard.

The tests confirmed that:

- The charts responded to the selected month.
- Selecting another month updated the displayed visualizations.
- The average closing-price Card changed according to the selected filter.

These tests demonstrated that the dashboard supports interactive exploration of the data.

## 8. Lightweight Preview Version

A lightweight version of the Power BI report was created specifically for preview and upload to GitHub.

The original report contained the full dataset, making the `.pbix` file too large for standard GitHub uploads. To reduce the file size, the preview version was modified in Power Query to retain only the first 1,000 rows.

### Preview Version Characteristics

- Contains the first 1,000 rows of the original dataset.
- Retains the dataset's seven columns.
- Is intended to demonstrate the report layout and visualizations.
- Is designed for preview and publication on GitHub.
- Does not replace the original full-data report.

**Important:** Numerical results and trends in the preview version may differ from those obtained using the complete dataset. The preview version should not be interpreted as representing the full dataset's statistical results.

The original full-data report is retained separately. Neither the original CSV dataset nor the full-data report is included in the GitHub repository.

## 9. Final Dashboard and Deliverables

The dashboard was arranged in Power BI Desktop to present the visualizations clearly.

The project deliverables include:

1. **Lightweight Power BI report (`TP03_Interactive_Data_Analysis_Lite.pbix`):** A reduced-size preview version containing the first 1,000 rows.
2. **Dashboard screenshot (`screenshots/TP03_Dashboard.png`):** A screenshot of the dashboard.
3. **Project documentation (`README.md`):** This file, describing the dataset, methodology, visualizations, and interactive filtering.
4. **Short written report (`report/Report.txt`):** A concise summary of the practical assignment.

The original full-data report and source CSV are kept separately and are not uploaded to GitHub.

## 10. Conclusion

This practical assignment demonstrated how Power BI can be used to inspect, prepare, analyze, and visualize financial trading data. Power Query was used to assess data quality, verify data types, and check for duplicate rows. Five visual elements were created to summarize average closing prices and total trading volume. A month slicer enabled interactive filtering, and its effect on the charts and KPI Card was tested successfully. A lightweight preview report containing the first 1,000 rows was prepared for publication on GitHub, while the original full-data report and CSV dataset were retained separately.

## 11. Tools and Technologies

- **Microsoft Power BI Desktop:** Data visualization and dashboard development.
- **Power Query Editor:** Data inspection, quality assessment, and preparation.
- **CSV:** Source dataset format.
- **GitHub:** Project documentation and lightweight report publication.
