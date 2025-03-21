# Power BI Dashboard: Bike Store Sales Analysis

The Power BI dashboard presents an analytical view of the sales performance of a Bike Store. It contains detailed visualizations covering various business metrics, like revenue trends, brand/category performance, customer contributions, store-wise revenue, and city-wise sales.

Data Sources and Data Modeling
Datasets Used:
- **Bike store db**
- **Tables: Brands, Categories, Customers, Order_Items, Orders, orders_delivered, Products, Staffs, Stocks, Stores**

Data Modeling Process:
- **Relationships Created:**
   - **One-to-Many relationships**
      - **Customers ➔ Orders**
      - **Orders ➔ Order_Items**
      - **Products ➔ Order_Items**
      - **Brands, Categories ➔ Products**
      - **Stores ➔ Staffs, Orders**
  - **Proper Primary Key-Foreign Key mappings done.**
- **Star Schema approach followed: Fact table (Order_Items) in the center linked to dimension tables (Products, Customers, Stores, etc.).**

Analysis and create a dashboard report.
