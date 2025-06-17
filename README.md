# - 🏠Danish-Housing-Market-Insights-with-Power-BI-Google-BigQuery

(Add dashboard link here once published — e.g., Power BI Service or NovyPro)

## 📌 Problem Statement
This project focuses on analyzing Denmark’s real estate transaction data to uncover trends in housing sales, price fluctuations, and regional dynamics. Using data hosted in Google BigQuery, the goal is to explore the market through dynamic Power BI dashboards, drawing actionable insights around pricing, interest rates, and buyer behavior.

The project demonstrates how cloud-based data platforms like BigQuery can be integrated with Power BI to enable scalable, interactive business intelligence solutions in the real estate sector.

## 🔄 Steps Followed
#### 1. Data Sourcing & Environment Setup
Created a Google Cloud account with BigQuery access.

Loaded the housing dataset (CSV format) from a local machine to BigQuery:

Created a dataset named 1

Uploaded and auto-detected schema for the table housing

### 2. Data Connection (Power BI + BigQuery)
Connected Power BI Desktop to BigQuery using the Google BigQuery connector.

Selected Import mode for faster processing and full DAX functionality.

### 3. Data Cleaning (Power Query Editor)
Performed data profiling and transformation inside Power BI:

Replaced nulls in columns like city, annual_inflation, and yield_on_mortgage with values like "Unknown" or mode values.

Verified and corrected data types for date, numeric, and text fields.

Standardized column profiles, validated unique keys, and corrected formatting inconsistencies.

### 4. SQL-based Transformation (BigQuery)
Used SQL in BigQuery to:

Create a duplicate test table from housing

Update records (e.g., set sqm = 100 where no_rooms = 3)

Analyze sales by type using aggregate functions (GROUP BY)

### 4. SQL-based Transformation (BigQuery)
5. Feature Engineering (Power BI – DAX)
Created measures and calculated columns for:

📈 YoY Sales Growth

🏷️ Offer Price (calculated from purchase price and % change)

💰 Median Sales Price Change by Region

📦 Units Sold in Latest Year and Quarter

🕒 Last 12-Month Sales

🌍 Sales by Region (ignoring filters)

📅 YTD Sales (using TOTALYTD)

All measures were moved to a dedicated "Measures Table" for better model organization.

## 📊 Dashboard Design & Visuals

### Page 1 – House Market Overview

🔹 Line Chart: YoY Sales Growth by Sales Type

🔹 Scatter Plot: Offer Price vs Purchase Price

🔹 Key Influencers: Factors influencing price increase/decrease (e.g., age over 113)

🔹 Top Segments: Market clusters by price category

🔹 Bar Chart: Median Price Change by Region

🔹 Cards: Units Sold in Latest Quarter & 12-Month Sales

### Page 2 – Sales Performance

🔹 Bar Chart: Total Sales by Region (with ALLEXCEPT logic)

🔹 Table Visual: Daily Purchase Price vs Cumulative YTD Sales

Each visual includes:

Conditional formatting

Tooltips

Branded backgrounds and headers

Clean UI with consistent styling

### Page 3 – House Type Analysis

🔹 Bar Chart: Average Offer Price vs Purchase Price by House Type

🔹 Bar Chart: Inflation, Interest, and Yield Rates by House Type

🔹 Combo Chart: Average SQM and SQM Price by House Type (dual axis)

🔹 Slicers: City, Area, Region, Sale Type for dynamic filtering

## 🛠️ Tools & Technologies Used
Purpose	Tools/Tech
Data Storage	Google BigQuery
Data Visualization	Power BI Desktop
Scripting/Queries	SQL (BigQuery), DAX, Power Query (M)
Data Cleaning	Power Query, SQL (BigQuery)
Cloud Integration	GCP + Power BI Connector

## 🌟 Outcome
Built an interactive real estate analysis dashboard connected to BigQuery.

Visualized market dynamics like YoY growth, regional price shifts, and sales patterns.

Derived offer price using reverse % change calculation.

Used advanced DAX measures and BigQuery SQL for analytical insights.

Delivered a polished Power BI project, ready for stakeholder or recruiter review.

## 🧠 Key Learnings
Integrating cloud data platforms (BigQuery) with Power BI dashboards.

Cleaning and transforming large datasets in Power Query and SQL.

Writing advanced DAX measures for time intelligence and performance analysis.

Creating professional-grade dashboards with interactivity and storytelling.
