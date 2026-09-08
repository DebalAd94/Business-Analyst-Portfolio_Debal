# Scrum Foods | 24/7 Food Delivery Platform
**COEPD Capstone Project 2 — Agile-Scrum Implementation**

---

## 📌 Project Overview

**Scrum Foods** is an on-demand, multi-stakeholder food delivery platform designed to provide rapid, reliable, 24/7 food ordering and real-time delivery tracking across mobile, tablet, and desktop interfaces. The project was executed under the Agile-Scrum framework for client **COEPD IT Solutions**, simulating end-to-end product delivery from initial visioning to a shippable Minimum Viable Product (MVP) increment.

The platform orchestrates multi-sided operations among six distinct stakeholder groups: **Customers, Restaurants, Delivery Personnel, Regional Administrators, System Administrators, and Business Owners**. Within this project lifecycle, the role of **Product Owner (PO)** was undertaken to lead product visioning, backlog grooming, user story authoring with acceptance criteria, Business Value (BV) prioritization, sprint planning, and increment acceptance.

### Key Project Metadata
* **Project Name:** Scrum Foods (Food Delivery Applications)
* **Client Organization:** COEPD IT Solutions
* **Delivery Framework:** Agile Scrum (2-Week Sprints / 1-Day Daily Scrums)
* **Role Performed:** Product Owner (PO)
* **Scrum Master:** Satya Rathnakar
* **Scrum Development Team:** 8 Developers (Linesh Vegad, Yogender, Gowri, A. Lakshmikala, Madhuri, Varun, Rakesh, Rajesh)
* **Backlog Volume:** 52+ User Stories, Epics, and Technical Tasks
* **Sprint Cadence & Capacity:** 2-Week Sprints (10 working days), Target Velocity ~22–25 Story/Complexity Points (CP)

---

## 🛑 Business Problem

The competitive online food delivery market requires instant accessibility, total operational transparency, and high service availability. Traditional dining and manual ordering channels suffer from critical limitations:

### 1. Primary Market Bottlenecks
* **Lack of 24/7 Reliable Access:** Customers struggle to find quality-assured, hygienic meals during late-night or off-peak hours with predictable delivery windows.
* **Absence of Real-Time Visibility:** Lack of live GPS-enabled tracking causes delivery anxiety, high support ticket volume, and delivery route inefficiencies.
* **Fragmented Multi-Stakeholder Coordination:** Disconnect among restaurant kitchens, freelance delivery partners, and administrative hubs leads to order delays, food quality deterioration, and mismanaged dispute/refund workflows.
* **Operational Inefficiencies:** Restaurants lack dynamic menu controls and revenue dashboards, while delivery partners face opaque payout and order assignment systems.

### 2. Multi-Stakeholder Operational Scope

| Stakeholder Persona | Core Operational Pain Points & Platform Needs |
| :--- | :--- |
| **Customer** | Frictionless registration/login, location-based restaurant discovery (within 5 km radius), multiple payment options, live GPS tracking, and issue/refund self-service. |
| **Restaurant Partner** | Rapid onboarding approval, real-time incoming order feeds, kitchen dispatch time slot management, and settlement revenue tracking. |
| **Delivery Executive** | Streamlined self-registration (KYC validation), order acceptance/rejection controls, pickup-to-drop navigation, COD cash collection, and payout tracking. |
| **Regional Administrator** | Oversight of regional restaurant performance, delivery fleet load balancing, localized revenue reporting, and customer dispute/refund handling. |
| **System Administrator** | Global platform governance, restaurant & delivery partner approval/rejection workflows, system configuration, and audit trails. |
| **Business Owner** | High-level business analytics, aggregated regional revenue reports, margin optimization, and partner payout governance. |

---

## 🎯 Project Objectives

* **Rapid Time-to-Market via MVP:** Deliver a fully functional, testable Minimum Viable Product increment within the initial 2-week sprint focusing on the core ordering-delivery pipeline.
* **Continuous Value Delivery:** Maximize business ROI by prioritizing high Business Value (BV) features (Customer Registration, Menu Browsing, Payment Selection, Order Assignment) using Scrum Currency and MoSCoW frameworks.
* **Predictable Team Velocity:** Establish a steady delivery cadence across the 8-developer Scrum team, burning down 20–25 Complexity Points (CP) per 2-week sprint cycle.
* **High Quality & Release Readiness:** Enforce strict Definition of Ready (DoR) and Definition of Done (DoD) standards to eliminate technical debt and ensure zero-regression increment deliveries.
* **Multi-Sided Visibility:** Provide dedicated reporting and dashboard capabilities for Regional Admins and Business Owners to track regional performance and partner revenues.

---

## 🔄 Approach & Methodology

