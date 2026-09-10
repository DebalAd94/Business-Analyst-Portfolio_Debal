# UI/UX Wireframes & Interactive Prototypes

This directory contains the user interface wireframes, screen architecture blueprints, and interactive prototypes developed for the **ResolveSphere B2B Customer Issue Resolution Platform**.

---

## 📌 Prototyping Overview

To bridge the gap between abstract business requirements and frontend technical execution, the complete user interface was prototyped using **Axure RP Pro 7**. 

Axure RP Pro 7 was chosen to simulate real-world B2B CRM interactions, validate complex operational workflows with stakeholders, and provide the engineering team with clear behavioral specifications for widget states, modal overlays, and responsive layouts.

### Key Tooling Capabilities Applied
* **Dynamic Panels & States:** Used to simulate tab switching (Comments, Internal Help, JIRA Details, Content Audits) and persistent multi-case tabs without page refreshes.
* **Modal Windows & Overlays:** Modeled the 2-step JIRA issue creation wizard, displaying contextual warnings and backend synchronization behavior on top of active case records.
* **Interactive Form Logic:** Simulated validation states for required fields, character limits, PII warnings, and button enable/disable conditions.
* **Widget Libraries & Master Components:** Maintained reusable headers, global search bars, SLA countdown timers, and customer metadata sidebars across all screens.

---

## 🖥️ Prototyped Screen Inventory

| Screen / Blueprint | View Type | Key Functional Elements Modeled |
| :--- | :--- | :--- |
| **01. Support Specialist Home Dashboard** | Kanban & Workspace View | Multi-status queue lanes (New, Open, Pending, On Hold, Solved), global search bar, real-time chat window, AI response spot-checking panel, ReTool/LogRocket quick-launch actions. |
| **02. Case Management Details View** | Primary Agent Console | Active case tabs (e.g., `#2267821`), SLA milestone countdown clocks, high-ARR customer warning banners, customer metadata sidebar, and rich-text comment feeds. |
| **03. JIRA Integration Tab View** | Case Sub-Module | Existing linked JIRA issues table, development comments stream, and quick-action triggers for creating new issues or associating existing engineering tickets. |
| **04. Create JIRA Issue (Modal Step 1)** | Modal Dialog | Project selection dropdown, Issue Type picker, and an automated synchronization impact explanation detailing the backend webhook linkage. |
| **05. Create JIRA Issue (Modal Step 2)** | Modal Form | Summary input field, formatted issue description body, priority selector (Highest), component picker, critical blocker toggles, and ReTool/LogRocket link attachments. |
| **06. Stakeholder Executive Portal** | C-Level Client Dashboard | Macro KPI tiles (Ongoing Cases, Resolved Cases, MTTR at 48H), interactive case status grid, direct chat-with-support flyout, and report generation triggers. |

---

## 📂 Directory Contents

* `Screenshots/`: High-resolution PNG exports of all operational screens and modal states for fast visual reference.
* `ResolveSphere_Prototypes.rp`: Editable source project file created in **Axure RP Pro 7**, containing page hierarchies, masters, and interactive widget logic.
* `HTML-Prototype-Export/`: Standalone compiled HTML/CSS/JS export generated directly from Axure RP for interactive browser testing and stakeholder walkthroughs.
