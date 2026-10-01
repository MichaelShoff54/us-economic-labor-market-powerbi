Data Dictionary

This document defines the primary fields used in the U.S. Economic & Labor Market Intelligence Dashboard.

Labor Market Tables
Fact_Unemployment
Field	Description
Date	Observation date
Unemployment Rate	U.S. civilian unemployment rate
Source	FRED data source identifier
Fact_Labor_Force
Field	Description
Month Start	Month represented by the observation
Labor Force Participation Rate	Percentage of the civilian population participating in the labor force
Source	FRED data source identifier
Fact_Payrolls
Field	Description
Month Start	Month represented by the observation
Nonfarm Payrolls	Total U.S. nonfarm payroll employment
Source	FRED data source identifier
Fact_Wages
Field	Description
Month Start	Month represented by the observation
Average Hourly Earnings	Average hourly earnings measure
Source	FRED data source identifier
Inflation & Interest Rate Tables
Fact_CPI
Field	Description
Month Start	Month represented by the observation
CPI	Consumer Price Index
Source	FRED data source identifier
Fact_Fed_Funds
Field	Description
Month Start	Month represented by the observation
Federal Funds Rate	Effective federal funds rate
Source	FRED data source identifier
Fact_Treasury_Monthly
Field	Description
Month Start	Month represented by the observation
Average 10-Year Treasury Yield	Monthly average of daily 10-year Treasury constant maturity yields
Economic Growth Table
Fact_GDP
Field	Description
Quarter Start	Beginning date of the quarter represented by the observation
Real GDP	Inflation-adjusted U.S. gross domestic product
Source	FRED data source identifier
Date Dimensions
Dim_Date

Provides daily date attributes used for date-based analysis.

Key fields include:

Date
Year
Month Number
Month
Quarter
Year Month
Dim_Month

Provides monthly date attributes used to connect monthly economic indicators.

Key fields include:

Month Start
Year
Month Number
Month
Quarter
Year Month
Dim_Quarter

Provides quarterly date attributes used for GDP analysis.

Key fields include:

Quarter Start
Year
Quarter
Measures

The Measures table contains centralized DAX measures used throughout the report.

Examples include:

Current Unemployment Rate
Inflation YoY %
Wage Growth YoY %
Real Wage Growth %
Payroll YoY Growth
Current Federal Funds Rate
Current 10Y Treasury Yield
10Y - Fed Funds Spread
Real GDP YoY Growth %
Real GDP QoQ Growth %
