# PROCUREMENT PERFORMANCE & SUPLLIER ANALYTICS DASHBOARD

This project aims to analyze procurement operations and supplier performance to support procurement monitoring and decision making. The analysis focuses on procurement cost, supplier delivery performance, lead time efficiency, product quality, and cost savings.

In addition, an interactive Tableau dashboard was developed to monitor procurement KPIs and identify opportunities for operational improvement.

## Key Business Question
- Has the procurement process been operating efficiently in terms of cost, product, quality, and delivery performance?
- Which product categories contribute the most to procurement spending and product defects?
- Which suppliers demonstrate the best performance and which require improvement based on operational KPIs such as On-Time Rate, Lead Time, and Defect Rate?

## Objectives
- To evaluate procurement efficiency by analyzing procurement cost, saving rate, lead time, and on-time delivery performance
- To identify product categories that have significant impacts on procurement spending and quality performance
- To asses supplier performance using operational KPIs, including On-Time Rate, Average Lead Time, and Defect Rate, in order to identify areas for improvement
- To develop an interactive dashboard for monitoring procurement activities, evaluating supplier performance, and supporting data driven decision making

## Dataset
Source: Kaggle [Procurement Dataset](https://www.kaggle.com/datasets/shahriarkabir/procurement-kpi-analysis-dataset)

Features:
- PO_ID: Purchase Order ID
- Supplier: Supplier name
- Order_Date: Order creation date
- Delivery_Date: Delivery completion date
- Item_Category: Purchased item category
- Quantity: Ordered quantity
- Unit_Price: Original item price
- Negotiated_Price: Negotiated item price
- Order_Status: Delivery status
- Defective_Units: Number of defective items
- Compliance: Supplier compliance status

## Tools
- Excel for data cleaning & validation
- Tableau for dashboard development

## Project Workflow
### 1. Data Cleaning
- Missing Value Check
  Missing values were identified in:
  | Column          | Missing Values |
  | --------------- | -------------- |
  | Delivery_Date   | 87             |
  | Defective_Units | 136            |
- Handling Missing Value
  - Delivery Date
    - Calculate lead time:

      Lead_day = Delivery_Date - Order_Date
    - Calculate median lead time for each supplier
    - Missing delivery dates were imputed with:

      Order_Date + Median Lead_day by Supplier
      
      This approach preserved supplier specific delivery behavior
  - Defective Units
    Missing values were replaced with "0", assuming no defective items were reported
- Duplicate Check
  Duplicate records were checked and no duplicate transaction were found
- Data Validation
  Validation rules applied:

  Delivery_Date > Order_Date

  All records passed validation

### 2. Feature Engineering
- Lead Day: Measures delivery efficiency
- Total Amount: Represent procurement cost before negotiation
- Total Negotiated Cost
- Saving
- On-Time Status

### 3. Dashboard Development
An interactive Tableau dashboard was developed with three analytical sections.
- Overview Dashboard
  Metrics included:
  - Total Orders
  - Total Cost
  - Saving Rate
  - On-Time Rate
  - Average Lead Day
  - Defect Rate
  Visualizations:
  - Procurement Cost Trend
  - On-Time Rate Trend
  - Total Cost by Category
  - Defect Rate by Category
    
  <img width="1649" height="894" alt="{B92D822A-2C9B-4A80-A0A5-879D3626759B}" src="https://github.com/user-attachments/assets/e55320e9-7b87-452a-a7fc-81b6ef586e6a" />

- Supplier Performance Dashboard
  Visualizations:
  - On-Time Rate by Supplier
  - Average Lead Day by Supplier
  - Defect Rate by Supplier
    
  <img width="1643" height="887" alt="{C2D1EB66-2BB8-4845-8F4C-B437AD5D2E8B}" src="https://github.com/user-attachments/assets/04b2a03d-04b7-4e13-979b-7dc0486d31f9" />

- Order Insight Dashboard
  Visualizations:
  - Monthly Order Trend
  - Order Status Distribution
  - Total Orders by Category
  - Top Procurement Transaction by Cost
    
  <img width="1651" height="889" alt="{32AD186F-EAE0-4386-B1C9-8C1221A1F546}" src="https://github.com/user-attachments/assets/b02ca2d4-5b40-430e-ad0b-9461fce68c47" />

## Insights
- Procurement operations recorded a total spending of $45.4M across 777 purchase orders, while procurement negotiations generated a 7.97% saving rate, indicating effective cost control and supplier negotiation practices.
- The overall On-Time Rate reached 75.2%, which remains below the operational target of 80%, suggesting opportunities to improve delivery performance and procurement planning.
- Supplier performance varied across key operational metrics:
  - Beta Supplies achieved the highest On-Time Rate (81.4%), demonstrating strong delivery reliability.
  - Gamma Co recorded the shortest average lead time (10.2 days), indicating efficient delivery performance.
  - Delta Logistics showed the highest defect rate (10.8%), highlighting potential quality concerns that require further evaluation.
- Procurement spending was concentrated in a few product categories:
  - MRO and Office Supplies contributed the highest procurement costs.
  - These categories represent the largest opportunities for future cost optimization and supplier negotiation.
- Product quality performance differed across categories:
  - Raw Materials recorded the highest defect rate among all categories.
  - This may indicate quality control issues that could impact operational efficiency and procurement effectiveness.
- Monthly procurement spending and On-Time Rate fluctuated throughout the observed period, indicating that supplier performance and procurement efficiency were not consistently maintained over time.

## Business Recommendations
- Improve supplier performance management by establishing regular reviews for suppliers with low On-Time Rates and high defect rates.
- Prioritize corrective actions for suppliers with quality issues, particularly those contributing to higher defect rates, to reduce operational risks and improve product quality.
- Strengthen procurement planning and order scheduling to improve delivery performance and achieve the target On-Time Rate.
- Focus negotiation efforts on high-spending categories such as MRO and Office Supplies, where even small cost reductions can generate significant savings.
- Implement supplier scorecards that track On-Time Rate, Lead Time, Defect Rate, and Procurement Cost to support continuous performance monitoring.
- Conduct root-cause analysis on categories with high defect rates, especially Raw Materials, to identify quality improvement opportunities.
- Establish procurement performance targets and regularly monitor KPI trends through the dashboard to support data-driven operational decision-making.
