# Corporates Guide 

A Power BI project built using the **Superstore Practice Dataset** to demonstrate data cleaning, data modeling, DAX calculations, and interactive dashboard creation.

---

## 📌 Project Overview

This project showcases the complete Power BI workflow, including:

- Data Import & Cleaning using Power Query
- Star Schema Data Modeling
- DAX Calculated Columns & KPI Measures
- Interactive Sales Dashboard Design

---

## 📂 Dataset

- **Dataset:** Superstore Practice Dataset
- **Domain:** Retail Sales
- **Tool Used:** Microsoft Power BI Desktop

---

## 🔹 Task 1 – Data Import & Cleaning

The dataset was cleaned using **Power Query** by performing the following operations:

- Imported Excel dataset into Power BI
- Removed duplicate records
- Checked and handled missing (null) values
- Corrected data types
- Split **Customer Name** into **First Name** and **Last Name**
- Renamed columns to business-friendly names
- Loaded the cleaned data into the Power BI model

---

## 🔹 Task 2 – Data Modeling

A Star Schema was created for efficient analysis.

### Fact Table
- Orders

### Dimension Tables
- DimCustomer
- DimProduct
- DimLocation
- DateTable

### Data Modeling Steps

- Created dimension tables using DAX
- Created Date Table using `CALENDAR()`
- Established one-to-many relationships
- Set Cross Filter Direction to **Single**
- Organized the model as a Star Schema

---

## 🔹 Task 3 – DAX Calculations

### Calculated Column

```DAX
Profit Status =
IF(Orders[Profit] > 0, "Profit", "Loss")
```

### KPI Measures

```DAX
Total Sales = SUM(Orders[Sales])

Total Profit = SUM(Orders[Profit])

Total Orders = COUNT(Orders[Order ID])

Total Customers = DISTINCTCOUNT(Orders[Customer ID])

Average Sales = AVERAGE(Orders[Sales])
```

### CALCULATE Measure

```DAX
West Region Sales =
CALCULATE(
    [Total Sales],
    Orders[Region] = "West"
)
```

### Time Intelligence Measure

```DAX
YTD Sales =
TOTALYTD(
    [Total Sales],
    DateTable[Date]
)
```

---

## 🔹 Task 4 – Interactive Dashboard

The dashboard contains:

- KPI Cards
- Clustered Column Chart
- Line Chart
- Table Visual
- Region Slicer
- Category Slicer
- Drill-through Page
- Cross-filtering between visuals
- Professional formatting and theme

---

## 📊 Dashboard Features

- Sales Performance Overview
- Monthly Sales Trend
- Category-wise Sales Analysis
- Product-wise Details
- Dynamic Filtering using Slicers
- Interactive Drill-through Navigation

---

## 🛠️ Tools & Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX
- Star Schema Data Modeling

---

## 📈 Outcome

Successfully developed an interactive Power BI Sales Dashboard by applying data cleaning, data modeling, DAX calculations, and visualization techniques. The dashboard provides meaningful business insights with dynamic filtering and interactive reporting.

---
