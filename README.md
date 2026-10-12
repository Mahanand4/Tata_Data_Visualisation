# Tata Data Visualisation

## Project Overview

This project was completed as part of the Tata Data Visualisation Virtual Experience, focusing on analysing online retail transaction data and converting the analysis into meaningful business insights.
The objective was to explore revenue trends, country-level performance, customer revenue contribution, and geographic demand using Microsoft Power BI.
The analysis was designed to support business decision-making by identifying sales patterns, high-performing markets, valuable customers, and potential areas for growth.

---

## Business Objective
The business required an analysis of online retail transaction data to help senior stakeholders understand:
- Analyze overall revenue performance and monthly revenue trends.
- Identify the products contributing the most to total revenue.
- Measure the revenue contribution of the top 10 customers.
- Calculate Average Order Value (AOV).
- Identify high-revenue and low-revenue months.
- Compare revenue performance across countries.
- Investigate potential growing and declining markets.
- Support conclusions with numerical evidence.
- Provide actionable business recommendations.

---

## Business Questions

### Q1. How does revenue trend over time?

The analysis examines monthly revenue patterns and identifies periods of higher and lower sales activity throughout the year.

### Q2. Which are the top 10 countries by revenue and quantity sold, excluding the United Kingdom?

The analysis compares countries based on revenue generated and quantity purchased to identify important international markets.

### Q3. Who are the top 10 customers by revenue?

The analysis identifies the customers contributing the highest revenue and examines the distribution of revenue across these customers.

### Q4. Which countries show strong product demand and potential expansion opportunities?

A geographic visualisation was used to understand product demand across countries, excluding the United Kingdom to focus on international opportunities.

---

## Dataset

 **InvoiceNo:** Unique transaction or invoice identifier.
- **StockCode:** Product identifier.
- **Description:** Product description.
- **Quantity:** Number of units purchased.
- **InvoiceDate:** Transaction date and time.
- **UnitPrice:** Price per unit.
- **CustomerID:** Customer identifier.
- **Country:** Country associated with the transaction.

A Revenue field was used to analyze sales performance.
---

## Data Preparation
The dataset was prepared before visualisation to improve the quality and relevance of the analysis.

The main preparation steps included:
- Removed transactions containing negative quantities.
- Removed transactions containing negative unit prices.
- Focused the analysis on valid sales transactions.
- Used the cleaned data for revenue, quantity, customer, country, and geographic analysis.

---

## Tools & Technologies

### Microsoft Power BI

Used for:
- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Data Cleaning and Transformation
- Exploratory Data Analysis
- Data Visualization
- KPI Development
- Business Intelligence and Reporting

##  Project Methodology

###  Data Import

Imported the Online Retail dataset into Power BI for data preparation, analysis, and dashboard development.

###  Data Cleaning and Transformation

- Reviewed the dataset for missing and invalid values.
- Examined data types and transaction fields.
- Converted InvoiceDate to the appropriate date format for time-based analysis.
- Checked numeric fields, including Quantity and UnitPrice.
- Reviewed missing dates and other data-quality issues.
- Prepared the data for revenue, customer, product, and market analysis.

###  Revenue Calculation
Revenue was calculated using the following formula:
Revenue = Quantity × UnitPrice

### Data Analysis
Analyzed retail transactions to identify monthly revenue fluctuations, high-performing products, customer revenue contribution, average order value, and country-level performance.

### Dashboard Development

Created Power BI report pages covering:
- Revenue Analysis
- Product Revenue Analysis
- Market Analysis
The report includes KPI cards, bar charts, monthly revenue trends, and written business insights.

## DAX Measure

### Average Order Value (AOV)

The following DAX measure calculates revenue per distinct invoice:
```dax
Average Order Value =
DIVIDE(
SUM('Online Retail Data Set'[Revenue]),
DISTINCTCOUNT('Online Retail Data Set'[InvoiceNo])
)
```

**Interpretation:** Average Order Value represents total revenue divided by the number of distinct invoices under the selected report filters.The result depends on the filters applied and how cancellations or credit notes are handled in the dataset.

