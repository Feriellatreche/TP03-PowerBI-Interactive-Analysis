
# TP03 – Interactive Data Analysis and Visualization Using Power BI

## 1. Project Overview

This project focuses on interactive data analysis and visualization using **Microsoft Power BI Desktop**. It uses the large CSV dataset prepared for TP02 to explore financial trading records, assess data quality, and develop an interactive dashboard.

The dataset covers the period **2000–2009** and includes historical trading information such as opening prices, closing prices, trading volumes, and trading amounts.

The project includes:
- Data import and inspection.
- Data cleaning and quality assessment using Power Query.
- Data visualization and dashboard development.
- Interactive filtering using slicers.
- Analysis and interpretation of dashboard results.
- Preparation of project deliverables for GitHub.

A lightweight Power BI report was also created for GitHub publication because the original report was too large for standard GitHub uploads.

---

## 2. Project Objectives

The objectives of this practical assignment are to:

- Import the dataset prepared during TP02 into Power BI.
- Inspect columns, data types, missing values, errors, and duplicate rows.
- Use Power Query to prepare the data for analysis.
- Create visualizations for closing prices and trading volumes.
- Identify months with the highest and lowest average closing prices.
- Analyze variations in monthly trading volumes.
- Examine average closing-price trends.
- Implement interactive filtering using slicers.
- Evaluate the effects of filters on the visualizations.
- Interpret the analytical results.
- Prepare a lightweight version of the report for GitHub.

---

## 3. Dataset Description

The dataset used in this project is:

`combined_over_5gb.csv`

### 3.1 Original Dataset Characteristics

| Property | Description |
|---|---|
| File format | CSV |
| File size | Approximately 5.20 GB |
| Number of rows | 98,777,445 |
| Number of columns | 7 |
| Time period | 2000–2009 |
| Domain | Financial market trading data |

### 3.2 Dataset Columns

| Column | Description |
|---|---|
| `trade_time` | Date and time of the trading record |
| `open` | Opening price during the recorded interval |
| `high` | Highest price during the interval |
| `low` | Lowest price during the interval |
| `close` | Closing price during the interval |
| `vol` | Trading volume |
| `amount` | Total trading amount |

These variables support the analysis of closing-price variations and trading activity.

**Note:** The original CSV dataset is not included in this repository because of its large size.

---

## 4. Data Import and Inspection

The original CSV dataset was imported into Power BI Desktop.

The dataset structure, column names, and data types were inspected.

### Data Types

| Column | Power BI Data Type |
|---|---|
| `trade_time` | Date/Time |
| `open` | Decimal Number |
| `high` | Decimal Number |
| `low` | Decimal Number |
| `close` | Decimal Number |
| `vol` | Whole Number |
| `amount` | Decimal Number |

The column names were clear and descriptive, so renaming was unnecessary.

---

## 5. Data Cleaning and Preparation

Power Query Editor was used to inspect data quality and prepare the dataset for visualization.

### 5.1 Missing Values and Errors

The **Column Quality** feature was used to examine the inspected columns.

The displayed results were:

| Quality Indicator | Result |
|---|---|
| Valid values | 100% |
| Empty values | 0% |
| Errors | 0% |

These results indicate that no missing values or errors were identified in the inspected columns according to the displayed Column Quality statistics.

Column Quality does not independently guarantee that every financial value is economically reasonable.

### 5.2 Duplicate Rows

Duplicate detection was performed using the **Group By** functionality in Power Query.

The procedure involved:

1. Grouping records according to the selected columns.
2. Applying the **Count Rows** operation.
3. Creating a count for each group.
4. Checking whether any group had a count greater than 1.

A count greater than 1 indicates repeated records with identical values in the grouping columns.

The reported duplicate-checking result was **zero duplicate rows**.

Therefore, no duplicate removal was required.

### 5.3 Data Types and Column Names

The data types were checked and found appropriate for the analysis.

