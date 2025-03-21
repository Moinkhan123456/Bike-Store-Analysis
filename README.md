# Power BI Dashboard: Bike Store Sales Analysis

The Power BI dashboard presents an analytical view of the sales performance of a Bike Store. It contains detailed visualizations covering various business metrics, like revenue trends, brand/category performance, customer contributions, store-wise revenue, and city-wise sales.

Data Sources and Data Modeling
Datasets Used:
- **Bike store db**
- **Tables: Brands, Categories, Customers, Order_Items, Orders, orders_delivered, Products, Staffs, Stocks, Stores**

1. **Data Modeling Process:**
- **Relationships Created:**
   - **One-to-Many relationships**
      - **Customers ➔ Orders**
      - **Orders ➔ Order_Items**
      - **Products ➔ Order_Items**
      - **Brands, Categories ➔ Products**
      - **Stores ➔ Staffs, Orders**
  - **Proper Primary Key-Foreign Key mappings done.**
- **Star Schema approach followed: Fact table (Order_Items) in the center linked to dimension tables (Products, Customers, Stores, etc.).**

2. **Data Cleaning & Data Processing**
  - **Steps Taken:**
      - **Removed unwanted columns and null values from datasets.**
      - **Standardized naming conventions and ensured consistency.**
      - **Filtered unnecessary date ranges (Used slicers in the dashboard for order_date filter).**
      - **Removed duplicate entries, handled blank fields using Power Query Editor.**
      - **Converted data types (like dates, currency, etc.) to appropriate formats.**

3. **DAX Functions & Calculated Columns**
DAX Calculations Performed:
- **New Measures:**
   - **Total Revenue = SUM(Order_Items[Revenue])**
   - **Total Customers = DISTINCTCOUNT(Customers[Customer_ID])**
- **Calculated Columns:**
   - **Extracted Year, Month, City, Category_Name from raw columns for visualization purposes.**
   - **Created revenue-related calculated columns per product, brand, and staff using DAX:**
        - **Revenue_Per_Product = RELATED(Products[Product_Price]) * Order_Items[Quantity]** 
   - **Goal/KPI indicator using DAX for Year-over-Year comparisons (e.g., Goal: +3010% in screenshot).**

4. **End-to-End Process Workflow**
- **1.Data Import:**
     - **Connected to the Bike Store database using Power BI's SQL Server connector.**
- **2.Data Cleaning:**
     - **Removed unnecessary columns, handled null values, corrected data types.**
- **3.Data Modeling:**
     - **Established clear relationships between tables using star schema.**
- **4.DAX Calculation:**
     - **Created measures for revenue, customer count, goal targets.**
     - **Built calculated columns for derived metrics.**
- **5.Data Visualization:**
     - **Built interactive charts, KPIs, slicers, maps, and tree visualizations.**
- **6.Dashboard Design:**
     - **Applied dark-themed design, used consistent color schemes.**
     - **Created separate pages (Page 1, 4, 5, Tooltip Page) for focused insights.**

Dashboard Interaction <a href="https://github.com/Moinkhan123456/Bike-Store-Analysis/blob/main/Screenshot%20(9).png">View Dashboard of Sales Bike Store</a>
<br>
Dashboard Interaction <a href="https://github.com/Moinkhan123456/Bike-Store-Analysis/blob/main/Screenshot%20(10).png">View Dashboard</a>
<br>
Dashboard Interaction <a href="https://github.com/Moinkhan123456/Bike-Store-Analysis/blob/main/Screenshot%20(11).png">View Dashboard of Sales Bike Store</a>
<br>
Analysis and create a dashboard report.