##  Key Performance Indicators (KPIs)
- Total Revenue
- Average Order Value (AOV)
- Top 10 Customer Revenue Contribution
- Top 10 Product Revenue Contribution
- Monthly Revenue Performance
- Country-Level Revenue Performance

##  Key Findings and Analysis

###  Revenue Analysis
- The dashboard displays total revenue of approximately **1.60M**.
- Monthly revenue analysis highlights fluctuations across the observed period. May and November 2011 recorded strong revenue performance, while August 2011 showed a lower value than May.
- These differences provide opportunities to investigate the products, customers, and markets associated with revenue changes.

###  Product Revenue Analysis
- The Top 10 Products by Revenue chart identifies the products generating the highest revenue.
- The Top 10 products contribute approximately **14.92% of total revenue**, according to the dashboard KPI.
- This analysis helps identify important revenue-generating products and supports product-level inventory and sales planning.

###  Customer Revenue Analysis
- The Top 10 customers contribute approximately **49.74% of total revenue**, according to the dashboard KPI.
- This indicates that a substantial share of revenue is associated with a relatively small group of customers.
- Customer contribution analysis can support customer retention, relationship management, and targeted marketing strategies.

###  Average Order Value
- The Average Order Value card displays approximately **791.21**.
- AOV measures average revenue per distinct invoice under the selected filters. It can help evaluate purchasing value and assess opportunities to increase the value of customer orders.

###  Market Analysis
- The dashboard compares revenue across countries, including the Netherlands, EIRE, Germany, France, and Australia.
- The Top 5 Countries by Revenue chart helps identify markets with strong revenue contributions. The monthly revenue trends chart supports comparisons of market performance over time.
- Further investigation is needed to establish the causes of market-level growth or decline.

##  Numerical Evidence
The following figures were recorded from the Power BI dashboard:
- **Total Revenue:** Approximately 1.60M.
- **Top 10 Customer Revenue Contribution:** 49.74% of total revenue.
- **Top 10 Product Revenue Contribution:** 14.92% of total revenue.
- **May 2011 Revenue:** 69,041.42, one of the highest monthly revenue values observed.
- **August 2011 Revenue:** 32,277.74, showing a decline compared with May.
- **November 2011 Revenue:** 66,241.79, showing another strong revenue month.
- **December 2011 Revenue:** 52,554.01, lower than November.

These figures provide numerical support for the revenue, product, and customer analysis.The monthly values show revenue fluctuations, but they do not independently establish the causes of those changes or prove recurring seasonal patterns.

##  Business Impact
This project demonstrates how Power BI can transform retail transaction data into meaningful business intelligence.
The dashboard supports:

- Monitoring overall revenue performance.
- Identifying important products and customers.
- Evaluating average order value.
- Comparing country-level market performance.
- Investigating monthly revenue fluctuations.
- Supporting inventory and promotional planning.
- Making evidence-based business recommendations.

## Skills Demonstrated
- Data Cleaning and Transformation
- Power Query
- DAX Measures
- KPI Development
- Revenue Analysis
- Product Performance Analysis
- Customer Revenue Analysis
- Time-Series Analysis
- Market Performance Analysis
- Dashboard Design
- Data Visualization
- Business Insight Generation
- Data-Driven Decision-Making

---

##  Top 10 Countries by Revenue and Quantity

### Objective

Identify the strongest international markets based on revenue and quantity sold, excluding the United Kingdom.

### Visualisation
A clustered column chart compares revenue and quantity across the top 10 countries.

---

##  Top 10 Customers by Revenue

### Objective
Identify the customers contributing the highest revenue.

### Visualisation
A column chart ranks the top 10 customers according to revenue generated.

##  Product Demand by Country

### Objective
Understand geographic differences in product demand and identify markets that may require further investigation.

### Visualisation
A geographic map was used to display product demand based on quantity purchased, excluding the United Kingdom.Larger bubbles represent countries with higher purchase quantities.

### Key Insight
The analysis shows strong demand across several European markets, particularly the Netherlands, Ireland, Germany, and France. Other markets also show demand, although at comparatively lower levels.

### Business Implication
The business can investigate these markets further using:

