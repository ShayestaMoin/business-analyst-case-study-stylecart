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
