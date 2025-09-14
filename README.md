# Business Intelligence Data Warehouse Project  

## Overview  
This project was developed as part of **IMT 577: Business Intelligence Systems**.  
It focuses on building a dimensional data warehouse to support analytical insights for retail store operations, addressing:  

- Sales performance analysis  
- Fair bonus allocation  
- Weekday sales trends  
- Market expansion recommendations  

The solution integrates raw transactional data, sales targets, and master data into a dimensional model using **Snowflake**.  
Secure views were created for access, and **Tableau dashboards** were built for interactive analysis.  

---

## Objectives  
- Assess store-level performance against sales targets.  
- Recommend fair allocation of a $2M bonus pool.  
- Analyse weekday sales patterns for efficiency.  
- Evaluate expansion opportunities.  
- Deliver dashboards for data-driven decision-making.  

---

## Project Schedule  
- **Apr 23, 2025** – Project planning & scope
- **May 1, 2025** – Data profiling & source identification  
- **May 7, 2025** – Dimensional model design (Star Schema, ERD, Fact & Dimension tables)  
- **May 14, 2025** – Data transformation & loading  
- **May 21, 2025** – Data access layer & secure views  
- **May 27, 2025** – Dashboard development & insights  
- **May 31, 2025** – Group synthesis & presentation prep  
- **Jun 6, 2025** – Final presentation & recommendations  

---

## Data Architecture  

### Fact Tables  
- **Fact_SalesActual** – transaction-level sales
- **Fact_ProductSalesTarget** – product-level sales targets
- **Fact_SRCSalesTarget** – channel/store-level targets
### Dimension Tables  
- **Dim_Date** – time attributes  
- **Dim_Product** – product details  
- **Dim_Store** – store details  
- **Dim_Customer** – customer profiles  
- **Dim_Reseller** – reseller details  
- **Dim_Channel** – sales channel classification  
- **Dim_Location** – location and geography

### Design Notes  
- **Snowflake schema** with normalized location data  
- **Surrogate keys** for performance & integrity  
- **Secure views** for reporting & Tableau integration

---

## Analysis Framework  
Business questions addressed  
1. How are Stores 10 & 21 performing vs. targets?  
2. How should a $2M bonus pool be allocated fairly?  
3. What weekday sales patterns can be identified?  
4. Should new stores be opened, and where?  

---

## Tools & Technologies  
- **Azure Blob Storage** – source data storage  
- **Snowflake** – data warehouse (ELT, schema, secure views)  
- **SQL** – transformations, data cleansing, fact/dim table creation  
- **Tableau** – dashboards for analysis & insights

---

## Dashboards  
Built with Tableau for dynamic insights:  
- Store performance vs. targets  
- Bonus allocation distribution  
- Weekday sales patterns  
- Expansion opportunities  

Dashboard Link:  [Store Performance](https://public.tableau.com/app/profile/apeksha.tejwani/viz/IMT577_DW_Apeksha_Tejwani_Dashboard_Story/StorePerformance)  

---

## Key Insights  
- Stores 10 & 21 **underperformed in 2014**, achieving ~82% and ~76% of targets 
- Both showed **positive growth trends**, so closures were not recommended
- Bonus allocation was **proportional to performance ratios**, rewarding high achievers
- Weekday sales peaked on **Mondays & Sundays**, dipped midweek
- Expansion analysis identified **Georgia (Store 5)** as a high-potential location

---

## How to Run  

1. Clone or download project files.  
2. Load raw CSV data into **Snowflake staging tables** (via Azure Blob Storage).  
3. Run SQL scripts to:  
   - Create Dimension & Fact tables.  
   - Load transformed data.  
   - Create secure views for reporting.  
4. Connect **Tableau** to Snowflake views for dashboarding.  

---

## License  
This project was developed for academic purposes under **IMT 577: Business Intelligence Systems**.  
It is not licensed for commercial use.  

---