The original column names were clear and meaningful, so no renaming was necessary.

Unnecessary transformations were avoided.

---

## 6. Dashboard Design and Visualizations

The Power BI dashboard contains five visual elements.

### 6.1 KPI Card – Average Closing Price

The KPI Card displays the average value of the `close` column.

- Measure: Average of `close`
- Displayed value: **15.39**

**Purpose:** Provide an overall indicator of the average closing price.

### 6.2 Horizontal Bar Chart – Average Closing Price by Month

- Category axis: Month derived from `trade_time`
- Value: Average of `close`

**Purpose:** Compare monthly average closing prices and identify relatively high and low values.

### 6.3 Vertical Column Chart – Average Closing Price by Month

- Category axis: Month derived from `trade_time`
- Value: Average of `close`

**Purpose:** Compare monthly average closing prices using vertical columns.

### 6.4 Column Chart – Total Trading Volume Over Time

- Category axis: Month derived from `trade_time`
- Value: Sum of `vol`

**Purpose:** Analyze differences in total trading volume across months.

This visualization was used as an alternative to the map requirement.

### 6.5 Line Chart – Average Closing Price Trend

- Horizontal axis: Month derived from `trade_time`
- Vertical axis: Average of `close`

**Purpose:** Illustrate monthly fluctuations in average closing prices.

---

## 7. Dashboard Results, Analysis, and Interpretation

This section presents the main observations from the Power BI dashboard.

**Note:** Monthly numerical values are approximate readings from the dashboard screenshot. They should be verified using Power BI data labels or exported tables before being treated as exact results.

### 7.1 KPI Card Analysis

The KPI Card displays an average closing price of **15.39**.

This represents the average closing price across the records included in the current filter context.

It provides a reference for comparing monthly average closing prices.

### 7.2 Monthly Average Closing Price Analysis

The horizontal bar chart shows variations in average closing prices across the twelve calendar months.

| Indicator | Month | Approximate Value |
|---|---|---|
| Highest average closing price | June | 16.5 |
| Lowest average closing price | October | 14.1 |
| Difference | June–October | 2.4 |

**Interpretation:**

June recorded the highest average closing price, indicating relatively higher price levels during this calendar month.

October recorded the lowest average closing price, indicating comparatively lower price levels.

The approximate difference of 2.4 price units highlights variation between monthly averages.

These differences may be associated with changing market conditions, investor behavior, or the composition of the underlying observations.

However, additional analysis would be necessary to determine the exact causes.

### 7.3 Trading Volume Analysis

The trading-volume chart compares total trading volume across the twelve calendar months.

| Indicator | Month | Approximate Trading Volume |
|---|---|---|
| Highest trading volume | April | 85 billion |
| Lowest trading volumes | October and November | 30 billion each |
| Other relatively active months | March, May, July | Relatively high |

**Interpretation:**

April recorded the highest total trading volume, indicating the greatest aggregate trading activity among the displayed months.

October and November recorded comparatively low trading volumes.

These differences suggest that trading activity was not distributed equally across calendar months.

Higher trading volume may reflect increased trading activity, but the total can also be influenced by differences in record counts and the number of trading sessions.

Therefore, the observed variation does not independently establish a specific economic cause.

### 7.4 Average Closing Price Trend Analysis

The line chart illustrates changes in average closing prices across calendar months.

#### Phase 1: January to June – Upward Trend

The average closing price increased from approximately 14.1 in January to 16.5 in June.

This represents an upward pattern in the monthly averages.

#### Phase 2: July to October – Downward Trend

After June, the average closing price decreased progressively.

The lowest approximate monthly average was recorded in October at 14.1.

#### Phase 3: November to December – Partial Recovery

Average closing prices increased again in November and December.

The December average reached approximately 14.9.

This indicates a partial recovery relative to October, although the average remained below the June peak.

**Interpretation:**

The monthly average closing prices fluctuated rather than following a constant upward or downward pattern.

