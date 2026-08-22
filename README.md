<h1 align="center">
  <b>Analytics Dashboard for Accounts Payable </b>
</h1>

<div align="center">
  <a href="#"><img src="https://custom-icon-badges.demolab.com/badge/Power%20BI-F2C811?logo=power-bi&logoColor=fff" alt="Power BI"></a>
  <a href="#"><img src="https://custom-icon-badges.demolab.com/badge/DAX-0078D4?logo=microsoft&logoColor=fff" alt="DAX"></a>
  <a href="#"><img src="https://img.shields.io/badge/Power%20Query-5E9624?logo=microsoftexcel&logoColor=fff" alt="Power Query"></a>
  <a href="#"><img src="https://img.shields.io/badge/Data%20Modelling-00599C?logo=microsoftsqlserver&logoColor=fff" alt="Data Modelling"></a>
</div>

## 📌 Executive Summary
Finance and external audit procedures are traditionally manual and spreadsheet-heavy workflows. I developed this Power BI project to bridge **Accounts Payable Analysis** with **Finance Transformation**. 

This interactive analytics solution transforms static Accounts Payable (AP) procedures into a dynamic, parameter-driven automating cut-off testing, anomaly detection, and aging analysis. It demonstrates how scalable data modelling can reduce manual hours, improve transparency, and be tailored to different materiality thresholds.

> *![Dashboard Demo](https://github.com/JackWhooo/Audit-Analytics-PowerBI/blob/main/Demonstration/GIF/Cut-off%20Dashboard.gif)*

---

## 📌 Solutions & Features

### 1. Dynamic Cut-Off & Anomaly Detection Engine
* **The Problem:** Auditors pull transaction logs and manually filter dates around year-end to test for cut-off inaccuracies.
* **The Automated Solution:** A parameter-driven cut-off dashboard. Users adjust a visual slider (e.g., +/- 15 days from Year-End) and input a custom materiality limit. The system instantly isolates and highlights high-value, high-risk transactions near the financial boundary.
> *![Cut-off Report](https://github.com/JackWhooo/Audit-Analytics-PowerBI/blob/main/Demonstration/Screenshots/Cut-off%20Report.png)*

Interactive Features:
- Cut-off days selector
- Threshold slicer

Users can:
- Adjust cut-off window (X days before/after year-end) and select the desired threshold,
- Analyse transaction volumes around YE,
- Identify high-value transactions above threshold (highlighted automatically) near YE.
- Analyse transaction trend
- Analyse transaction amounts by vendor via the scatter chart
- Drill-through to Transaction Details directly

> *![Cut-off Drill Through](https://github.com/JackWhooo/Audit-Analytics-PowerBI/blob/main/Demonstration/GIF/Cut-off%20Drill%20Through.gif)*

### 2. Interactive Aging & Working Capital Analysis
* **The Problem:** Static AP aging reports offer no ability to investigate underlying invoices without pulling secondary reports. AP aging is not visualised.
* **The Automated Solution:** A continuous-monitoring aging matrix with drill-through capabilities. Users can identify an overdue liability bucket at the macro level, and click through to investigate the exact supplier details and individual invoice histories.
> *![Ageing Dashboard](https://github.com/JackWhooo/Audit-Analytics-PowerBI/blob/main/Demonstration/Screenshots/Ageing%20Dashboard.png)*

The dashboard includes:
- aging bucket analysis,
- vendor-level aging review,
- overdue invoice tracking.

Users are able to drill-through to all the accounts payable to any supplier and to the summary of all the invoices in a certain age bucket.
> *![Ageing Drill Through](https://github.com/JackWhooo/Audit-Analytics-PowerBI/blob/main/Demonstration/GIF/Ageing%20Analysis.gif)*

---
## 📌 Data Model

The solution uses a star-schema data model.

Fact Tables:
- Accounts Payable Listing
- Transaction Listing

Dimension Tables:
- Date
- Vendor

Benefits:
- Improved query performance
- Scalable reporting architecture
- Consistent filtering behaviour

![Data Model](https://github.com/Jack-HY-Hu/Audit-Analytics-PowerBI/blob/main/Demonstration/Screenshots/Data%20Model.png)

---

## 📌 Technical Architecture & Skills Demonstrated

* **Power BI & Data Storytelling:** Designed an intuitive UI with interactive drill-throughs, dynamic slicers, and conditional formatting to instantly surface high-risk transactions.
* **DAX (Data Analysis Expressions):** Built parameter-driven measures enabling users to adjust materiality thresholds, modify cut-off testing windows, and dynamically identify high-risk transactions
* **Data Modelling (Star Schema):** Built a relational model connecting Fact tables (Transactions, AP Listing) with Dimension tables (Vendors, Dates).
* **Finance Knowledge:** Cut-off, Aging analysis, AP review procedures

---

## 📌 Files Included
| File                                         | Description              |
| -------------------------------------------- | ------------------------ |
| `Analytics Dashboard for Accounts Payable.pbit`  | Power BI dashboard       |
| `Modified_ dummy_AP_Listing_v2.csv`            | Accounts Payable dataset |
| `Modified_ dummy_Transaction_Listing_v2.csv`   | Transaction dataset      |
| `README.md`                                  | Project documentation    |


P.S.
Example data presented in the project is fictional for illustration





