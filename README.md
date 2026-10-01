U.S. Economic & Labor Market Intelligence Dashboard

An interactive Power BI dashboard analyzing U.S. economic and labor-market conditions using publicly available data from the Federal Reserve Economic Data (FRED) database.

The project combines labor-market, inflation, wage, interest-rate, and economic-growth data to provide an executive-level view of current economic conditions and their potential implications for business planning.

Project Overview

This project was developed as a portfolio demonstration of end-to-end data analytics and business intelligence skills.

The dashboard transforms raw economic datasets into an interactive reporting solution designed to help analysts and business leaders monitor:

Employment and unemployment conditions
Labor-force participation
Nonfarm payroll growth
Wage growth and purchasing power
Consumer price inflation
Federal funds and Treasury yields
Real economic growth
Potential business implications of changing economic conditions

The project emphasizes data preparation, dimensional modeling, DAX-based analysis, interactive visualization, and translating quantitative trends into business-oriented insights.

Business Objective

Businesses operate within changing economic conditions that can affect labor costs, consumer purchasing power, hiring decisions, financing costs, and overall financial planning.

The objective of this dashboard is to consolidate several major U.S. economic indicators into a single interactive reporting environment so users can evaluate trends and relationships across the labor market, inflation, interest rates, and economic growth.

The dashboard is designed around the perspective of a financial or business analyst monitoring external economic conditions that may be relevant to budgeting, forecasting, workforce planning, and strategic decision-making.

Key Business Questions

The dashboard is designed to help answer several practical business and financial analysis questions:

How are unemployment, labor-force participation, and nonfarm payrolls changing over time?
Is wage growth keeping pace with inflation?
How has the federal funds rate changed relative to 10-year Treasury yields?
What does the relationship between inflation and interest rates indicate about the broader financing environment?
How are economic growth and labor-market conditions changing over time?
What potential implications could these economic trends have for workforce planning, consumer purchasing power, and financial planning?

The analysis is primarily descriptive and diagnostic rather than a forecasting model. Its purpose is to demonstrate how public economic data can be transformed into actionable business intelligence.

Data Sources & Indicators

All economic data used in this project was obtained from the Federal Reserve Economic Data (FRED) database maintained by the Federal Reserve Bank of St. Louis.

Labor Market
Indicator	FRED Series	Description
Unemployment Rate	UNRATE	U.S. civilian unemployment rate
Labor Force Participation Rate	CIVPART	Percentage of the civilian population participating in the labor force
Nonfarm Payrolls	PAYEMS	Total U.S. nonfarm payroll employment
Average Hourly Earnings	CES0500000003	Average hourly earnings of production and nonsupervisory employees
Inflation & Interest Rates
Indicator	FRED Series	Description
Consumer Price Index	CPIAUCSL	Consumer Price Index for All Urban Consumers
Federal Funds Rate	FEDFUNDS	Effective federal funds rate
10-Year Treasury Yield	DGS10	U.S. 10-year Treasury constant maturity yield
Economic Growth
Indicator	FRED Series	Description
Real GDP	GDPC1	Inflation-adjusted U.S. gross domestic product
Data Frequency

The datasets contain different reporting frequencies:

Monthly: unemployment, labor-force participation, payrolls, wages, CPI, and federal funds rate
Daily: 10-year Treasury yield
Quarterly: real GDP

The daily Treasury yield data was aggregated to monthly averages for consistency with the other monthly economic indicators.

Data was cleaned and transformed using Power Query before being incorporated into the Power BI data model.

Data Preparation & Modeling

The project uses Power Query and a dimensional data model to prepare the FRED datasets for analysis.

Data Preparation

The raw datasets were imported into Power BI and transformed using Power Query.

Key preparation steps included:

Standardizing column names and data types
Converting date fields to appropriate date formats
Creating month-start and quarter-start fields for datasets with different reporting frequencies
Removing unnecessary columns and metadata
Aggregating daily 10-year Treasury yield observations into monthly averages
Separating raw data from analysis-ready fact tables
Creating consistent time dimensions for monthly, daily, and quarterly analysis
Data Model

The Power BI model uses separate fact tables for the major economic indicators and dedicated date dimensions to support time-based analysis.

The primary tables include:

Fact_Unemployment
Fact_Labor_Force
Fact_Payrolls
Fact_Wages
Fact_CPI
Fact_Fed_Funds
Fact_Treasury_Monthly
Fact_GDP

The model also includes:

Dim_Date for daily date relationships
Dim_Month for monthly economic analysis
Dim_Quarter for quarterly GDP analysis
Measures for centralized DAX calculations

Relationships were designed as one-to-many relationships with single-direction filtering from the date dimensions to the fact tables.

Modeling Approach

Separate date dimensions were used because the underlying economic indicators are reported at different frequencies. This approach allows monthly and quarterly datasets to be analyzed without forcing incompatible date relationships into a single fact table.

The resulting model supports interactive filtering, time-series analysis, KPI calculations, and cross-indicator comparisons throughout the dashboard.

DAX & Analytical Techniques

