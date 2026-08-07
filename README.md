# Analysis Artifacts Summary
# 1. Root Cause Analysis (RCA)
Core Issue Identified: 78% of cancellations resulted from items being sold online after physical inventory had run out.
Root Cause: Storefront relied on a single daily midnight CSV file batch upload rather than dynamic API synchronization with the Warehouse Management System (WMS).

# 1: Root Cause Analysis (RCA)
# Root Cause Analysis: StyleCart Order Fulfillment Bottlenecks

## Problem Statement
During Q1/Q2, StyleCart experienced a **15% order cancellation rate**, an average **dispatch delay of 96 hours (4 days)**, and a **25% drop in CSAT**. Analysis reveals that **78% of order cancellations** occurred because items purchased online were discovered to be out of stock *after* payment processing.

---

## 5 Whys Analysis

1. **Why are order dispatches delayed by 4 days?**
   * *Because warehouse staff delay packing orders while manually verifying physical stock availability.*
2. **Why do staff manually verify stock availability?**
   * *Because stock counts in the online storefront regularly mismatch physical inventory on warehouse shelves.*
3. **Why is storefront inventory inaccurate?**
   * *Because stock levels update via a legacy batch CSV file export once daily at midnight.*
4. **Why are stock levels updated only once daily?**
   * *Because the current setup relies on a manual file upload script rather than automated data synchronization.*
5. **Why is a manual file upload script being used?**
   * *Because the storefront lacks a real-time API integration with the warehouse inventory management system (WMS).*

---

## Root Cause Statement
The core driver of fulfillment delays and out-of-stock cancellations is the **lack of real-time API integration** between the storefront e-commerce platform and the Warehouse Management System (WMS).

# Fishbone Diagram for Analysis:
<img width="1746" height="661" alt="image" src="https://github.com/user-attachments/assets/7a3d764c-0534-4c0d-aa77-f9d1a5fe9a13" />

# 2. Process Re-engineering (BPMN 2.0)
As-Is Process: Highlighted a 48-hour manual communication gap between sales confirmation and warehouse fulfillment.

To-Be Process: Implemented real-time CheckInventoryAPI calls prior to checkout completion and enabled parallel processing (AND Gateway) for picking alerts and customer tracking.

<img width="4412" height="3320" alt="image" src="https://github.com/user-attachments/assets/749d82a8-086e-4eda-a685-7659ecf70a01" />


# 3. Agile Requirements (Jira)
Built Epic SC-EPIC-01 and structured user stories (SC-101, SC-102) complete with story points and Gherkin Acceptance Criteria.

<img width="1920" height="860" alt="image" src="https://github.com/user-attachments/assets/c1f40c59-d874-417b-b917-23a604de66fb" />
<img width="1920" height="871" alt="image" src="https://github.com/user-attachments/assets/23dda46e-4d9a-4ba9-8e57-78e67551e4a3" />

# 4. Governance & Documentation (Confluence)
Published formal Product Requirements Document (PRD) and Standard Operating Procedure (SOP) for exception handling.

<img width="2000" height="2588" alt="image" src="https://github.com/user-attachments/assets/2c6d79a9-299f-4be6-a56b-ae226481c466" />
<img width="2000" height="2588" alt="image" src="https://github.com/user-attachments/assets/4932c389-babf-4d19-98c6-8367c8f9f72d" />


# Business Analyst Case Study: StyleCart Fulfillment Optimization

![Project Status](https://img.shields.io/badge/Status-Approved-brightgreen)
![Domain](https://img.shields.io/badge/Domain-E--Commerce%20%26%20Logistics-blue)
![Tools](https://img.shields.io/badge/Tools-Jira%20%7C%20Confluence%20%7C%20BPMN--2.0%20%7C%20Lucidchart-orange)

## Project Overview
During Q1/Q2, StyleCart faced severe fulfillment bottlenecks that drove a **15% order cancellation rate**, an average **dispatch delay of 4 days (96 hours)**, and a **25% drop in CSAT**. This case study covers the end-to-end Business Analysis lifecycle executed to resolve these issues.

---

## Target Project Outcomes & Key Results

| Metric | Baseline (Q1/Q2) | Target (Q3/Q4) | Impact |
| :--- | :--- | :--- | :--- |
| **Order Cancellation Rate** | 15% | **<2%** | Elimination of post-payment stockouts |
| **Dispatch Cycle Time** | 96 Hours (4 Days) | **<12 Hours** | 87.5% reduction in cycle time |
| **Customer Satisfaction (CSAT)** | 3.2 / 5.0 | **4.5 / 5.0** | Restored customer retention |