- Customer research
- Market research
- Localised marketing
- Pricing analysis
- Product-demand analysis
- Distribution considerations

---

# Key Insights

### Revenue
- Monthly revenue varies throughout the year.
- May represents one of the strongest revenue periods.
- November also shows strong revenue performance.
- February and August show comparatively lower revenue.

### Countries
- The Netherlands and Ireland are among the strongest international markets.
- Germany and France also contribute significant revenue and quantity sold.
- Several European countries demonstrate strong demand.

### Customers
- Revenue is concentrated among a group of high-value customers.
- Customer ID 14646 is the highest-revenue customer shown in the analysis.
- Maintaining relationships with high-value customers can support recurring revenue.

### Geographic Demand
- European markets account for a significant portion of the international demand shown in the analysis.
- Markets with lower demand should be evaluated further before making expansion decisions.

---

# Business Recommendations

1. Plan Around Seasonal Revenue Patterns
2. Use historical revenue patterns to support inventory and marketing planning during stronger sales periods.
3. Strengthen High-Performing International Markets Continue monitoring markets such as the Netherlands, Ireland, Germany, and France through targeted campaigns and customer-retention  initiatives.
4. Focus on High-Value Customers Develop retention strategies for customers generating significant revenue, including personalised communication and loyalty initiatives.
5. Diversify the Customer Base While retaining high-value customers, continue developing new customer segments to reduce dependency on a limited number of customers.
6. Investigate Lower-Demand Markets
   Before expanding into lower-performing regions, conduct additional research into:
- Product demand
- Pricing
- Customer preferences
- Competition
- Market potential

7. Use the Dashboard for Ongoing Monitoring
The Power BI dashboard can be used as a recurring management tool to monitor:
- Revenue trends
- Country performance
- Customer contribution
- Geographic demand

---

# Project Outcome
This project demonstrates my ability to:
- Understand business requirements
- Clean and prepare transactional data
- Analyse sales performance
- Create meaningful Power BI visualisations
- Identify business trends and patterns
- Analyse customer and country performance
- Translate data findings into business recommendations
- Communicate analytical results to business stakeholders

---

## Challenges & Limitations
1. Incomplete December data:The dataset contains incomplete transaction records for December 2011. Therefore, December revenue and sales should be interpreted cautiously and should not be directly compared with complete months without considering data completeness.
Data quality issues: The raw transaction data required data cleaning and preparation before analysis. Inconsistent or missing values had to be identified and handled to ensure reliable reporting.
2. Limited historical period: The available data covers a limited period, which restricts the ability to perform long-term trend and year-over-year analysis.
3. Limited business context: The dataset primarily contains transaction-level information. Additional information such as marketing activities, pricing strategy, product costs, inventory levels and customer demographics was not available, making it difficult to determine the exact reasons behind some trends.
4. Revenue-focused analysis: The analysis mainly evaluates sales/revenue performance. Since detailed cost and expense information is not available, profitability and margin analysis could not be performed comprehensively.
5. Customer behaviour limitations: Customer analysis is based on recorded purchase transactions. The dataset does not provide sufficient information about customer preferences, demographics or reasons for purchasing behaviour.
6. Geographic analysis limitations: Country-level differences in sales can be identified, but the available data does not explain external factors such as market size, competition, local demand or economic conditions that may influence performance.
Limited ability to establish causation: The analysis identifies trends, patterns and relationships in the data, but these observations do not necessarily prove that one factor directly caused another.
7. Data-driven recommendations: The recommendations are based on the information available in the dataset. Additional business and operational data would be required before implementing major strategic decisions.

---

# Project Files

The repository contains:

- **Power BI Analysis File** - Interactive Power BI analysis
- **Tata_Data_Visualisation_Final.pdf** - Detailed final project report
- **TATA Certificate.pdf** - Virtual experience completion certificate
- **README.md** - Project overview, analysis, insights, and recommendations

---

# GitHub Repository

https://github.com/Mahanand4/Tata_Data_Visualisation

## Certificate

[Tata Data Visualisation Virtual Experience Certificate](TATA%20Certificate.pdf)
