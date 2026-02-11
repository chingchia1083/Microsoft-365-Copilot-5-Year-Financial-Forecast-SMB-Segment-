# 🤖 Microsoft 365 & Copilot 5-Year Financial Forecast (SMB Segment)

## 🚀 Executive Summary
This repository showcases a high-fidelity, **driver-based financial model** forecasting the performance of **Microsoft 365 (M365) Core** and the **Copilot AI Add-on** for the SMB segment (2026–2030). 

The model evaluates unit economics across **five key regions** (US, Eurozone, UK, Australia, Canada) and **three subscription tiers** (Business Basic, Standard, and Premium), providing a roadmap for AI monetization at scale.

---

## 🏗️ Model Architecture & Technical Innovation
The core differentiator of this project is the use of **Power Query** to automate complex subscription "waterfall" logic, eliminating the need for hundreds of manual Excel tables.
> **[INSERT SCREENSHOT: waterfall.png]**<img width="1545" height="462" alt="waterfall" src="https://github.com/user-attachments/assets/822fc892-b3ca-4421-ac80-704568d8850f" />


### 1. Automated Waterfall Engine
* **Dynamic Expansion**: Every row of Gross New Enrollees (GNE) is expanded to 20 quarters using the `List.Numbers` function.
* **Data Integrity**: Uses group all rows and index to simulate waterfall movements within a clean, tabular structure optimized for recurring revenue calculation.
* **Logic-Driven Revenue**: The engine calculates recurring revenue by merging unit prices with enrollee data through a join-and-multiply logic, ensuring automated accuracy across every period.

> **[INSERT SCREENSHOT: Power_Query_Steps.png]**

### 2. Enrollment Methodology
* **Top-Down Forecasting**: Starts with a baseline of **450M M365 Commercial Seats** with a 2% mature-market annual growth rate.
* **S-Curve Adoption**: Applies a progressive **Copilot Attach Rate** (starting at 8.0% in 2026 and scaling to 32.0% by 2030) to calculate incremental AI enrollees.

> **[INSERT SCREENSHOT: Enrollment_Forecast_Table.png]**

---

## 📊 Sophisticated Financial Drivers
The model incorporates advanced SaaS and AI-specific metrics:

* **Churn Dynamics**: Segmented by commitment type (Monthly vs. Annual). Accounts for **Trial Drop-offs** (up to 55%) vs. **Steady-State Churn** (as low as 0.4% for Premium Annual).
* **AI-Specific COGS**: Detailed modeling of incremental costs, including **One-time Data Indexing setup** ($1.50/GB), monthly storage maintenance, and GPU compute time ($4.00–$11.80/user depending on region).
* **Metered Revenue Layer**: Includes a consumption-based revenue forecast for Premium plans based on **Active User %** and **PAYG Trigger %**.

---

## 🧪 Scenario & Sensitivity Analysis
The model features **100+ scenarios and toggleable assumptions**, enabling users to stress-test the P&L through interactive slicers.

* **Assumptions Toggles**: Switch between "Best," "Middle," and "Worst" cases for Churn, Metered ARPU ($2 to $12), and Active User engagement.
* **Regional Deep-Dives**: Slicers allow for a single-region P&L view or a fully consolidated worldwide view.

> **[INSERT SCREENSHOT: P&L_Dashboard_with_Slicers.png]**

---

## 💡 Key Model Insights
* **US Market Dominance**: The US Copilot add-on for SMB is projected to reach **$9.5 Billion in Gross Margin by 2030**.
* **Global Scale**: Worldwide Copilot Gross Margin is forecasted at **$16.5 Billion by 2030**.
* **Margin Resilience**: While Basic/Standard plans maintain high margins (~90%), the **Business Premium plan is more cost-sensitive** (~58%–69%) due to intensive AI compute and data indexing requirements.
* **Consumption Upside**: Under "Best Case" scenarios, consumption-based revenue contributes **2.5% of total Copilot revenue**, representing a significant future growth lever.

---
