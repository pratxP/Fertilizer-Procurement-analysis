# Fertilizer Procurement Data Analysis

## Overview
This repository contains a detailed analysis of fertilizer procurement data visualized using Power BI. The project aims to uncover procurement trends, supplier performance metrics, cost breakdowns, and demand patterns. Several custom measures and calculated fields were created to derive actionable insights and improve decision-making processes.

---

## Key Features

### Metrics and Calculations
1. **On-Time Delivery Rate**:  
   Percentage of deliveries meeting lead time and order status criteria.

2. **Average Lead Time by Supplier**:  
   Average delivery time per supplier.

3. **Average Supplier Rating**:  
   Mean supplier rating for each supplier.

4. **Total Procurement Cost**:  
   Aggregate procurement expenditure over a selected period.

5. **Cost per Product Category**:  
   Summed total cost grouped by product category.

6. **Average Unit Price by Product Category**:  
   Mean price per unit for each product category.

7. **Total Cost by Region**:  
   Procurement expenditure grouped by region.

8. **Quantity Ordered by Region**:  
   Total quantity of products ordered for each region.

9. **Supplier Cost Contribution**:  
   Total procurement cost attributed to each supplier.

10. **Procurement Cycle Time**:  
    Average lead time across all suppliers.

---

### Insights Derived
1. **Regional Cost Insights**:
   - Organic materials in North America constituted **5.46%** of the total cost.
   - North America accounted for **21.38%** of total procurement cost.

2. **Supplier Performance**:
   - **Supplier B** had the highest procurement cost of **$918,189.8**, **21.32%** higher than Supplier A's cost of **$756,863.4**.
   - Procurement costs across five suppliers ranged from **$756,863.4** to **$918,189.8**.

3. **Demand Trends**:
   - Monthly demand increased by **1.77%** between January and December 2024.
   - The steepest demand increase occurred between **August and December 2024**, with a rise of **4.39% (56.11)**.

4. **Order Status Analysis**:
   - Delivered orders had the highest count (**240**), followed by In Transit (**231**) and Ordered (**229**).

5. **Product Category Breakdown**:
   - Detailed cost allocation by product category.

6. **Monthly Demand**:
   - October recorded the highest demand (**88,825**), **52.82%** higher than September's **58,123**.
   - October accounted for **10.15%** of total monthly demand.

7. **Lead Time Insights**:
   - Solvent in North America had the highest average lead time at **20.74 days**.

---

### Power BI Measures
- **CostMTD**: Total procurement cost for the current month.  
  ```DAX
  CostMTD = TOTALMTD([Total procurement cost], 'fertilizer_procurement_data (1)'[Date].[Date])
- **LM_Cost**: Procurement cost for the previous month.  
  ```DAX
  LM_Cost = CALCULATE([Total procurement cost], PREVIOUSMONTH('fertilizer_procurement_data (1)'[Date].[Date]))
- **MoMChange**: Month-over-month percentage change in procurement cost.  
  ```DAX
  LM_Cost = CALCULATE([Total procurement cost], PREVIOUSMONTH('fertilizer_procurement_data (1)'[Date].[Date]))
- **Total Procurement Cost**: Sum of total costs across the dataset.  
  ```DAX
  Total procurement cost = SUM('fertilizer_procurement_data (1)'[Total Cost])

---

### Visualizations
**The analysis includes interactive Power BI dashboards featuring:**

- Bar Charts: Breakdown of costs by region and product category.
- Line Charts: Monthly demand trends and procurement cost variations.
- Pie Charts: Supplier contribution to total costs and product category distribution.
- Tables: Supplier performance and procurement cycle times.
  

![Screenshot 2025-01-11 142955](https://github.com/user-attachments/assets/da19acac-bf22-4e30-9c15-5abc91cd0767)
![Screenshot 2025-01-11 143004](https://github.com/user-attachments/assets/6ec17ca3-8d3a-4487-af39-916b02b56cc6)
![Screenshot 2025-01-11 143007](https://github.com/user-attachments/assets/ef3614e2-8399-42c0-9754-9701a3231661)
![Screenshot 2025-01-11 143022](https://github.com/user-attachments/assets/0d6ed7c9-362f-4467-810b-4c1322d80f3c)
![Screenshot 2025-01-11 143034](https://github.com/user-attachments/assets/352aedf3-7b1c-4f4d-8a09-7afc5cd3b1a5)

---

### Future Enhancements
-**Incorporate predictive models for demand forecasting.**
-**Integrate external datasets for market trend analysis.**
-**Automate data updates for real-time insights.**

---

### Contributing
**Contributions are welcome! Feel free to open issues or submit pull requests for enhancements or bug fixes.**

---

### License
**This project is licensed under the MIT License.**

---

## Contact

For questions or support, please contact [pratyaksh@gmail.com].