### 1. Agile Framework & Sprint Cadence
* **Sprint Length (Timebox):** 2 Weeks (10 working days), maintaining a strict, non-extendable timebox.
* **Daily Scrum (Daily Stand-up):** 15-minute daily synchronization addressing:
  1. *What did you accomplish yesterday?*
  2. *What will you work on today?*
  3. *What obstacles or impediments are blocking your progress?*
* **Sprint Planning:** 2-hour collaborative session where the Product Owner presents prioritized PBIs, the development team estimates story complexity via Planning Poker, and tasks are pulled into the Sprint Backlog.
* **Sprint Review & Demo:** Working software demonstration to stakeholders, evaluating completed story points against velocity and gathering direct client feedback.
* **Sprint Retrospective:** 1.5-hour team-focused meeting evaluating team dynamics, tooling, and process bottlenecks to formulate concrete action items for the next sprint.

### 2. Prioritization & Estimation Methodology
* **Business Value (BV) Estimation:** Estimated in collaboration with client stakeholders using **Scrum Currency Notes** (₹1000, ₹500, ₹200, ₹100, ₹50, ₹20, ₹10) to determine strategic importance and revenue impact.
* **Complexity Points (CP / Story Points):** Estimated exclusively by the 8 Scrum Developers using **Planning Poker** cards based on the Modified Fibonacci Sequence (0, 1, 2, 3, 5, 8, 13, 20, 40, 100).
* **Prioritization Framework:** Applied **MoSCoW** classification (Must Have, Should Have, Could Have, Won't Have) alongside the BV/CP ratio to identify the MVP baseline (high BV, manageable CP).

### 3. Quality Gates: DoR & DoD
* **Definition of Ready (DoR):** User story is INVEST-compliant; clear acceptance criteria are baselined; UI wireframes are attached; technical dependencies are identified; story point estimation is agreed upon.
* **Definition of Done (DoD):** Code written, reviewed, and merged into the main trunk; unit and integration tests passed; UI/UX verified against mocks; PO demonstration and acceptance sign-off completed; release notes generated.

---

## 📂 Business Analysis & Product Owner Artefacts Used

The project produced and utilized a comprehensive suite of Agile artifacts across the product lifecycle:

| Agile Lifecycle Phase | Artefacts & Deliverables Produced | Description & Focus |
| :--- | :--- | :--- |
| **Product Visioning & Strategy** | • Product Vision Document<br>• Stakeholder Matrix (6 Personas)<br>• Agile Manifesto Alignment Deck | Defined product vision statement, target demographics, value proposition, competitive differentiators, and strategic revenue streams. |
| **Backlog Engineering** | • Product Backlog (52+ Stories)<br>• Epic Breakdown Documents<br>• MoSCoW Prioritization Matrix | Formulated overarching epics (*Restaurant Ratings & Reviews*, *Scheduled Orders*); decomposed themes into granular, INVEST-compliant user stories. |
| **User Story Specification** | • INVEST User Story Cards<br>• Functional Acceptance Criteria<br>• BV & CP Valuation Matrices | Authored standardized user stories (`As a... I want to... So that...`) with explicit acceptance criteria, business rules (e.g., 5 km delivery radius, single payment selection), assigned BV (Scrum Currency), and CP (Poker Cards). |
| **Sprint Execution & Tracking** | • Sprint Backlog Task Board<br>• Impediments Log<br>• Definition of Ready (DoR) Checklist<br>• Definition of Done (DoD) Checklist | Maintained PBI-to-Task decomposition (`PBI → Tasks → WIP → Done`); logged operational blockers (e.g., Payment Gateway Sandbox delay, regional delivery shortages) with resolution tracking. |
| **Metrics & Burndown Analysis** | • Sprint Burndown Chart<br>• Product / Release Burndown Chart<br>• Velocity Tracking Log | Tracked day-by-day story point burn down across the 2-week cycle (22 CP target); monitored long-term release trajectory across sprints; evaluated 3-sprint rolling velocity averages. |
| **Scrum Ceremony Governance** | • Sprint Planning Agendas<br>• Daily Scrum Stand-up Logs<br>• Sprint Review Demo Scripts<br>• Retrospective Action Item Logs | Facilitated sprint ceremonies; baselined team action items for continuous engineering improvement. |

---

## 🧰 Agile Tooling Utilized

* **Agile Lifecycle & Backlog Management:** Atlassian JIRA Software (Scrum Boards, Backlog Refinement, Burndown Tracking)
* **Documentation & Knowledge Base:** Atlassian Confluence (Product Vision, Meeting Minutes, Retrospective Boards)
* **Estimation & Collaboration:** Planning Poker (Fibonacci story pointing), Scrum Currency Cards (BV valuation)
* **Process & Workflow Diagrams:** MS Visio, Lucidchart (Order lifecycle, Delivery state machines)
