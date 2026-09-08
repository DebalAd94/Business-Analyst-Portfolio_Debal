# AgriDirect | Online Agriculture Products Store
**COEPD Capstone Project 1 (Parts 1, 2, & 3) — Traditional & Hybrid SDLC**

---

## 📌 Project Overview

The **Online Agriculture Products Store (AgriDirect)** is a B2B/B2C agricultural e-commerce platform initiated under a Corporate Social Responsibility (CSR) program by **SOONY Company** (founded by Mr. Henry). The project was awarded to **APT IT SOLUTIONS** with a fixed contractual budget of **₹2.00 Crores INR** and an execution timeline of **18 Months**.

The platform is designed to disintermediate traditional rural agricultural supply chains by connecting remote farmers directly with manufacturers of **fertilizers, certified seeds, and chemical pesticides**. By bridging geographical barriers via accessible web and mobile touchpoints, the platform empowers rural farming communities with transparent pricing, guaranteed product authenticity, doorstep delivery, and flexible payment mechanisms.

### Key Project Metadata
* **Sponsor / Client:** Mr. Henry (SOONY Company, CSR Committee)
* **Client Committee:** Mr. Henry (Executive Sponsor), Mr. Pandu (Finance Head), Mr. Dooku (Project Coordinator)
* **Delivery Partner:** APT IT SOLUTIONS
* **Key Delivery Leads:** Mr. Karthik (Delivery Head), Mr. Vandanam (Project Manager)
* **Key Stakeholders / Farmer Representatives:** Peter, Kevin, Ben
* **BA Role:** Lead Business Analyst (Requirements Engineering, Process Modeling, Traceability, UAT Governance)
* **Contract Model:** Fixed Bid (₹2.00 Cr hard limit)

---

## 🛑 Business Problem

Rural farming communities face systemic supply chain exploitation and severe logistical overhead when procuring critical farm inputs.

### 1. Primary Pain Points
* **Physical Travel & Sunk Productivity:** Farmers travel long distances to distant district market centers to buy basic supplies, disrupting seasonal planting and sowing cycles.
* **Middlemen Price Exploitation:** Local intermediaries and multi-tiered brokers artificially mark up prices by **20% to 50%** over wholesale rates.
* **Stockouts & Counterfeit Risks:** Rural supply lines suffer from zero real-time inventory visibility, resulting in frequent stockouts during peak monsoon/sowing seasons. Farmers are also vulnerable to spurious, expired, or non-certified pesticides and adulterated seeds.
* **Cash-Only Dependency & Delivery Deficits:** Traditional suppliers lack digital payment support and offer zero fulfillment logistics to rural farming plots.

### 2. AS-IS vs. TO-BE Gap Analysis

| Business Dimension | AS-IS State (Manual / Intermediary Dependent) | TO-BE State (AgriDirect Digital Platform) |
| :--- | :--- | :--- |
| **Accessibility** | Physical travel to distant brick-and-mortar stores; fragmented localized stock. | 24/7 web & mobile catalog access with category/crop filters. |
| **Procurement Cycle** | Days to weeks required for travel, negotiation, and cartage. | Minutes to search, add to cart, and checkout with instant confirmation. |
| **Pricing & Margin** | Middlemen inflate retail costs by 20–50%; zero price transparency. | Direct manufacturer pricing, transparent invoicing, and bulk discounts. |
| **Quality & Trust** | No certification records; high incidence of fake seeds/chemicals. | Verified manufacturer profiles, technical spec sheets, and batch certificates. |
| **Payment Modes** | Cash-driven; high personal risk and delayed ledger settlements. | Omnichannel checkout: Cash on Delivery (COD), UPI, and Credit/Debit cards. |
| **Order Tracking** | Paper receipts; no delivery transit visibility. | Automated SMS/email updates and end-to-end GPS delivery tracking. |

---

## 🎯 Project Objectives

* **Digital Accessibility & Ease of Use:** Deliver a user-friendly, responsive web and mobile application tailored for users with varying digital literacy, meeting **WCAG 2.1** standards and achieving sub-2-second page load times.
* **Supply Chain Disintermediation:** Establish direct manufacturer-to-farmer communication and procurement channels, cutting overall farming procurement costs by up to **30%**.
* **Rapid Turnaround & Fulfillment:** Standardize order-to-delivery fulfillment within a **24–48 hour** logistics window.
* **Contract & Financial Governance:** Execute all deliverables within the **₹2.00 Crore** budget and **18-month** timeframe, achieving projected ROI payback within **29 months** (11 months post-launch).
* **System Stability & Reliability:** Guarantee **99.5%** monthly system uptime, atomic transaction integrity across order/payment states, and high concurrency resilience.

---

## 🔄 Approach & Methodology

