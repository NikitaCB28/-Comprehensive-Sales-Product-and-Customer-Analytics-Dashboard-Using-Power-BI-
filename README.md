# -Comprehensive-Sales-Product-and-Customer-Analytics-Dashboard-Using-Power-BI-
## Features
⚡Microsoft SQL Server / SQL / T-SQL [For building the datasource]
⚡PowerBI Desktop [For building the PowerBI dashboard/report]
⚡PowerQuery Editor [For data-transformation/data-modeling]
⚡PowerBI Service [For making the report accessible on the web without PowerBI login]
⚡Multipage fully Interactive Report [For drawing insights and analysis]
## Introduction
AdventureWorks is an online retailer that sells Bikes and Biking related items such as bike parts, biking protective gear, articles of clothing, etc.
Online sales transactions, inventory, financials, customer and product information are captured in real-time in a transaction database.
At the End of the day after the closing of business, data from the transaction database is extracted, formatted, and then exported to a data warehouse database.
## Objectives
We have been asked by AdventureWorks to perform the in-depth data analysis for the years 2016 and 2017 and draw insight into company sales performance, customers, and products so that they can build a strategy around it to generate more revenue and higher profits.
## Dataset
AdventureWorks makes data available strictly through its datawarehouse-database for any data analysis. The real-time transaction database is not directly accessible
## Budget Data
AdventureWorks allocates a monthly budget for sales. The company sets a monthly target against which sales performance for a given month is expected to be measured as a key KPI for success. The budget/target is decided and fixed yearly in advance. Note that the budget is decided by the company's top management once a year, and it's not a part datawarehouse-database.
Exploratory Data Analysis (EDA) and Data Preparation [SQL]
To understand, be familiar with and check the sanity of the given data, the first step is EDA. In this project, the initial data exploration has been carried out using SQL. Here, in general, we are...

## EDA
Here we explore the datawarehouse-database to identify the dimension and fact tables we'd need as our data source. We further explore the identified tables to understand their structure and their data. Based on the requirements, we identified the tables below as our primary data source
## Data Preparation
We are going to import data directly from the database into PowerBI. For this, we could directly execute the SELECT statement joining all the relevant tables from PowerBI. However, to make it cleaner, we'll create database VIEWS that'd encapsulate the required SQL, and finally, we need to execute a simple SELECT * from <view> statement from PowerBI. This approach has the following advantages...

## Makes PowerBI side of data import simpler
We do not need to build, manage and schedule any extract (CSV or XLS files) to pull the latest data from the database and provide it to the PowerBI report since we are directly removing data from the database whenever the PowerBI report is refreshed it'll get the latest data.
We are decoupling the data selection logic from PowerBI. If the selection logic changes, we need to modify the underlying database view; no changes are required in PowerBI as long as the selected columns remain the same.
