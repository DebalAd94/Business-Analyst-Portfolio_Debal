# OmniPay Flow | Omnichannel Payment Processing System
**Technical Systems Analysis & Object-Oriented Design Specification**

---

## 📌 Project Overview

The **Omnichannel Payment Processing System (OmniPay Flow)** is an enterprise transaction routing and settlement module designed for the **Scrum Foods On-Demand Delivery Ecosystem**. Developed as a critical component of the platform checkout and billing architecture, OmniPay Flow orchestrates multi-modal transaction processing across four primary consumer payment instruments: **Credit/Debit Card**, **Digital Wallet**, **Cash on Delivery (COD)**, and **Net Banking**.

The system mitigates transaction drop-offs at checkout by abstracting disparate financial protocols, third-party banking gateways, and internal customer ledgers into a unified, secure processing engine. Adhering to **3-Tier Enterprise Architectural Standards**, **PCI-DSS guidelines**, and **RBI directives**, this deliverable highlights end-to-end technical business analysis—spanning use case behavioral modeling, Robustness Analysis (Boundary-Controller-Entity stereotypes), Net Banking domain engineering, and interaction sequence flows.

### Key Project Metadata
* **Project Name:** OmniPay Flow (Omnichannel Payment Processing System)
* **Parent Platform:** Scrum Foods On-Demand Delivery Ecosystem
* **Document Type:** Technical Systems Analysis & Object-Oriented Architecture Specification
* **Stakeholder Groups:** Customers, Core Banking Partners, Payment Gateway Aggregators, Delivery Executives, System Administrators
* **Core Standards:** UML 2.5, 3-Tier Layered Architecture, Robustness Analysis (BCE), TLS 1.3 Encryption, Idempotency Standards
* **BA Competencies:** System Use Cases, Stereotype Class Derivations, Architectural Layer Mapping, Sequence Modeling, Domain & Conceptual Data Engineering

---

## 🛑 Business Problem

During initial elicitation sessions for the checkout and billing journey, stakeholders identified that payment friction, limited instrument availability, and system drop-offs directly erode checkout conversion rates and brand trust.

### 1. Primary Market & Operational Challenges
* **Cart Abandonment via Payment Restrictions:** Consumers demand diverse payment methods tailored to situational convenience (e.g., instant UPI/wallets for speed, Net Banking for high-value transactions, cards for rewards, or COD for first-time trust). Lack of immediate instrument availability causes cart abandonment.
* **Complex Third-Party Banking Asynchrony:** Net Banking and external banking APIs involve asynchronous redirects, out-of-band user authentication (OTP/credentials), and delayed status callbacks, creating race conditions, orphan orders, or double deductions.
* **Security & Regulatory Mandates:** Storing sensitive banking credentials on internal application servers violates PCI-DSS and financial regulatory directives. Payment flows require strict architectural separation with TLS 1.3 and payload hashing.
* **Reconciliation & Settlement Fragmentation:** Processing cash handoffs through delivery executives alongside digital gateway authorizations creates reconciliation bottlenecks between internal order ledgers and external merchant settlement accounts.

### 2. Omnichannel Transaction Modes

| Payment Instrument | Operational Flow & Validation Mechanism | Settlement State & Responsibility |
| :--- | :--- | :--- |
| **Credit / Debit Card** | Capture card credentials via secure tokenized iFrame; route to payment gateway for 3D Secure OTP verification. | Instant gateway authorization; settlement batch cleared asynchronously. |
| **Digital Wallet** | Elicit wallet provider/identifier; query available account balance; authorize one-click debit. | Immediate ledger deduction from internal/partner wallet service. |
| **Cash on Delivery (COD)** | Validate delivery address feasibility; generate COD invoice; bypass online payment gateways. | Transaction placed in `Pending Collection`; physical cash collected by Delivery Executive upon delivery. |
| **Net Banking** | Populate list of approved financial institutions; redirect user session to external core banking portal; process secure callback. | Asynchronous callback handling; order marked `Paid` upon digital handshake verification. |

---

## 🎯 Project Objectives

* **Omnichannel Payment Enablement:** Support four primary payment instruments (Card, Wallet, Cash, Net Banking) within a unified checkout workflow.
* **Robust Tiered Separation:** Enforce strict decoupling across the Presentation Tier (Boundaries), Business Logic Tier (Controllers), and Data Persistence Tier (Entities) using Robustness Analysis principles.
* **Transactional Reliability & Idempotency:** Implement idempotency keys and atomic state updates to eliminate duplicate deductions, system timeouts, or ledger inconsistencies.
* **Zero-Trust Security Compliance:** Ensure zero storage of unencrypted banking credentials or card CVVs, operating under TLS 1.3 with SHA-256 encrypted payload handshakes.
* **Asynchronous Status Reconciliation:** Standardize Net Banking external redirection and callback listener services to provide sub-second transaction status resolution.

---

## 🔄 Approach & Methodology

The analysis and technical modeling followed an **Object-Oriented Analysis and Design (OOAD)** approach integrated with the **Unified Modeling Language (UML 2.5)** and **Robustness Analysis**:

### 1. Use Case & Behavioral Modeling
* Mapped user interactions within the payment boundary, isolating the primary actor (**Customer**) and external secondary actor systems (**Server / Core Banking System / Gateways**).
* Structured behavioral dependencies using UML `<<extends>>` stereotypes where the core *View Payment Options* use case is extended dynamically based on the customer's payment selection.

