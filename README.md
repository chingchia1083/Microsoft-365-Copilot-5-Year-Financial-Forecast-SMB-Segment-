# 🤖 Microsoft 365 & Copilot 5-Year Financial Forecast (SMB Segment)

## 🚀 Key Model Features
This repository contains a high-fidelity, **driver-based financial model** forecasting the performance of **Microsoft 365 (M365) Core** revenue and the **Copilot AI Add-on** for the Small and Medium Business (SMB) segment from **2026 to 2030**. 

The model analyzes unit economics across **five key regions** (US, Eurozone, UK, Australia, Canada) and **three subscription tiers** (Business Basic, Standard, and Premium). It is designed to evaluate the margin impact of transitioning from traditional SaaS to an AI-enabled "Seat + Consumption" revenue model.

---

* **Comprehensive Driver-Based Forecasting**: Delivers a granular, 5-year projection (2026–2030) of Microsoft 365 (M365) Core revenue alongside the Copilot AI Add-on specifically for the SMB segment.**.
* **Advanced Scenario Engine (100+ Permutations)**: Robust architecture with **toggleable assumptions**. Users can switch between **Single Scenario views** (individual plan/region) and **Aggregated Global views**.
* **Automated ETL Pipeline**: Utilizes **Power Query** to handle complex data transformations, ensuring the model remains **scalable** and can be **refreshed instantly** as underlying data changes.
* **Dynamic Scalability**: Modular design allows the forecast horizon to be extended indefinitely beyond the 5-year baseline.

---

## 💡 Key Model Insights

* **Copilot as a Margin-Protection Engine**: While Core M365 revenue shows a slight decline in the model (dropping from $34B in 2026 to $31B in 2030), Copilot revenue grows from $6B to $20B over the same period.Insight: Copilot isn't just an add-on; it is the primary driver of Gross Margin (GM) expansion. By 2030, Copilot is projected to contribute $16B in GM at a consistent 79% margin, effectively offsetting the stagnation in the core business.
* **Margin Resilience**: While Basic/Standard plans maintain high margins (~90%), the **Business Premium plan is more cost-sensitive** (~58%–69%) due to intensive AI compute and data indexing requirements.
* **Consumption Upside**: Under "Best Case" scenarios, consumption-based revenue contributes **2.5% of total Copilot revenue**, representing a significant future growth lever.
* **Regional Profitability Disparity**:The regional P&L breakdown reveals that the United States is the absolute anchor of the Copilot program, but the Eurozone is the critical secondary market for scale. UK has lowest Copilot GM rate due to higer AI associated cost.  


---

## 🏗️ Model Architecture & Technical Innovation
The core differentiator of this project is the use of **Power Query** to automate complex subscription "waterfall" logic, eliminating the need for hundreds of manual Excel tables.
> **[typical waterfall table]**
> <img width="1545" height="462" alt="waterfall" src="https://github.com/user-attachments/assets/822fc892-b3ca-4421-ac80-704568d8850f" />


### 1. Automated Waterfall Engine in *Power Query*
The model executes waterfall logic by transforming each enrollee record into multiple rows—one for each forecast period—to capture recurring revenue streams. It then merges these records with unit pricing by region and plan, calculating the final P&L amounts through record-level multiplication.

> **[Power_Query_Steps]**
> <img width="263" height="547" alt="query steps" src="https://github.com/user-attachments/assets/7998d495-988e-4510-a2ed-46b7842e0dfa" />


### 2. Enrollment Methodology
* **Top-Down Forecasting**: Starts with a baseline of **450M M365 Commercial Seats** with a 2% mature-market annual growth rate.
* **S-Curve Adoption**: Applies a progressive **Copilot Attach Rate** (starting at 8.0% in 2026 and scaling to 32.0% by 2030) to calculate incremental AI enrollees.

> **[Enrollment_Forecast_Table.]**
<img width="1223" height="451" alt="GNE Assumption" src="https://github.com/user-attachments/assets/3a2959dd-4693-46a4-b64c-3c4010c87f68" />
<img width="1297" height="416" alt="GNE by country" src="https://github.com/user-attachments/assets/a8a78879-1ead-440f-a605-65537f4926f2" />

---

## 📊 Sophisticated Financial Drivers
The model incorporates advanced SaaS and AI-specific metrics:

* **Churn Dynamics**: Segmented by commitment type (Monthly vs. Annual). Accounts for **Trial Drop-offs** (up to 55%) vs. **Steady-State Churn** (as low as 0.4% for Premium Annual).
* **AI-Specific COGS**: Detailed modeling of incremental costs, including **One-time Data Indexing setup** ($1.50/GB), monthly storage maintenance, and GPU compute time ($4.00–$11.80/user depending on region).
* **Metered Revenue Layer**: Includes a consumption-based revenue forecast for Premium plans based on **Active User %** and **PAYG Trigger %**.
> **[Unit Economic Assumptions.]**
<img width="2400" height="1002" alt="unit price" src="https://github.com/user-attachments/assets/0034c018-fecb-42cf-94b1-cf8487cc4d62" />

---

## 🧪 Scenario & Sensitivity Analysis
The model features **100+ scenarios and toggleable assumptions**, enabling users to stress-test the P&L through interactive slicers.

* **Assumptions Toggles**: Switch between "Best," "Middle," and "Worst" cases for Churn, Metered ARPU ($2 to $12), and Active User engagement.
* **Regional Deep-Dives**: Slicers allow for a single-region P&L view or a fully consolidated worldwide view.

> **[P&L_Dashboard_with_Slicers]**
<img width="628" height="814" alt="single scenario view" src="https://github.com/user-attachments/assets/65a6b5a5-c6b0-4f0b-b272-67c36819764c" />
<img width="598" height="812" alt="aggregate view" src="https://github.com/user-attachments/assets/2ea303cd-1edc-475c-be39-111e9f20f099" />

---

