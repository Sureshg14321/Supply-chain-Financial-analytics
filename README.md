# 📊 Supply-Chain & Financial Analytics Dashboard

---

## 📌 Project Overview
This project presents a **Power BI dashboard** designed to provide a unified view of business performance across financial and operational areas.  
It enables quick monitoring of key metrics and supports data-driven decision-making.

---

## 🎯 Business Objective
- Track revenue and profitability  
- Monitor supply chain performance  
- Identify inventory risks  
- Evaluate shipment efficiency  
- Analyze customer behavior  

---

## 📂 Data Source
The dashboard is built using multiple CSV datasets:
- Sales  
- Customer  
- Product  
- Supplier  
- Inventory  
- Procurement  
- Production  
- Shipment  
- Facility  
- Date Table  

---

## 🧹 Data Preparation
- Cleaned and transformed data using Power Query  
- Created relationships using a **star schema model**  
- Built a centralized **Date Table**  
- Removed inconsistencies and handled null values  

---

## 📊 Key KPIs
- Total Revenue  
- Profit  
- Profit Margin %  
- Total Orders  
- Inventory Quantity  
- Shipment Quantity  
- On-Time Delivery %  
- Customer Count  

---

## 📄 Dashboard Pages

### 1️⃣ Index Page
- Navigation hub for all dashboard pages  

### 2️⃣ Executive Overview
- High-level KPIs and revenue trends  
- Business performance summary  

### 3️⃣ Supply Analysis
- Supplier performance  
- Procurement cost insights  

### 4️⃣ Inventory Analysis
- Stock levels by product and facility  
- Low inventory identification  

### 5️⃣ Shipment Analysis
- Shipment trends  
- Delivery performance and delays  

### 6️⃣ Customer Analysis
- Customer segmentation  
- Top customers and purchase behavior  

---

## 🎛 Filters & Interactivity
- Date filter  
- Product category filter  
- Customer and supplier filters  
- Interactive visuals across all pages  

---

## 🧮 DAX Measures
```DAX
Total Revenue = SUM(Sales[net_revenue])

Gross Revenue = SUM(Sales[gross_revenue])

Avg Order Value = DIVIDE([Total Revenue],[Total oders],0)

Profit = SUM(Sales[profit])

Profit Margin % = DIVIDE([Profit], [Total Revenue], 0)

Total Orders = DISTINCTCOUNT(Sales[order_number])

Total Shipments = COUNT(Shipment[shipment_id])

Total Shipment Quantity = SUM(Shipment[quantity])

Total Purchase Orders = DISTINCTCOUNT(Procurement[po_number])

Total Procurement Quantity = SUM(Procurement[order_quantity])

Total Inventory = SUM(Inventory[stock_level])

Total Customers = DISTINCTCOUNT(Customer[customer_id])

Supplier Contribution % = DIVIDE([Total procurement Cost],CALCULATE([Total procurement Cost],all(Supplier)),0)

Perfect Orders = CALCULATE(COUNT(Shipment[shipment_id]),Shipment[status]="Delivered")

Order Quantity = SUM(Sales[quantity_sold])

Inventory Quantity = SUM(Inventory[stock_level])

Avg Cost Per Unit = AVERAGE(Procurement[unit_cost])

```

---

## 📈 Key Insights
- Revenue trends highlight business growth patterns
- Supplier analysis identifies cost-heavy vendors
- Inventory page detects low stock risks
- Shipment analysis reveals delivery performance gaps
- Customer page highlights top revenue contributors

---

## 🧾 Conclusion

This dashboard provides a comprehensive view of business operations, helping stakeholders make informed decisions across finance, supply chain, and customer domains.

## 📷 Screenshots

<img width="1366" height="768" alt="index" src="https://github.com/user-attachments/assets/04e77312-6e6c-4b4f-9e4f-645a3536e05f" />


<img width="1366" height="768" alt="overview" src="https://github.com/user-attachments/assets/783b036f-5350-4a97-85f8-63fb3d0eb28d" />




 



