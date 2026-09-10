# OrderFlow Nexus | Order & Vendor Coordination System
**Agile Scrum Product Delivery & Supply Chain Optimization**

---

## 📌 Project Overview

**OrderFlow Nexus** is an intelligent, Agile-driven B2B order lifecycle management and vendor coordination platform engineered for **FreshPrints**, an enterprise operating in the custom apparel procurement and supply chain market. Developed at Manyata Tech Park (Bengaluru, India) under the executive sponsorship of **Vikram Malhotra** (Project Sponsor) and **Megha Kulkarni** (Business Sponsor), the system was designed and delivered within a disciplined **4-month Agile-Scrum roadmap (8 two-week sprints)** with a total budget limit of **₹5,00,000 INR**.

The platform transitions the organization from a disjointed, spreadsheet-reliant coordination model into a centralized digital coordination hub ("Nexus Hub"). Specifically architected to handle a high-volume concurrent workload of **2,321+ active apparel orders**, OrderFlow Nexus synchronizes cross-functional workflows across client operations, external printing partners, and management teams. Core capabilities include automated vendor capability matching based on print techniques, real-time logistics tracking via manufacturer APIs, systematic Root Cause Analysis (RCA) snag logging, and dynamic KRA/KPI performance analytics.

### Key Project Metadata
* **Project Name:** OrderFlow Nexus (Order & Vendor Coordination System)
* **Client / Domain:** FreshPrints | B2B Custom Apparel Supply Chain & Procurement Operations
* **Methodology:** Agile Scrum (4 Months / 8 Sprints / 2-Week Sprints)
* **Product Owner:** Sarah Jenkins (Principal Product Manager)
* **Lead Business Analyst / Contributor:** Debal Adhikari
* **Budget & Team:** ₹5.00 Lakhs INR | 7–8 Member Cross-Functional Scrum Team
* **Key Delivery Leads:** Rohan Murthy (Sr. Backend Dev), Priya Sharma (Full Stack Dev), Ananya Iyer (UI/UX Frontend Lead), Vikram Deshmukh (DB Architect), Karthik Nair (QA Automation)
* **Primary Infrastructure / Scale:** 2,321+ Concurrent Orders, Scalable up to 3,000 Order Metadata Records

---

## 🛑 Business Problem

Prior to OrderFlow Nexus, the procurement and order processing lifecycle at FreshPrints relied heavily on manual spreadsheet tracking, uncoordinated email chains, and tribal operational workarounds to juggle over 2,300 concurrent bulk custom apparel orders.

### 1. Primary Operational Challenges
* **Communication Silos & Timeline Conflicts:** Lack of a centralized synchronization module between internal operations, client deadlines, and external apparel decorators led to constant fulfillment delays and misaligned shipping schedules.
* **Inefficient & Sub-Optimal Vendor Assignment:** Support and procurement coordinators manually assigned print jobs without standardized visibility into vendor machinery, operational capacity, or technical specializations (e.g., Screen Printing vs. Direct-to-Garment [DTG]), resulting in high error rates, print defects, and vendor overloading.
* **Reactive Troubleshooting & Repeated Snags:** Order-related defects, fabric shortages, and print misprints were handled reactively without a structured Root Cause Analysis (RCA) classification, causing identical operational bottlenecks to recur repeatedly.
* **Operational Blindspots & Reporting Lag:** Management lacked real-time visibility into mission-critical operational metrics such as Mean Time to Resolve (MTTR), rolling Customer Satisfaction (CSAT), and On-Time Delivery accuracy.

### 2. Gap Analysis (AS-IS vs. TO-BE State)

| Business Dimension | AS-IS Legacy State (Manual & Disjointed) | TO-BE State (OrderFlow Nexus System) |
| :--- | :--- | :--- |
| **Order Tracking** | Manual spreadsheet entries and ad-hoc updates across 2,321 orders. | Centralized Nexus Hub with automated stage tracking from placement to delivery. |
| **Vendor Matching** | Manual assignment prone to capacity bottlenecks and machinery mismatch. | Automated Top-3 vendor recommendation engine filtering by print technique and error rate. |
| **Material Tracking** | Disconnected tracking of blank apparel shipments via individual carrier sites. | Automated manufacturer shipping API integrations with live "In-Transit" milestone bars. |
| **Issue Handling** | Unstructured escalation emails without documented reason codes. | Structured RCA snag logging with photo attachments and 12.5-hour delay triggers. |
| **Performance Visibility** | Subjective, retroactive monthly reporting with high manual overhead. | Real-time KRA/KPI Performance Dashboard tracking on-time delivery (99.5%) and CSAT. |

---

## 🎯 Project Objectives & Success Criteria

The development roadmap was tied to specific, quantifiable operational milestones:

* **Fulfillment Timeline Alignment:** Achieve **100% synchronization** between vendor production schedules and client deadlines, eliminating "timeline conflict" alerts.
* **Vendor Matching Accuracy:** Deliver a **20% increase** in orders assigned to "Best Fit" vendors through capability and capacity algorithms, reducing order defect rates by **15% by Q2 post-launch**.
* **Accelerated Issue Resolution:** Cut average issue resolution time by **25%** (reducing resolution turnaround from baseline delays to under **12.5 hours**) via standardized RCA reason codes.
* **High Customer Satisfaction:** Maintain a sustained Customer Satisfaction (CSAT) score of **>= 4.2 / 5.0**, measured continuously through the integrated customer feedback module.
* **Rapid Operational Transition:** Migrate **100% of the active 2,321 orders** to the OrderFlow Nexus platform within 30 days of the production Go-Live date.
* **Budget & Velocity Adherence:** Deliver 8 two-week iterations within the **₹5,00,000 INR** budget limit, achieving a predictable release cadence of **20–25 Story Points / Complexity Points (CP)** per sprint.

---

## 🔄 Approach & Methodology

The project executed an **Iterative Agile-Scrum Delivery Model** divided into 8 distinct two-week sprints:

```text
[Sprint 1–2: Foundation] ➔ [Sprint 3–4: Coordination] ➔ [Sprint 5–6: RCA & Quality] ➔ [Sprint 7–8: Analytics & CSAT]
 - Order Lifecycle Engine    - Vendor Matching Logic        - Snag Logging & RCA Engine   - KPI Executive Dashboards
 - Core DB Schema Setup      - Shipping API Integrations    - Delay Flagging Triggers     - Full Platform Handover
