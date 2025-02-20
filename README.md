# Azure End to End Project

## 1. Project Overview

The objective of this project is to build a data pipeline that extracts customer and sales data from an on-premises SQL database, processes it in the cloud, and generates actionable insights through a Power BI dashboard. The dashboard will provide key performance indicators (KPIs) on gender distribution and product category sales, enabling stakeholders to filter and analyze data by date, product category, and gender.

## 2. Business Requirements
The business seeks to bridge a knowledge gap in customer demographics—specifically, gender distribution and its impact on product sales. The key requirements include:

Sales Analysis by Gender and Product Category: A dashboard showcasing total products sold, total sales revenue, and a breakdown of customers by gender.
Data Filtering: Functionality to filter data based on product category, gender, and date.
User-Friendly Interface: A seamless and intuitive interface for stakeholders to access and explore insights.

## 3. Solution Overview
To meet these requirements, the solution is structured into the following components:

### 1. Data Ingestion
Extract customer and sales data from an on-premises SQL database.
Load data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).
### 2. Data Transformation
Use Azure Databricks to clean and process the data.
Implement a Bronze, Silver, and Gold architecture for data refinement:
Bronze Layer: Raw data storage.
Silver Layer: Cleansed and structured data.
Gold Layer: Aggregated and enriched data for reporting.
### 3. Data Loading and Reporting
Load transformed data into Azure Synapse Analytics for analysis.
Develop a Power BI dashboard to visualize key insights on sales and demographics.
### 4. Automation
Schedule the pipeline to run daily to ensure timely updates of data and reports.
## 4. Technology Stack
Azure Data Factory (ADF): Orchestrates data movement and transformation.  
Azure Data Lake Storage (ADLS): Stores raw and processed data.  
Azure Databricks: Performs data transformation and processing.  
Azure Synapse Analytics: Provides data warehousing and SQL-based analytics.  
Power BI: Enables data visualization and reporting.  
Azure Key Vault: Manages credentials and secrets securely.  
SQL Server (On-Premises): Serves as the data source for customer and sales records.

## 5. Setup Instructions
Prerequisites
An active Azure account with sufficient credits.
Access to an on-premises SQL Server database.
#### Step 1: Azure Environment Setup
Create a Resource Group in Azure.
Provision the necessary services:
Deploy Azure Data Factory for data ingestion.
Set up Azure Data Lake Storage with bronze, silver, and gold containers.
Configure Azure Databricks and Azure Synapse Analytics for data processing.
Set up Azure Key Vault for secure credential management.
#### Step 2: Data Ingestion
Install SQL Server and SQL Server Management Studio (SSMS).
Restore the AdventureWorks database as a sample dataset.
Configure ADF pipelines to extract data from SQL Server and load it into the Bronze layer of ADLS.
#### Step 3: Data Transformation
Mount ADLS to Databricks for data access.
Develop Databricks notebooks to clean and aggregate data, transferring it through the Bronze, Silver, and Gold layers.
#### Step 4: Data Loading and Reporting
Load the Gold layer data into Azure Synapse Analytics for structured analysis.
Connect Power BI to Synapse and build interactive dashboards based on business requirements.
#### Step 5: Automation and Monitoring
Schedule ADF Pipelines to automate daily data refreshes.
Monitor performance using ADF and Synapse monitoring tools to ensure successful execution.
#### Step 6: Security and Governance
Implement Role-Based Access Control (RBAC) using Azure Entra ID (formerly Active Directory) to manage permissions.
#### Step 7: End-to-End Testing
Insert new records into the SQL database.
Validate that the pipeline processes data end-to-end and updates the Power BI dashboard accordingly.

## 6. Conclusion
This project delivers a scalable, automated, and secure data pipeline for analyzing customer demographics and their impact on sales. By leveraging Azure services, the solution ensures stakeholders always have access to real-time, data-driven insights.

