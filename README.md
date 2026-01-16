# 🙂 What I bring to the table

I spent 10 years as an electronics technician, then intentionally transitioned into BI. I’ve built strong fundamentals in data modeling, ETL, and analytics across operations, finance, and IT. Now my focus is scaling those skills into enterprise and consulting environments.

- My name is Cyrus, and I’m based in Lapu-Lapu City with my wife and kids—they inspire me to give my best every day. 

- Professionally, I specialize in Power BI, helping businesses streamline and automate their reporting processes.

- I handle end-to-end Power BI solutions, including understanding requirements, ETL, data modeling, dashboarding, testing and validation, and maintaining Power BI assets.

- Outside of work, I honestly enjoy catching up on sleep to recharge, but I always make sure to spend quality time with my family.

- I believe data is the new oil, and my goal is to keep growing in this field while using my experience to inspire others to embrace data as a driver of transformation.

<img width="63" height="57" alt="image" src="https://github.com/user-attachments/assets/85f2242f-797b-4d22-8664-b0ccb8375e2c" />

**At D&E Air Conditioning**

*D&E is a mechanical services and air conditioning solutions leader in Australia. They supported large-scale projects: commercial buildings, hotels, mall, hospitals*

I worked closely with operations and business development teams, helping streamline their reporting processes for project tracking, EHS/health & safety, tools inventory, tender phasing, and revenue forecasting.

- I gathered business requirements, standardized data entry, and prepared data before building optimized data models, executive dashboards, and paginated reports.
  
- The projects significantly reduced manual effort in weekly and monthly reporting processes, improved team coordination across departments, increased confidence in the data, and enabled faster decision-making.

*While Fabric isn’t yet adopted at D&E, I’ve built and tested Fabric-based architectures in parallel to stay current.*

---
<img width="65" height="65" alt="image" src="https://github.com/user-attachments/assets/715c3a36-ba4a-4a4e-889b-0cc15d579e0b" />

**At Lexmark** | 
I worked at Lexmark as a Finance Business Analyst, partnering closely with finance stakeholders to gather requirements and translate them into BI solutions using data from the business warehouse.

- I processed and modeled data, then delivered dashboards such as OPEX Analytics, Revenue Analytics, and Cost Center Analytics, providing a quick view of top cost and revenue drivers with drill-down analysis.

- This reduced manual effort and streamlined monthly reporting, allowing analysts to focus more on analysis and insights.

--- 
<img width="195" height="38" alt="image" src="https://github.com/user-attachments/assets/b1f37ace-f7a0-4d6f-85f5-c63e7ef1e6b7" />

- I worked part-time at AvantGuard LLC, integrating data from IT operations and endpoint management tools like HaloPSA, NinjaOne, and Cove to build internal dashboards that monitored users and machines and enabled cross-validation across systems.
  
- I later worked with one of their clients to migrate from Excel-based reporting to Power BI, handling ETL, dimensional modeling, report and dashboard development, including paginated reports and executive dashboards like the Income Statement and P&L.

- This provided quick-glance insights and faster decision-making through executive summaries with drill-down analysis.

--- 
<img width="198" height="46" alt="image" src="https://github.com/user-attachments/assets/0397d34a-fe87-4d46-83a5-e4a4b4ac650e" />

**Moderno Plant X** 
- Built near OEE dashboards to monitor machine performance and equipment utilization.

--- 
<img width="304" height="81" alt="image" src="https://github.com/user-attachments/assets/378e878b-e56d-4d0f-9764-61d5dc487668" />

**At Excigence** 
- Built a Python desktop application using Tkinter for the GUI and Pandas and Matplotlib for data preparation, analysis, and automated report generation for final testing of electronics and electrical devices.

---

# Senior Consultant – BI & Analytics Cheat Sheet

A quick reference for **Power BI, DAX, T-SQL, Data Modeling, and Consulting Prep**.

---

## 1️⃣ Power BI Components

| Component | Key Points | Tips / Notes |
|-----------|------------|--------------|
| **Data Modeling** | Star schema, Snowflake schema, fact & dimension tables, relationships | Optimize for query performance; avoid bi-directional unless necessary |
| **Power Query (M)** | Data cleaning, transformations, merging, appending | Use `Table.TransformColumns`, `Merge Queries`, `Append Queries`, parameterize queries |
| **DAX** | Measures, calculated columns, time intelligence | Common functions: `CALCULATE`, `FILTER`, `SUMX`, `ALL`, `RELATED`, `DATESYTD` |
| **Visualizations** | Dashboards, paginated reports, drill-downs, slicers | Keep user-friendly, use KPIs & conditional formatting for quick insights |
| **DirectQuery vs Import** | DirectQuery: real-time, Import: in-memory | Import is faster for complex calculations; DirectQuery good for large datasets |
| **Licensing & Workspaces** | Pro vs Premium, workspace roles, permissions | Understand deployment, sharing, and security considerations |

---

## 2️⃣ T-SQL / SQL Server (Working Knowledge)

