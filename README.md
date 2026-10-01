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
