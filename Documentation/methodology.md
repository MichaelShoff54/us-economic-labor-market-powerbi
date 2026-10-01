Methodology

This document describes the analytical methods, calculations, and modeling decisions used in the U.S. Economic & Labor Market Intelligence Dashboard.

Data Preparation

Publicly available economic data was obtained from the Federal Reserve Economic Data (FRED) database.

Power Query was used to prepare the datasets for analysis.

Key transformation steps included:

Standardizing field names and data types
Converting observation dates into consistent date formats
Creating month-start and quarter-start fields
Removing unnecessary source columns
Aggregating daily Treasury yield observations into monthly averages
Preparing separate fact tables for each economic indicator
Creating dedicated date dimensions for daily, monthly, and quarterly analysis
Time Period Comparisons

Year-over-year calculations compare the current observation with the corresponding observation from the previous year.

For monthly data:

Current Month − Same Month Prior Year

For quarterly data:

Current Quarter − Same Quarter Prior Year

Growth percentages are calculated as:

(Current Period − Prior Period) / Prior Period

Inflation

Inflation is measured using the year-over-year percentage change in the Consumer Price Index.

The calculation is:

(Current CPI − CPI 12 Months Earlier) / CPI 12 Months Earlier

The resulting value is displayed as a percentage.

Wage Growth

Wage growth represents the year-over-year percentage change in average hourly earnings.

The calculation is:

(Current Average Hourly Earnings − Prior-Year Average Hourly Earnings) / Prior-Year Average Hourly Earnings

Real Wage Growth

Real wage growth is calculated as nominal wage growth minus CPI inflation.

The calculation is:

Wage Growth YoY % − Inflation YoY %

This provides an approximate measure of whether employee earnings are increasing faster or slower than consumer prices.

A positive result indicates that nominal wage growth exceeds the measured inflation rate, while a negative result indicates that inflation exceeds nominal wage growth.

Payroll Growth

Nonfarm payroll growth is evaluated using year-over-year percentage change.

The calculation is:

(Current Payrolls − Prior-Year Payrolls) / Prior-Year Payrolls

This provides a standardized measure of employment growth over time.

Interest Rate Analysis

The dashboard analyzes both the federal funds rate and the 10-year Treasury yield.

The 10-year Treasury dataset contains daily observations. These observations were aggregated into monthly averages before being incorporated into the final model.

Treasury-Fed Funds Spread

The spread is calculated as:

10-Year Treasury Yield − Federal Funds Rate

This provides a simple measure of the difference between longer-term Treasury yields and the short-term federal funds rate.

GDP Growth

Real GDP growth is evaluated using both year-over-year and quarter-over-quarter comparisons.

Year-over-Year GDP Growth

(Current Quarter GDP − Same Quarter Prior Year GDP) / Same Quarter Prior Year GDP

Quarter-over-Quarter GDP Growth

(Current Quarter GDP − Previous Quarter GDP) / Previous Quarter GDP

Data Modeling

The Power BI model uses a dimensional structure with dedicated date dimensions and separate fact tables.

Monthly economic indicators are connected through Dim_Month, while quarterly GDP data is connected through Dim_Quarter.

Daily observations are supported by Dim_Date.

Relationships are configured as one-to-many relationships with single-direction filtering from dimension tables to fact tables.

Visualization Approach

The dashboard was designed around an executive-reporting approach.

Visual design decisions include:

KPI cards for high-level metrics
Line charts for time-series trends
Percentage formatting for growth and rate measures
Conditional formatting for real wage growth
Interactive year filtering
Consistent page navigation
Business-focused explanatory text
Consistent visual hierarchy across all report pages

The goal is to make the dashboard useful for both detailed analysis and executive-level review.

Analytical Limitations

The dashboard is intended as a descriptive and diagnostic analytical tool rather than a forecasting model.

Economic indicators are subject to revisions, different reporting frequencies, seasonal effects, and methodological changes by the underlying data providers.

The analysis should therefore be interpreted as a view of historical and currently available economic data rather than a prediction of future economic conditions.
