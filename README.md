# Business_Insights
This project focuses on implementing Power BI at AtliQ Hardware to drive data-driven decision-making and optimize performance across finance, sales, marketing, and supply chain operations.

🌟 Challenge: Atliq Technologies, a leading electronics firm, struggled with data analysis due to reliance on Excel files and was looking for an efficient solution for their business insights.

🌟 Objective: Using Power BI, I aimed to transform approximately 2 million rows of records into actionable insights, enhancing decision-making across Finance, Sales, Marketing, Supply Chain, and Executive sectors.

🌟 Tools Utilized: MySQL, Power BI Desktop, Excel, DAX Studio.

🌟 Data Modeling Approach: Snowflake Schema for a scalable data model.

🌟 Key Metrics Analyzed:
- Sales Performance: Gross Sales, Net Invoice Sales, Net Sales.
- Profitability: Net Profit, Gross Margin, Cost of Goods Sold (COGS).
- Deductions: Pre-Invoice and Post-Invoice Deductions.
- Error Metrics: Net Error, Absolute Net Error.
- Forecasting: Year to Date (YTD), Year to Go (YTG), Forecast Accuracy.

🌟 Skills & Techniques Applied:
- Data Transformation and Loading: Efficiently handled large datasets using Power Query and DAX.
- Advanced Data Modeling: Implemented robust data models and calculated columns.
- Dynamic Visualizations: Created interactive dashboards with dynamic titles, bookmarks, and toggle buttons.
- KPI Implementation: Developed and visualized key performance indicators.
- Report Optimization: Enhanced performance by disabling unnecessary loads and validating data accuracy.

🌟 Dashboards:
- 💹 Finance Dashboard: Get P&L statements for any customer/product/country or aggregation of the above over any time period and more.
- 💰 Sales Dashboard: Analyze the performance of your customers over key metrics like Net Sales, and Gross Margin, and view the same in profitability/growth matrix.
- 📢 Marketing Dashboard: Analyze the performance of your product over key metrics like Net Sales, and Gross Margin, and view the same in profitability/growth matrix.
- 💱 Supply Chain Dashboard: Get Forecast Accuracy, Net Error, and risk profile for product, segment, category, customer, etc.
- 👨🏻‍💼 Executive Dashboard: A top-level dashboard for executives consolidating top insights from all dimensions of the business.


## Deployment

[Live Dashboard link](https://app.powerbi.com/view?r=eyJrIjoiNTJiZmQ3OGItYTMyNi00ZDJhLWJmZmYtZWY1YWI3MWY3ZGI5IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)


## Data Model

- Data modeling plays a vital role and is considered as the basement of the report. All the visuals will be built upon the data model.
- In this project, we have followed the Snowfall data modeling method.

<img src="https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Data_model.PNG">


### Dataset **Understanding.**

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get a good understanding of what are data available.

Dimension table: It will have static data like details of customers and products

Fact table: It will have the data about the transactions  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, Spain)
        - **75** distinct customers throughout the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, Flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, Spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s needs in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purposes
        - The table is denormalized by the data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the dates of the month will be replaced by the start date of the month
        - It will have all the column names and in the end, it will have the forecast quantity needed of the customer
    - fact_sales_monthly
        - This table is more or less is same as the fact_forecase_monthly table, but the last column has the value of the sold quantity instead of the forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre-invoice deductions percentage for each customer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deduction details

## Info Page

![App Screenshot](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Home_page.jpg)

## Finance View

![App Screenshot](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Finance_page.jpg)

## Sales View

![App Screenshot](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Sales_page.jpg)

## Marketing View

![App Screenshot](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Marketing_page.jpg)

## Supply chain View

![App Screenshot](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Supply%20chain_page.jpg)

## Executive View

![App Screenshot](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Resources/Executive_page.jpg)



you can find the full report file pdf here : [Report](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Report/Report.pdf)

BI report file here : [Report](https://github.com/Sandeepm959/Business_Insights/blob/0a5ace08ed65a7383f43a4476da14696a716521d/Report/bi_360.pbix)
