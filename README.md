# 🚀 Mastering Data Analysis in Excel: Power Pivot & DAX Functions Project

---

📘Power Pivot Interface

<img src="https://github.com/amolhatwar/Power-Pivot-DAX-Functions-Project/blob/28585d4a1923c48d00ec3e604ef1989cd43a2332/Dax_power_Pivot_Project.png" width="600">

---

📘Complete Project & Reports!

<img src="https://github.com/amolhatwar/Power-Pivot-DAX-Functions-Project/blob/28585d4a1923c48d00ec3e604ef1989cd43a2332/Dax_power_Pivot_Project_Reports.png" width="600">

---

I'm excited to share a project where I delved into **Microsoft Excel's Power Pivot** and built essential **DAX (Data Analysis Expressions) functions** for deeper data analysis. This project demonstrates how to transform raw sales data into actionable business intelligence, showing the power of these tools far beyond standard Excel functions.

---

## 🔽 Download the Project Files:= https://github.com/amolhatwar/Power-Pivot-DAX-Functions-Project/blob/main/Dax_power_Pivot_Project.xlsx

---

🎥 **Video Tutorial:** https://youtu.be/oe1Kyklvq0Q

---

## 🎯 What’s Covered in This

* **Importing Data:** Pulling raw data from an external CSV-like format into the Power Pivot Data Model.
* **Creating Calculated Columns:** Using DAX to derive new data points, like `Amount` (Total Sales for a transaction).
* **Defining Measures:** Writing core DAX functions to calculate key business metrics, such as `Total Sales`, and product-specific totals.
* **Advanced Aggregations:** Demonstrating $\text{MAX}$ and $\text{MIN}$ aggregations on quantities.
* **Time Intelligence & Context:** Calculating percentages of total sales using context modification (`ALL`).
* **Visualization:** Connecting the Power Pivot Data Model to a PivotTable for insightful reporting.

---

## ❓ Problem Explained

The raw sales data contains information on the **Date**, **Product**, **Quantity**, and **Unit Price**. A traditional PivotTable setup would require helper columns in the original worksheet or limited calculated fields. The goal was to perform complex, dynamic calculations (like per-product totals and contribution to total sales) directly within the **Data Model** using DAX, which handles large datasets and complex relationships more efficiently and scalably.

---

## ✅ Solution (What We Built)

We built a robust Data Model using Power Pivot and defined several key DAX calculations:

### 1. Calculated Column: Total Transaction Amount
This calculates the total monetary value for each individual transaction row.
$$\text{Amount} = [\text{Quantity}] * [\text{Unit Price}]$$

### 2. Measures for Key Metrics (DAX Functions)
These measures perform aggregations over the entire or filtered dataset:

| Measure Name | DAX Function | Purpose |
| :--- | :--- | :--- |
| $\text{[Total Sales]}$ | $\text{SUM}(\text{SalesData}[\text{Amount}])$ | Sums the total revenue across all transactions. |
| $\text{[Pen sales]}$ | $\text{CALCULATE}([\text{Total Sales}], \text{SalesData}[\text{Product}] = "\text{Pen}")$ | Sum of sales specifically for the "Pen" product. |
| $\text{[Max quantity]}$ | $\text{MAX}(\text{SalesData}[\text{Quantity}])$ | Finds the largest single quantity sold in any transaction. |
| $\text{[Min quantity]}$ | $\text{MIN}(\text{SalesData}[\text{Quantity}])$ | Finds the smallest single quantity sold in any transaction. |
| $\text{[% of Total Sales]}$ | $\text{DIVIDE}([\text{Total Sales}], \text{CALCULATE}([\text{Total Sales}], \text{ALL}(\text{SalesData})))$ | Calculates the revenue for the current row's context (e.g., a specific product) as a percentage of the grand total, ignoring all current filters applied to the 'SalesData' table. |

---

## 🧠 Insights Shown in the Video

The final PivotTable, powered by these DAX measures, immediately delivered several valuable insights:

| Product | Total Sales | % of Total Sales |
| :--- | :--- | :--- |
| **Pen** | 440 | 40.55% |
| **Notebook** | 450 | 41.47% |
| **Pencil** | 120 | 11.06% |
| **Marker** | 75 | 6.91% |
| **Grand Total** | **1085** | **100.00%** |

* **Dominant Products:** **Notebook** and **Pen** are the top-selling products by revenue, accounting for over **82%** of total sales combined.
* **Sales Floor & Ceiling:** The maximum single quantity sold was **10**, while the minimum was **2**, offering a quick view into transaction size.
* **Direct Metric Calculation:** By creating measures like `[Pen sales]`, we can perform specific, hardcoded filtering which is a key strength of the `CALCULATE` function.

---

## 🧩 Use Cases for This

This approach is invaluable for:

* **Financial Reporting:** Creating complex P&L statements, Gross Margin analysis, and cost-of-goods-sold calculations.
* **Sales Analysis:** Calculating year-over-year growth, moving averages, or market basket analysis.
* **Time Intelligence:** Using DAX's powerful time functions to compare sales month-over-month (MoM) or year-to-date (YTD).
* **Building KPI Dashboards:** Creating dynamic metrics that respond to slicers and filters in real-time.

---

## 📘 Key Learnings from This

* **Data Model over Spreadsheet:** Power Pivot stores data in a columnar, compressed database, offering superior performance for large datasets compared to standard Excel sheets.
* **DAX is Context-Sensitive:** Functions like `CALCULATE` and `ALL` are crucial for manipulating the filter context, allowing you to compare a specific data point (like a product's sales) against a broader scope (like total company sales).
* **Measures vs. Calculated Columns:** **Calculated Columns** are computed row-by-row during data refresh (like the `Amount`), while **Measures** are aggregated on the fly based on the PivotTable's context (like `Total Sales`), making them essential for numerical aggregation.

---

## 🧪 Practical Applications

Imagine extending this project to a retail environment:

1.  **Inventory Health:** Use DAX to calculate the "Days of Supply" for each product based on current stock and average daily sales.
2.  **Customer Value:** Calculate the Average Transaction Value ($\text{ATV}$) and Lifetime Value ($\text{LTV}$) for different customer segments.

---

## 🧰 Tools Used

* Microsoft Excel (with Power Pivot Add-in)
* DAX (Data Analysis Expressions)

---
## 📬 Feedback & Contributions

Open to:
- Feature suggestions for new automation and smart dashboard tricks
- Sample dataset contributions
- Enhancements for Power Query/Power BI integration

Open an Issue or submit a Pull Request with improvements!

## ⭐ License

This project is MIT-licensed for both education and business use.

## 📬 Contact Me
If you’d like to collaborate, discuss a project, or simply connect — I’m always open.

📧 🔗 [Email](amolhatwar.analytics@gmail.com)  
🌍 🔗 [Portfolio Website](https://amolhatwar.github.io)
🐙🔗 [GitHub](https://github.com/amolhatwar)
💼 🔗 [LinkedIn](https://www.linkedin.com/in/amolhatwar)

---