Because the dataset covers 2000–2009, this chart represents an aggregated calendar-month pattern across multiple years, not a continuous price trend for a single year.

### 7.5 Closing Prices and Trading Volume Comparison

An important observation is that the highest average closing price and highest total trading volume occurred in different months.

- Highest average closing price: **June**
- Highest total trading volume: **April**

This demonstrates that the month with the highest average closing price did not necessarily have the highest total trading volume.

Additional statistical analysis would be needed to examine the relationship between trading volume and closing prices.

### 7.6 Summary of Analytical Findings

The dashboard highlights the following observations:

- Overall average closing price: **15.39**.
- Highest monthly average closing price: **June (~16.5)**.
- Lowest monthly average closing price: **October (~14.1)**.
- Highest total trading volume: **April (~85 billion)**.
- Relatively low trading volumes: **October and November (~30 billion each)**.
- Average closing prices increased toward June, declined toward October, and partially recovered afterward.
- The highest average closing price and the highest total trading volume occurred in different months.

**Methodological limitation:**

Monthly statistics combine observations from multiple years between 2000 and 2009.

Therefore, these results should not be interpreted as the performance of a single stock or a single calendar year.

---

## 8. Interactive Filtering with Slicers

A month-based slicer was added to make the dashboard interactive.

Different month selections were tested.

The tests confirmed that:

- The charts responded to the selected month.
- Selecting another month updated the displayed visualizations.
- The KPI Card changed according to the selected filter.

These interactions support comparisons between selected periods.

---

## 9. Lightweight Preview Version

A lightweight version of the Power BI report was created for GitHub publication.

The original report contained the full dataset and was too large for standard GitHub uploads.

To reduce the file size, Power Query was used to retain only the first **1,000 rows**.

### Preview Characteristics

- Contains the first 1,000 rows of the original dataset.
- Retains all seven columns.
- Preserves the report layout and visualizations.
- Is intended for preview and demonstration.
- Does not replace the full-data report.

**Important:**

The lightweight version does not represent the complete dataset statistically.

Its numerical results and visualizations may differ from the original full-data report.

The original full-data report and CSV dataset are retained separately and are not included in the GitHub repository.

---

## 10. Final Dashboard and Deliverables

### Dashboard Screenshot

![TP03 Power BI Dashboard](screenshots/TP03_Dashboard.png)

### Project Deliverables

1. **Power BI Preview Report**

   `TP03_Interactive_Data_Analysis_Lite.pbix`

   Lightweight report containing the first 1,000 rows.


3. **Project Documentation**

   `README.md`

4. **Short Written Report**

   `report/Report.txt`

The original full-data report and source CSV are kept separately.

---

## 11. Conclusion

This practical assignment demonstrated the use of Power BI for inspecting, preparing, analyzing, and visualizing financial trading data covering the period **2000–2009**.

Power Query was used to assess data quality, verify data types, and check for duplicate rows.

Five visual elements were created to summarize average closing prices and total trading volume.

The dashboard displayed an overall average closing price of **15.39**.

The analysis indicated that June had the highest monthly average closing price, while October had the lowest.

April recorded the highest total trading volume.

The line chart revealed an increase in monthly average closing prices toward June, followed by a decline toward October and a partial recovery in the final months.

Interactive filtering was implemented using a month slicer, and its effects on the charts and KPI Card were tested.

A lightweight preview report containing the first 1,000 rows was prepared for GitHub, while the full-data report and original dataset were retained separately.

Overall, the project demonstrates the importance of data quality assessment, interactive visualization, and careful interpretation when analyzing large financial datasets.

---

## 12. Tools and Technologies

- **Microsoft Power BI Desktop:** Dashboard development and visualization.
- **Power Query Editor:** Data inspection, grouping, and preparation.
- **CSV:** Original dataset format.
- **GitHub:** Documentation and lightweight report publication.
