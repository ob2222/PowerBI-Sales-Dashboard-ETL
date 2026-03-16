# Sales Analysis Executive Dashboard (Power BI / ETL)

## 📌 Project Overview
This project showcases an end-to-end data analysis workflow, from extracting and cleaning messy raw data to building a relational data model and creating an interactive Executive Dashboard in Power BI. The goal of the dashboard is to provide business owners with a clear view of revenue trends, product performance, and sales distribution.


## 🛠 Tools & Technologies
- **Microsoft Power BI** (Data Visualization)
- **Power Query** (ETL: Extract, Transform, Load)
- **Data Modeling** (Star Schema, Relational Databases)
- **DAX / Custom Columns** (Data Manipulation)

## ⚙️ Workflow & Steps Performed

### 1. Data Extraction & Cleaning (Power Query)
- Combined three separate Excel files containing monthly sales data into a single fact table (`Sales_Fact`).
- Standardized store names by fixing case inconsistencies (e.g., converted everything to Proper Case).
- Filtered out empty rows that were causing data structure issues.
- Handled missing and `null` values by categorizing them as "Без категории" (Uncategorized) and "Без ТМ" (No Brand) to avoid losing any transaction data during revenue calculation.
- Created a custom calculated column to extract and track the "Month" of sales, as explicit dates were missing from the raw data.

### 2. Data Modeling (Star Schema)
- Designed a relational data model by extracting dimension attributes (Product Name, Category, Brand) from the main sales table.
- Created a unique dimension table (`Product_Dict`) and removed all duplicates to ensure data integrity.
- Established a **One-to-Many (1:*) relationship** between the `Product_Dict` (Dimension) and `Sales_Fact` (Fact) tables.
- Hid dimension columns in the Fact table to prevent end-user confusion and maintain a clean model view.

### 3. Data Visualization (Executive Dashboard)
- Designed a clean, "no visual noise" layout following the Z-pattern for optimal readability.
- **KPI Cards:** Displayed high-level metrics (Total Revenue, Total Items Sold).
- **Trend Analysis:** Built a line chart to visualize revenue dynamics across months.
- **Top Performers:** Used bar charts to highlight top-selling categories and stores.
- **Detailed Matrix:** Created a detailed breakdown table with formatted numbers for deep-dive analysis.
- **Interactive Slicers:** Added synchronized filters for Month, Category, and Brand.

## 💡 Business Value
This dashboard allows stakeholders to instantly track monthly performance, identify the most profitable product categories, and filter sales data dynamically without needing to interact with raw Excel files.
