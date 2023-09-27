# Power BI Bank Term Deposit Subscription Dashboard Project

1. **Project Overview**
    - **Introduction**: This document provides an in-depth technical overview of the Power BI Bank Term Deposit Subscription Dashboard Project.
    - **Purpose and Objectives**: The primary purpose of this project is to create an interactive and insightful dashboard for analyzing marketing campaign data.

3. **Data Sources**
    - **Data Sources Description**: Our primary data sources include customer data, campaign data, and survey data.
    - **Data Collection**: Data is collected through API integrations, manual inputs, and automated data feeds.
    - **Data Transformation**: Power Query is used to perform data transformations, including data cleaning, filtering, and merging.

4. **Data Modeling**
    - **Calculated Columns and Measures**: The DAX formula ```Response = IF([y] = "yes", 1, 0)``` was employed to generate a calculated column named 'Response.' This column assigns a value of 1 or 0 to each row based on the content of the 'y' column.
      
5. **Dashboard Design**
    - **Design Philosophy**: The dashboard is designed for user-friendliness and interactivity.
    - **Layout and Visuals**: It features a clean layout with a mix of visuals, including visual cards, line chart, and bar chart.
    - **User Interface Elements**: Interactive elements like slicers, filters, and drill-through options are strategically placed for easy exploration of data.

6. **Key Performance Indicators (KPIs)**
    - **KPI Explanation**: The dashboard tracks various KPIs, including Average Account Balance, Loan Subscribers, Response Rate, and Retention Rate.
    - **Formulas and Calculations**: Each KPI is calculated using DAX formulas, providing real-time insights into campaign performance.

7. **Data Visualization**
    - **Visual Descriptions**: Visualizations comprise visual cards representing several key performance indicators (KPIs), including Response Rate, Retention Rate, Loan Subscribers, and Average Account Balance. Additionally, there is a line chart that illustrates the 
     trend of loan subscribers over the course of the month, and a bar chart that provides insights into the distribution of loan subscribers based on their marital status.
    - **Purpose and Insights**: These visuals help users understand campaign effectiveness, customer behavior, and financial performance.

8. **Slicers and Filters**
    - **Slicer Explanation**: Slicers and filters enable users to interactively explore data by selecting specific demographics, time periods, and campaign types. However, in our visualizations, we have primarily focused on using the 'Job' demographic for filtering and       analysis.
    - **Usage Guidelines**: Users can simply click on slicers to filter data or use the drill-through feature to get more detailed insights.

9. **Measures and Calculations**
    - **List of DAX Measures**: Measures includes
       1. Average Account Balance.
      ```Average Balance = AVERAGE('bank-dataset'[balance])```
      2. Loan Subscribers
      ```Loan Subscribers = COUNTROWS(FILTER('bank-dataset', [loan] = "yes" && [y] = "yes"))```
      3. Response Rate
      ```Response Rate = DIVIDE(SUM('bank-dataset'[Response]), COUNTROWS('bank-dataset'))```
      4. Retention Rate
      ```Retention Rate = DIVIDE(COUNTROWS(FILTER('bank-dataset', [y] = "yes")), COUNTROWS(FILTER('bank-dataset', [previous] > 0)))```
    - **Purpose and Usage**: These measures provide users with the ability to analyze and compare KPIs across different dimensions.

![]()