### 1. SDLC Methodology: Phased V-Model
Following committee deliberations on Waterfall, RUP, Spiral, and Agile Scrum, the team adopted a **V-Model (Verification and Validation)** approach:
* **Simultaneous Verification:** Development stages (Requirements Gathering, Analysis, Architecture Design, Module Drops D1–D4) are mapped 1:1 with corresponding validation planning (Unit Testing T1–T4, System Testing, and UAT).
* **Budget & Scope Control:** Fits the 18-month contractual timeline and 15-member team structure while providing fixed-bid budget protection against uncontrolled scope creep.
* **Early Defect Containment:** Test cases and acceptance criteria are derived during the requirements and design phases, drastically reducing late-stage defect remediation costs.

### 2. System Architecture: 3-Tier Enterprise Framework
* **Presentation Tier:** Responsive web (React) and mobile-optimized interfaces designed for seamless product discovery, guest browsing, and multi-mode checkout.
* **Application Tier:** Java enterprise engine powered by **Spring Boot** (led by Senior Java Developer Ms. Juhi) managing business logic, payment gateway APIs (Razorpay), inventory validation, and tax engines.
* **Data Tier:** Relational database schema (**MySQL / PostgreSQL** managed by DB Admin John) structured across 7 core entities with ACID transaction compliance.

### 3. Governance, RACI, & Change Management
* **RACI Alignment:** High-interest/high-power sponsors (Mr. Henry, Mr. Karthik) govern milestone approvals; key farmers (Peter, Kevin, Ben) serve as consultative domain advisors.
* **Quarterly Milestone Audits:** Four formal audits (Q1 BRD, Q2 SRS/UML, Q3 Architecture/Design, Q4 SIT/UAT) govern progression across stage gates.
* **Scope Governance (CR vs. Enhancement):** Statutory compliance changes (e.g., GST structure revisions) are processed through a structured 5-step Change Request workflow. Major feature expansions (e.g., C2C Farmer Produce Auctions) are formally branched as Phase-2 enhancements.

---

## 📂 Business Analysis Artefacts Used

The Business Analyst delivered and baselined a comprehensive suite of artefacts across all phases of the project lifecycle:

| SDLC Phase | BA Deliverable / Artefact | Description & Purpose |
| :--- | :--- | :--- |
| **Enterprise Analysis & Scoping** | • Business Case Document<br>• Feasibility Study Report<br>• SWOT Analysis Matrix<br>• Stakeholder RACI & ILS Matrix | Evaluated financial/technical feasibility (Java/AWS/MySQL); documented 29-month ROI break-even; mapped stakeholder influence/interest. |
| **Requirements Engineering** | • Business Requirements Document (BRD)<br>• Functional Specs (FR0001–FR0020)<br>• Non-Functional Specs (NFR0101–NFR0108)<br>• Assumptions & Constraints Log | Baselined 12 prioritized BRs and 20 functional requirements covering registration, catalog, cart, multi-payment options, and order notifications. |
| **Process & Visual Modeling** | • Business Process Model (BPMN)<br>• UML Use Case Diagrams & Specs<br>• UML Activity Diagrams (MS Visio)<br>• Level-1 Data Flow Diagram (DFD) | Detailed 5+ core use case specifications (Search, Login, Place Order, Product Upload, Alerts); created activity diagrams with decision nodes/forks/joins; mapped DFD across `ItemMst`, `UserMst`, and `OrderMst`. |
| **UI Wireframing & Prototyping** | • Balsamiq Low-Fidelity Wireframes | Designed screen layouts for 5 core journeys: (1) Farmer Home & Catalog, (2) Registration, (3) Manufacturer Upload & Approval Dashboard, (4) Cart & Checkout, (5) Order Tracking Timeline. |
| **Data Architecture Collaboration** | • Database Schema Blueprint<br>• Entity-Relationship (ER) Diagram | Modeled 7 relational tables (`USERS`, `PRODUCTS`, `ORDERS`, `ORDER_ITEMS`, `ADDRESSES`, `WISHLIST`, `PAYMENTS`) with foreign key constraints. |
| **Traceability & Verification** | • Requirements Traceability Matrix (RTM)<br>• 10 Functional Test Case Documents<br>• Defect Triaging & Severity Matrix | Established 100% bi-directional requirement-to-test mapping; created test suites (TC_001 to TC_010) covering validation rules, load testing (100 concurrent users), and payment flows. |
| **Project Closure & Operations** | • UAT Test Plan & Execution Log<br>• Client Project Acceptance Form<br>• Project Closure Report<br>• BA SDLC Timesheets | Managed 5-stage UAT (150 test scripts, 95.3% pass rate, zero critical bugs); captured project metrics (₹1.56 Cr spent of ₹2.00 Cr budget; NPS 8.7/10); logged BA timesheets across SDLC phases. |

---

## 🧰 Tools Utilized

* **Diagramming & Process Modeling:** MS Visio, Draw.io
* **UI/UX Wireframing:** Balsamiq Mockups Desktop
* **Requirements & Backlog Governance:** JIRA, Confluence, Microsoft Word & Excel
* **Architecture & Database Modeling:** UML 2.5, MySQL Workbench