| Concept | Syntax / Example | Notes |
|---------|-----------------|------|
| **Create Table** | `CREATE TABLE Customers (ID INT, Name NVARCHAR(50), Country NVARCHAR(50));` | Defines new table |
| **Insert Data** | `INSERT INTO Customers (ID, Name, Country) VALUES (1, 'Cyrus', 'PH');` | Add rows |
| **Select Data** | `SELECT * FROM Customers;` | Retrieve rows |
| **Filtering** | `SELECT * FROM Customers WHERE Country='PH';` | WHERE clause |
| **Aggregations** | `SELECT Country, SUM(Sales) AS TotalSales FROM Sales GROUP BY Country;` | SUM, COUNT, AVG, MIN, MAX |
| **Joins** | `SELECT c.Name, o.Amount FROM Customers c INNER JOIN Orders o ON c.ID=o.CustomerID;` | INNER, LEFT, RIGHT, FULL OUTER |
| **CASE** | `SELECT Name, CASE WHEN Sales>1000 THEN 'High' ELSE 'Low' END AS Category FROM Sales;` | Conditional logic |
| **Subqueries** | `SELECT CustomerID FROM Sales WHERE SalesAmount > (SELECT AVG(SalesAmount) FROM Sales);` | Filter based on another query |
| **CTEs** | `WITH TopSales AS (SELECT CustomerID, SUM(Sales) AS Total FROM Sales GROUP BY CustomerID) SELECT * FROM TopSales WHERE Total>1000;` | Temporary result set |
| **Common Functions** | `GETDATE(), ISNULL(Column, 0), CAST(Column AS INT)` | Date, null handling, type conversion |
| **Order / Limit** | `SELECT * FROM Sales ORDER BY Total DESC;` | Sorting |
| **Update Data** | `UPDATE Customers SET Country='PHL' WHERE ID=1;` | Modify rows |
| **Delete Data** | `DELETE FROM Customers WHERE ID=1;` | Remove rows |

---

## 3️⃣ ETL / Data Pipeline Prep

| Step | Key Considerations |
|------|------------------|
| **Extract** | Source types: flat files, SQL Server, APIs, cloud services |
| **Transform** | Clean, standardize, merge, deduplicate; ensure data quality |
| **Load** | Into semantic model / Power BI dataset; optimize performance |
| **Incremental Refresh** | Only refresh changed data to improve efficiency |
| **Data Validation** | Cross-check totals, nulls, anomalies before report delivery |

---

## 4️⃣ DAX Functions Cheat

| Category | Common Functions | Notes / Example |
|----------|-----------------|----------------|
| **Aggregation** | `SUM`, `AVERAGE`, `COUNTROWS` | Standard calculations |
| **Filter & Context** | `CALCULATE`, `FILTER`, `ALL`, `ALLEXCEPT` | Modify row context for measures |
| **Time Intelligence** | `DATESYTD`, `SAMEPERIODLASTYEAR`, `TOTALYTD` | Year-to-date, growth comparisons |
| **Relationship** | `RELATED`, `RELATEDTABLE` | Pull data across tables |
| **Dynamic Measures** | `IF`, `SWITCH`, `ISBLANK` | Conditional or dynamic reporting |
| **VAR (scalar or table)** | `VAR SalesTable = FILTER(Sales, Sales[Amount]>100) RETURN SUMX(SalesTable, Sales[Amount])` | Temporary variable (like SQL CTE) |

---

## 5️⃣ Data Modeling / Best Practices

| Topic | Tips |
|-------|------|
| **Star Schema** | Single fact table with multiple dimension tables |
| **Normalization** | Avoid storing repetitive data in fact tables |
| **Calculated Columns vs Measures** | Prefer measures; calculated columns increase model size |
| **Relationships** | One-to-many, single-direction preferred for performance |
| **Optimizations** | Hide unnecessary columns, reduce cardinality, proper data types |

---

## 6️⃣ Client & Business Consulting Prep

| Area | How to Prepare |
|------|----------------|
| **Requirements Gathering** | Use structured templates; clarify metrics, KPIs, and data sources |
| **Communication** | Translate technical concepts into business terms |
| **Problem Solving** | Be ready to explain how you handled missing or inconsistent data |
| **Decision Support** | Show examples of dashboards that improved speed or quality of business decisions |

---

## 7️⃣ Sample STAR Stories (For Interview)

| Situation | Task | Action | Result |
|-----------|------|--------|--------|
| OPEX Analytics | Finance team had manual Excel reports | Migrated data to Power BI, built dashboards with drill-down | Reduced manual effort, enabled faster decision-making |
| IT Dashboard | Part-time BI project at AvantGuard | Integrated endpoint data, created monitoring dashboards | Improved cross-system validation, faster insights for operations |
| Revenue Forecasting | D&E Air Conditioning | Gathered requirements, standardized data, built executive dashboards | Improved coordination, faster top-driver insights |

---

## 8️⃣ Quick Tips for Interview

- Be ready to **walk through a full end-to-end Power BI project**: data prep → modeling → dashboard → report deployment  
- Highlight your **DP-600 Fabric certification** and PL-300 skills  
- Be confident explaining **T-SQL basics and working knowledge**  
- Show **consulting mindset**: requirement gathering, business impact, self-service enablement  
- Prepare questions about **client projects, tools, or processes** to show engagement  

---

*Prepared by Cyrus Baruc – Senior Consultant BI & Analytics Interview Prep*
