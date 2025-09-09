#  Superstore Sales Dashboard

A **Power BI Dashboard** showcasing key retail metrics—sales, profit, shipping performance, and regional insights—powered by the Superstore dataset. This repository is part of the **FUTURE_DS_01** learning series.

---

##  Project Overview

Designed to deliver quick, actionable insights into retail operations:
- **Sales & Profit Trends** over time  
- **Top Customers & Products**  
- **Sales Distribution by Region**  
- **Shipping Efficiency** via delivery times  

This dashboard enables business users to identify growth drivers, benchmark customer value, and reduce shipping delays.

---

##  Dataset

- **Source:** Superstore Sales Dataset (Excel)  
- **Key columns:**  
  `Order Date`, `Ship Date`, `Region`, `State`, `Category`, `Sub-Category`, `Sales`, `Profit`, `Quantity`, `Discount`, etc.

---

##  Data Cleaning & Transformation

Executed in **Power BI** using **Power Query & DAX**:

- Dates (`Order Date`, `Ship Date`) standardized to proper Date format  
- Created a **Date Table** for time-based analysis  
- Defined essential measures:

```DAX
Total_Sales = SUM(Superstore[Sales])

Total_Profit = SUM(Superstore[Profit])

Profit_Margin = DIVIDE([Total_Profit], [Total_Sales], 0)

Days_to_Ship = DATEDIFF(
  Superstore[Order Date],
  Superstore[Ship Date],
  DAY
)
```

---

##  Dashboard Features

### 1. Sales & Profit Trend (Line Chart)
- Tracks **Total Sales** and **Total Profit** by month  
- Includes **Profit Margin** as a secondary axis

### 2. Top 10 Customers / Products (Bar Chart)
- Shows highest contributing customers or products by **Total Sales**  
- Sorted descending to highlight the best performers

### 3. Sales by Region (Filled Map)
- Visualizes sales volume geographically  
- Darker coloring indicates higher sales  
- Modeled after the screenshot below

### 4. Shipping Performance
- **Days to Ship** highlights logistics efficiency and delays

---

##  Dashboard Preview

![Superstore Sales Dashboard Screenshot](https://github.com/abdulmossawer/FUTURE_DS_01/raw/main/dashboard/screenshots/Superstore%20Sales%20Dashboard.png)

---

##  How to Use

1. Clone this repository:
    ```bash
    git clone https://github.com/abdulmossawer/FUTURE_DS_01.git
    ```

2. Open the `.pbix` file using **Power BI Desktop**

3. Explore the visuals, interact with slicers, and filter insights

---

##  Business Value

- **Trend Insights:** Identify seasonal performance spikes  
- **Top Performers:** Prioritize high-value customers/products for growth  
- **Regional Strategy:** Optimize sales by geography  
- **Logistics Optimization:** Address shipping delays for better customer satisfaction

---

##  Tools Used

- **Power BI Desktop** for data modeling and reports  
- **DAX** for calculations and KPIs  
- **Excel** as the primary data source

---

##  Contribution

Contributions are welcome! Feel free to fork the repo, make enhancements, and submit a pull request.

---

Created with passion by **[Abdul Mossawer](https://github.com/abdulmossawer)**  
