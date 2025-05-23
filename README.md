# 🏡 Airbnb Property Analysis: Evaluating Investment Viability and Returns  

## 📌 Objective  
This project focuses on identifying 
- **optimal properties for Airbnb investment**
- **forecasting potential earnings**

## 🛠 Tool Stack  
🔹 **Power BI** | **MS Excel**  

## 🔍 Approach  

### 1️⃣ Data Structuring & Preparation  
- Dataset includes six worksheets:  
  - **Places** (fact table)  
  - **Hosts, Neighborhood** (dimension tables)  
- Ensured **data type integrity** across all columns  

### 2️⃣ Data Cleaning & Modeling 
- Standardized and optimized dataset using Excel functions:  
  - **IFS, SWITCH, VLOOKUP, MATCH, INDEX**, and date functions  
- Managed missing/null values using **ISBLANK and REPLACE**  
- Dataset includes six worksheets:  
  - **Places** (fact table)  
  - **Hosts, Neighborhood**, **P&L** (dimension tables)  
- Ensured **data type integrity** across all columns  
- Created relationships between Places, Hosts and Neighborhood in Power BI's data model using fact and dimension tables for optimized queries.

### 3️⃣ Developed Key Dax Measures 
**Total Hosts** = COUNT(Host[Year Joined])
**Total Superhost** = CALCULATE(
    COUNT(Host[Year Joined]),
    Host[Superhost] = "Yes")
**Superhost %** = DIVIDE([Total Superhost], [Total Hosts])
**Total Neighbourhood** = CALCULATE(DISTINCTCOUNT(Neighbourhood[Neighborhood]))
**Price per guest** = DIVIDE(
    SUM(Place[Price]),
    SUM(Place[Accommodates]))
**Average Rating** = AVERAGE(
    Place[Rating])

### 4️⃣ Visualization 
• 	**Line and Bar Chart Chart:** Shows superhost % and total hosts over time .
•   **Waterfall Chart:** Highlights estimated net income 
•   **Bar Chart:** Displays price per guest of different places 
•   **Line Chart:** Average rating of different places  
•   **Slicers:** Allow filtering by district, date, size, room type and superhost

## 📊 Findings & Insights 🏡  
- **Chelsea is the best neighborhood** for renting out a property on Airbnb, offering optimal returns.  
- **Superhost percentage has declined** from **60% in 2008 to 32% in 2020**, indicating shifts in host quality and competition over time.  
- **Estimated annual earnings** after expenses amount to **$9,672**, providing a realistic view of profitability.  