DAX was used to create calculated measures for current-period KPIs, growth rates, trend analysis, and business-oriented economic metrics.

Key Calculations

The dashboard includes measures for:

Current unemployment rate
Current labor-force participation
Current nonfarm payrolls
Current average hourly earnings
Inflation year-over-year growth
Wage growth year-over-year
Real wage growth
Payroll growth
Federal funds rate
10-year Treasury yield
Treasury-to-Fed-funds spread
Real GDP
Real GDP year-over-year growth
Real GDP quarter-over-quarter growth
Time-Based Analysis

Time-intelligence techniques were used to compare economic indicators across different periods.

Examples include:

Month-over-month changes
Year-over-year growth
Quarter-over-quarter growth
Trailing and moving-average analysis
Current-period versus prior-period comparisons
Business-Oriented Metrics

Several measures were created to translate raw economic data into metrics that are easier to interpret from a business perspective.

For example:

Real Wage Growth

Real wage growth is calculated as:

Wage Growth YoY % − Inflation YoY %

This provides an approximate measure of whether employee earnings are growing faster or slower than consumer prices.

10-Year Treasury − Federal Funds Spread

The spread between the 10-year Treasury yield and the federal funds rate provides additional context for the relationship between short-term and longer-term interest rates.

DAX Techniques Demonstrated

The project demonstrates the use of:

CALCULATE
MAX
AVERAGE
DIVIDE
DATEADD
EDATE
DATESINPERIOD
AVERAGEX
Variables using VAR and RETURN
Filter-context manipulation
Time-intelligence calculations
Conditional logic with IF

These calculations allow the dashboard to respond dynamically to user selections and provide consistent analytical metrics across the report.

Dashboard Structure

The Power BI report contains four interactive pages, each designed for a different analytical purpose.

1. Executive Economic Overview

Provides a high-level view of U.S. economic conditions through key performance indicators and trend analysis.

Key metrics include:

Unemployment
Labor-force participation
Nonfarm payrolls
Inflation
Wage growth
Real wage growth
Federal funds rate
10-year Treasury yield
Real GDP

This page is designed for executives, financial analysts, and business stakeholders who need a concise overview of the economic environment.

2. Labor Market Analysis

Focuses on employment conditions and wage trends.

The page analyzes:

Unemployment trends
Labor-force participation
Nonfarm payroll growth
Wage growth
Wage growth relative to inflation

This provides context for workforce planning, labor costs, and changes in employee purchasing power.

3. Inflation & Interest Rate Analysis

Examines inflation and the broader interest-rate environment.

The page includes:

CPI inflation trends
Federal funds rate trends
10-year Treasury yields
Treasury-to-Fed-funds spread
Inflation versus the federal funds rate

These indicators provide context for purchasing power, monetary conditions, financing costs, and financial planning.

4. Business Impact & Analyst Insights

Translates the economic indicators into business-oriented considerations.

The page evaluates:

Consumer purchasing power
Labor-market conditions
Financing conditions
Inflation and wage relationships
Key economic indicators through a business conditions matrix

It also includes a wage-growth-versus-inflation analysis designed to connect quantitative economic trends with potential business planning considerations.

Interactive Features

The report includes interactive features such as:

Year filtering
Cross-filtering between visualizations
Interactive KPI cards
Trend visualizations
Conditional formatting
Page navigation
Business-focused analytical insights

Tools & Technologies
Business Intelligence & Visualization
Microsoft Power BI
Power BI Desktop
Interactive dashboards
Data visualization
KPI reporting
Data Preparation & Transformation
Power Query
Data cleaning
Data transformation
Data aggregation
Data type standardization
Dimensional data modeling
Analytics & Calculations
DAX
Time-series analysis
Year-over-year analysis
Month-over-month analysis
Quarter-over-quarter analysis
Trend analysis
Conditional formatting
Data Source
Federal Reserve Economic Data (FRED)
Public economic datasets
Documentation & Version Control
GitHub
Markdown
Project documentation

Key Insights

The dashboard is designed to identify relationships and trends across major U.S. economic indicators.

Examples of analytical insights supported by the dashboard include:

Labor Market Conditions

Changes in unemployment, labor-force participation, and payroll growth can provide context for employment conditions and potential workforce-planning considerations.

Wage Growth & Purchasing Power

Comparing wage growth with consumer-price inflation provides an indication of whether nominal earnings are increasing faster or slower than the general price level.

Inflation & Interest Rates

Examining inflation alongside the federal funds rate and Treasury yields provides context for changes in the broader monetary and financing environment.

Economic Growth

Real GDP growth provides an additional measure of overall economic activity and allows economic growth to be evaluated alongside labor-market and inflation trends.

Business Planning Considerations

The combination of these indicators can help analysts monitor external economic conditions that may be relevant to:

Workforce planning
Compensation and labor-cost analysis
Consumer demand
Budgeting and forecasting
Financing decisions
Strategic planning

The dashboard is intended as an analytical monitoring tool rather than a predictive forecasting model. Conclusions should be evaluated alongside company-specific financial, operational, and market information.

