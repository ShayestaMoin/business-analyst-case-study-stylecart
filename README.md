# Analysis Artifacts Summary
# 1. Root Cause Analysis (RCA)
Core Issue Identified: 78% of cancellations resulted from items being sold online after physical inventory had run out.
Root Cause: Storefront relied on a single daily midnight CSV file batch upload rather than dynamic API synchronization with the Warehouse Management System (WMS).

📁 View full analysis: Five Whys Analysis

2. Process Re-engineering (BPMN 2.0)
As-Is Process: Highlighted a 48-hour manual communication gap between sales confirmation and warehouse fulfillment.

To-Be Process: Implemented real-time CheckInventoryAPI calls prior to checkout completion and enabled parallel processing (AND Gateway) for picking alerts and customer tracking.

📁 View diagrams: As-Is Diagram | To-Be Diagram

3. Agile Requirements (Jira)
Built Epic SC-EPIC-01 and structured user stories (SC-101, SC-102) complete with story points and Gherkin Acceptance Criteria.

📁 View backlog requirements: User Stories & Acceptance Criteria

4. Governance & Documentation (Confluence)
Published formal Product Requirements Document (PRD) and Standard Operating Procedure (SOP) for exception handling.

📁 View documents: PRD Document | SOP Document


# Business Analyst Case Study: StyleCart Fulfillment Optimization

![Project Status](https://img.shields.io/badge/Status-Approved-brightgreen)
![Domain](https://img.shields.io/badge/Domain-E--Commerce%20%26%20Logistics-blue)
![Tools](https://img.shields.io/badge/Tools-Jira%20%7C%20Confluence%20%7C%20BPMN--2.0%20%7C%20Draw.io-orange)

## Project Overview
During Q1/Q2, StyleCart faced severe fulfillment bottlenecks that drove a **15% order cancellation rate**, an average **dispatch delay of 4 days (96 hours)**, and a **25% drop in CSAT**. This case study covers the end-to-end Business Analysis lifecycle executed to resolve these issues.

---

## Target Project Outcomes & Key Results

| Metric | Baseline (Q1/Q2) | Target (Q3/Q4) | Impact |
| :--- | :--- | :--- | :--- |
| **Order Cancellation Rate** | 15% | **<2%** | Elimination of post-payment stockouts |
| **Dispatch Cycle Time** | 96 Hours (4 Days) | **<12 Hours** | 87.5% reduction in cycle time |
| **Customer Satisfaction (CSAT)** | 3.2 / 5.0 | **4.5 / 5.0** | Restored customer retention |
