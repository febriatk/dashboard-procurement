# PROCUREMENT DASHBOARD

This project visualizes procurement performance using transaction data from 2022 - 2023. The goal is to provide insights into supplier performance, order insight, and cost distribution using an interactive Tableau dashboard to support better procurement decision-making.

## Dashboard Preview

This dashboard containing 3 section such as :
- Overview : Summary KPIs. cost trends, top categories and suppliers
![{56BE7C95-D67C-4F61-A889-0F0487095D84}](https://github.com/user-attachments/assets/6c4827cb-e45a-4c64-b379-8ff0b0561aa5)

- Supplier Performances : On-time delivery rate, lead time, and detailed supplier data table
![{85AB0634-86B2-47FA-9C1D-FA6BF091BC55}](https://github.com/user-attachments/assets/b9819220-0694-4b64-8455-f4913b7b0c17)

- Order Insight : Distribution of orders by status and category, and detailed PO data table
![{0A9571AC-73E8-4EAB-925A-7998B01AF952}](https://github.com/user-attachments/assets/327b1494-7d78-45b0-af65-a0214df4a45d)

[View on Tableau Public](https://public.tableau.com/views/Procurement_17510369898440/Dashboard2?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Objective

- Monitor total procurement activity including quantity, cost, and savings
- Evaluate supplier performance based on on-time delivery (<= 15 days from order data) and average lead time
- Analyze total order by order status and item category
- Support data-driven decision making in supply chain and procurment operations

## Tools & Dataset
- Excel – Used for cleaning and preparing the dataset
- Tableau – For building the interactive dashboard
- Dataset – Procurement data collected from Kaggle

## Data Cleaning: Handling Missing Value in Delivery Dates

Problem: Some rows had missing values in the Delivery_Date column, which are critical for calculating lead time and determining on-time delivery.

Solution using Excel :
- Calculated the average lead time (in days) using rows where both Order_Date and Delivery_Date were available
- For row with missing Delivery_Date, filled in the value by adding the average lead time to the corresponding Order_Date
- Excel Formula : (Order_Date) + (Average_Lead_Time)

## Key Insights
- Negotiation efforts have resulted in 3.9M in total savings
- MRO and Office Supplies categories have the highest procurement cost
- On-time delivery rate is 77%, suggesting room for supplier performance improvement
- Some supplier have longer average lead times (>10 days)