### 2. Robustness Analysis (BCE Framework)
To transition from functional requirements (`FR-PAY-01` to `FR-PAY-06`) to enterprise system design, requirements were decomposed into three standardized class stereotypes:
* **Boundary Classes (`<<boundary>>`):** Interface components that facilitate communication between system actors and internal software components (UI screens, input forms, payment gateways).
* **Controller Classes (`<<controller>>`):** Central orchestrators encapsulating business rules, validations, cryptographic handshakes, and routing logic.
* **Entity Classes (`<<entity>>`):** Persistent domain objects encapsulating transactional states, account balances, and customer attributes.

### 3. 3-Tier Enterprise Architectural Mapping
* **Presentation Tier:** Hosts all boundary interfaces (`PaymentOptionBoundary`, `NetBankingPaymentBoundary`, etc.), ensuring loose coupling from back-end transactional rules.
* **Application / Business Logic Tier:** Hosts controller services (`PaymentController`, `PaymentProcessorController`) executing business rules, payment routing, and gateway adapters.
* **Data Tier:** Houses persistent entities (`Customer`, `Payment`, `Transaction`) and relational database tables, guaranteeing transactional ACID properties.

### 4. Chronological Interaction Modeling (Sequence Diagram)
* Modeled the end-to-end runtime lifecycle of a **Net Banking transaction**, tracing synchronous requests from the Customer UI through the Net Banking Controller, the external Bank Core System (authentication, validation, balance deduction), and asynchronous confirmation callbacks.

---

## 📂 Business Analysis & System Design Artefacts Used

The technical deliverables produced and baselined for this project include:

| Analysis Category | Technical Artefact Produced | Description & Key Architectural Focus |
| :--- | :--- | :--- |
| **Functional Modeling** | • System Use Case Diagram<br>• Use Case Narrative Specification | Modeled *Payment Initiation* and *View Payment Options*, detailing behavioral extensions for Cash, Net Banking, UPI/Wallet, and Debit/Credit Card. |
| **Robustness Analysis** | • Boundary-Controller-Entity (BCE) Matrix<br>• Stereotype Class Catalog | Derived 5 Boundary classes, 2 Controller orchestrators, and 3 persistent Entity models, documenting responsibilities and communication paths. |
| **System Architecture** | • 3-Tier Layered Deployment Mapping | Mapped BCE classes directly across the Presentation Tier (UI/Gateways), Business Logic Tier (Rules/Routing), and Data Tier (Database Persistence). |
| **Domain Engineering** | • Net Banking Domain Model (UML Class Diagram)<br>• Structural Relationship Catalog | Elaborated structural domain objects for Net Banking transactions: `Customer`, `Bank`, `Account`, `Authentication` (Username, Password, OTP), `Net Banking Service`, `Payment`, and `Transaction`. |
| **Interaction Modeling** | • Net Banking Sequence Diagram (UML 2.5)<br>• Gateway Callback Interaction Spec | Mapped sequential messages: Request Initiation → Bank Authentication → Validation → Balance Deduction → Inter-bank Routing → Payment Confirmation. |
| **Conceptual Modeling** | • High-Level Conceptual Model<br>• Entity-Attribute-Relationship Matrix | Defined high-level business abstractions (`Customer`, `PaymentMethod`, `Transaction`), capturing cardinality (`1:N`, `1:1`) and business integrity constraints. |

---

## 🏗️ Technical Class Derivations & Architecture Summary

### 1. Robustness Class Derivation Matrix

| Stereotype | Class Name | Tier Placement | Architectural Responsibilities |
| :--- | :--- | :--- | :--- |
| **Boundary** | `PaymentOptionBoundary` | Presentation Tier | Renders checkout UI; captures customer payment instrument selection. |
| **Boundary** | `CardPaymentBoundary` | Presentation Tier | Tokenizes cardholder data; handles 3D Secure redirection. |
| **Boundary** | `WalletPaymentBoundary` | Presentation Tier | Interacts with digital wallet providers; displays wallet balance check. |
| **Boundary** | `CashPaymentBoundary` | Presentation Tier | Captures COD acknowledgment; displays cash collection notice. |
| **Boundary** | `NetBankingPaymentBoundary` | Presentation Tier | Displays approved bank list; manages redirect to bank login portal. |
| **Controller** | `PaymentController` | Business Logic Tier | Coordinates overall payment flow; validates request payload and selection. |
| **Controller** | `PaymentProcessorController` | Business Logic Tier | Executes business rules; communicates with external bank APIs; handles callback integrity. |
| **Entity** | `Customer` | Data Tier | Persistent entity maintaining `customerID`, `name`, `accountBalance`, and profile. |
| **Entity** | `Payment` | Data Tier | Persistent record storing `paymentID`, `amount`, `method`, `timestamp`, and `status`. |
| **Entity** | `Transaction` | Data Tier | Transactional audit record storing `transactionID`, references, and settlement details. |

### 2. High-Level Conceptual Relationships
* **`Customer (1)` initiates `PaymentMethod (*)`:** A customer can maintain and select multiple payment options across checkout transactions.
* **`PaymentMethod (*)` produces `Transaction (1)`:** Each selected payment instrument executes an isolated transaction event.
* **`Transaction (1)` belongs to `Customer (1)`:** Enforces strict audit ownership, customer order linking, and financial traceability.

---

## 🧰 Tools Utilized

* **Diagramming & Architecture Modeling:** Microsoft Visio, UML 2.5
* **Requirements & Traceability Engineering:** Atlassian Confluence, Microsoft Word
* **Interface & Interaction Prototyping:** Balsamiq Mockups
