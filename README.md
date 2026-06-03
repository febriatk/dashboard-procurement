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
###1. Data Cleaning
- Missing Value Check
  Missing values were identified in:
  | Column          | Missing Values |
  | --------------- | -------------- |
  | Delivery_Date   | 87             |
  | Defective_Units | 136            |
- Handling Missing Value
  - Delivery Date
    - Calculate lead time:
      | Lead_day = Delivery_Date - Order_Date |
    - Calculate median lead time for each supplier
    - Missing delivery dates were imputed with:
      | Order_Date + Median Lead_day by Supplier |
      This approach preserved supplier specific delivery behavior
  - Defective Units
    Missing values were replaced with "0", assuming no defective items were reported
- Duplicate Check
  Duplicate records were checked and no duplicate transaction were found
- Data Validation
  Validation rules applied:
  | Delivery_Date > Order_Date |
  All records passed validation

###2. Feature Engineering
- Lead Day: Measures delivery efficiency
  | Lead_Day = Deliver_Date - Order_Date |
- 
