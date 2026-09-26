# Renewable Energy and Community Impact: M&E Performance Dashboard

## Overview
This project presents an evaluation of operational performance and community impact across renewable energy and development interventions. Using operational data, the analysis evaluates target achievement, clean-energy access adoption, system reliability, training-to-employment translation, and overall intervention performance across multiple target states. 

The primary objective is to provide program managers and decision-makers with data-backed insights to guide resource allocation, optimize program delivery, and address last-mile execution challenges.

> **Note:** The analysis presented in this project is based on a **Mock/Simulated Dataset**.


## Business Problem
Monitoring and evaluating development programs across diverse geographical regions poses significant operational challenges. Program managers often face difficulty in:
* Identifying specific states or regions falling behind target beneficiary allocations.
* Measuring the real gap between initial access provision and sustained clean-energy adoption.
* Determining whether capacity-building efforts (such as skills training) lead to concrete local employment outcomes.
* Distinguishing top-performing intervention types from underperforming ones to inform future budget distribution.

Without structured data-driven tracking, strategic planning risks being based on anecdotal evidence rather than measurable operational performance.

## Project Objectives
1. **Identify Performance Gaps:** Evaluate state-level beneficiary delivery against established target benchmarks.
2. **Assess Last-Mile Access:** Quantify the deficit between recorded beneficiaries and actual operational clean-energy access.
3. **Evaluate Operational Quality:** Examine patterns connecting system reliability to community satisfaction.
4. **Evaluate Program Outcomes:** Assess how effectively training programs translate into local job creation.
5. **Rank Interventions:** Benchmark the overall performance of distinct intervention models to identify high-impact strategies.

## Business Questions
This analysis directly answers six core operational questions:
1. Which interventions/states are missing their targets?
2. Are beneficiaries actually gaining clean-energy access?
3. Does reliability relate to community satisfaction?
4. Is training translating into local jobs?
5. Which interventions demonstrate the strongest overall performance?
6. What does the community impact profile look like across states?

## Dataset
* **Dataset Description:** The dataset is a simulated one for M&E Community impact analysis
* **Dataset Size:** 80 Rows, 21 Columnns
* **Data Source:** Mock/Simulated Dataset


## Data Preparation
The dataset was audited for quality and prepared for analytical aggregation through the following steps:

* **Data Quality Verification:** Verified that the dataset contained no missing values, empty cells, or duplicate records.
* **Calculated Fields & Metrics Creation:** Created calculated fields using explicit business logic and mathematical formulas:

| Metric Name | Analytical Purpose | Formula / Logic |
| :--- | :--- | :--- |
| **Achievement Gap** | Measures performance improvement relative to baseline| `Current_Achievement_% - Baseline_%`|
| **Target Gap** | Measures variance from target benchmark| `Current_Achievement_% - Target_%`|
| **Target Achievement Rate** | Evaluates proportion of target completed| `Current_Achievement_% / Target_%`|
| **Clean Energy Access Rate** | Evaluates proportion of beneficiaries with active energy access| `People_Gaining_Clean_Energy_Access / Beneficiaries`|
| **Training-to-Employment Rate** | Measures conversion of skills training into local jobs| `Local_Jobs_Created / People_Trained`|
| **Unserved Beneficiaries** | Quantifies beneficiaries currently lacking active clean-energy access| `Beneficiaries - People_Gaining_Clean_Energy_Access`|
| **Performance Status** | Categorizes entities as meeting, exceeding, or underperforming targets| Nested IF statements|


## Tools & Technologies

| Tool | Purpose |
| :--- | :--- |
| **Excel** | Primary data storage, data preparation, KPI calculations, PivotTables, and dashboard creation |
| **[SQL]** | [Data querying and analytical aggregations] |

## Analytical Approach
The analytical workflow combined structured aggregation, comparative benchmarking, and qualitative performance scoring:
* **PivotTables & Aggregations:** Summarized beneficiary targets, actual reach, reliability metrics, and job figures at state and intervention levels.
* **KPI Calculations:** Calculated target variances (Actual vs. Target) and percentage gaps between registered beneficiaries and active clean-energy access.
* **Comparative & Cross-State Analysis:** Evaluated state-level variances to highlight regional disparities in delivery.
* **Intervention Performance Scoring:** Benchmarked intervention models based on composite impact scores.
* **Filterable Slicer Integration:** Integrated dynamic cross-filtering by state and intervention type to allow flexible stakeholder exploration.


## Dashboard
The interactive dashboard provides program stakeholders with an end-to-end view of intervention metrics, combining high-level summary cards with granular comparative visuals.

![Dashboard Preview](INSERT_SCREENSHOT_LINK)

### Core Features & Stakeholder Utility:
* **KPI Summary Cards:** High-level overview of aggregate target progress, clean-energy adoption gaps, and overall community satisfaction.
* **Target Variance Charts:** Visual breakdown highlighting regional shortfalls and overachieved targets.
* **State & Intervention Slicers:** Interactive filtering allowing users to drill down into specific states or compare particular intervention models.
* **Community Impact Indicators:** Visual metrics comparing system reliability side-by-side with community feedback ratings.


## Key Insights

### 1. Target Performance
A comparative review of regional beneficiary targets reveals noticeable delivery variations across states, with four states exceeding projections and four failing to meet target benchmarks:

| State | Target Variance (Actual vs. Target) | Performance Bar | Status |
| :--- | :---: | :--- | :--- |
| **Delta** | +13 | `█████████████` | Above Target |
| **Oyo** | +7 | `███████` | Above Target |
| **Rivers** | +4 | `████` | Above Target |
| **Edo** | +2 | `██` | Above Target |
| **Enugu** | -10 | `░░░░░░░░░░` | Below Target |
| **Kwara** | -14 | `░░░░░░░░░░░░░░` | Below Target |
| **Lagos** | -18 | `░░░░░░░░░░░░░░░░░░` | Below Target |
| **Ogun** | -19 | `░░░░░░░░░░░░░░░░░░░` | Below Target |

* **Data Breakdown:** Ogun (-19), Lagos (-18), Kwara (-14), and Enugu (-10) failed to meet beneficiary targets, with Ogun recording the largest deficit. Delta (+13), Oyo (+7), Rivers (+4), and Edo (+2) surpassed target projections.
* **Business Implication:** The deficit in Ogun, Lagos, Kwara, and Enugu points to localized execution bottlenecks, resource constraints, or overly optimistic target setting. Operational resources may need to be reallocated from overperforming states to support struggling regions.


### 2. Clean-Energy Access
An evaluation of recorded beneficiaries versus actual active clean-energy access shows a persistent gap across all evaluated states:

| State | Beneficiaries | Actual Access | Gap / Deficit |
| :--- | :--- | :--- | :--- |
| **Anambra** | 16.6K | 13.9K | -2.7K |
| **Kwara** | 14.7K | 11.8K | -2.9K |
| **Plateau** | 12.1K | 10.9K | -1.2K |
| **Kaduna** | 9.1K | 8.0K | -1.1K |
| **Ogun** | 7.8K | 6.2K | -1.6K |
| **Lagos** | 7.5K | 6.0K | -1.5K |

* **Business Implication:** While clean-energy interventions are reaching substantial numbers, the deficit across all six states points to last-mile adoption and installation friction. Enrolling beneficiaries does not automatically guarantee operational energy access.


### 3. Reliability & Community Satisfaction
* **Finding:** Higher system reliability generally aligns with higher community satisfaction ratings, though this relationship is not uniform across all observed data points.
* **Business Implication:** While system uptime is a key factor in community satisfaction, non-reliability factors (e.g., customer support, user expectations, or pricing) likely influence satisfaction as well.

### 4. Training & Local Jobs
* **Finding:** Skills training programs contribute to local job creation, but outcome volumes vary significantly across different interventions.
* **Business Implication:** Training alone does not guarantee employment. Long-term job creation depends heavily on post-training absorption capacity, regional economic activity, and industry partnerships.

### 5. Intervention Performance
Interventions were evaluated and scored based on performance across key indicators:

| Intervention | Performance Score |
| :--- | :--- |
| **Community Energy Access** | **17** |
| **Solar Backup System** | **15** |
| **Solar Water Pump** | **15** |
| **Solar Mini-grid** | **12** |
| **Institutional Capacity Building** | **12** |
| **Skills Training** | **9** |

* **Business Implication:** Infrastructure-focused energy delivery solutions demonstrate stronger quantifiable outcomes than standalone capacity-building programs, with **Community Energy Access** emerging as the highest-performing intervention.


### 6. Community Impact Profile
Evaluating core operational metrics across states reveals distinct regional profiles:

| State | Metric 1 | Metric 2 | Metric 3 |
| :--- | :--- | :--- | :--- |
| **Anambra** | 97.01% | 83.45% | 86.48% |
| **Delta** | 103.57% | 84.10% | 85.60% |
| **Edo** | 100.57% | 76.00% | 89.43% |
| **Enugu** | 95.74% | 80.77% | 92.00% |
| **Kwara** | 98.93% | 80.76% | 87.01% |
| **Oyo** | 102.04% | 79.13% | 84.83% |
| **Rivers** | 102.12% | 87.30% | 84.00% |

* **Business Implication:** Operational success varies by region, with no single state leading across every measure. Management strategies should account for state-specific context rather than applying a standardized approach across all regions.


## Final Stakeholder Recommendations

1. **Prioritize Underperforming States:** I would prioritize operational support and resource allocation toward Ogun, Lagos, Kwara, and Enugu to address their beneficiary target shortfalls.
2. **Address Last-Mile Access Deficits:** I would focus program efforts on resolving last-mile connection issues to narrow the gap between registered beneficiaries and actual operational clean-energy access.
3. **Connect Training to Employment Opportunities:** I would strengthen post-training job placement by linking trainees directly with local installers, equipment suppliers, contractors, and project implementation teams.
4. **Target Technical Reliability Improvements:** I would focus technical support on regions reporting low community satisfaction to ensure system reliability issues are promptly addressed.
5. **Scale High-Performing Interventions:** I would recommend expanding investment in top-scoring intervention models, specifically **Community Energy Access**, **Solar Backup Systems**, and **Solar Water Pumps**.
6. **Adopt State-Specific Management Strategies:** I would tailor program interventions to fit each state's distinct performance profile rather than enforcing a uniform strategy across all regions.
7. **Establish a Monthly Operational Review:** I would introduce a monthly impact review tracking target achievement, actual access gaps, system reliability, community satisfaction, and job creation.

## Business Value
This project demonstrates the ability to translate operational dataset records into practical management insights:
* **Performance Monitoring:** Translates raw operational logs into clear executive metrics.
* **Target Accountability:** Highlights underperforming geographic regions and intervention types.
* **Resource Allocation:** Provides objective data to support budget and operational shifts.
* **Decision Support:** Connects program metrics (such as reliability and training) to real-world community outcomes.


## Limitations
* **Simulated Data:** Analysis is based on a mock/simulated dataset and should be validated against actual field logs before driving live operational changes.
* **Correlation vs. Causation:** Observed patterns (e.g., between reliability and satisfaction) indicate relationships rather than direct cause-and-effect.
* **Post-Training Context:** The dataset lacks detailed long-term tracking on post-training employment retention and income levels.
* **Timeframe Boundaries:** Limited longitudinal data prevents long-term trend analysis over extended multi-year periods.

## Future Scope
* **Automated Dashboarding:** Migrating static reporting into an automated Power BI dashboard with live data refreshes.
* **Beneficiary-Level Tracking:** Developing unique beneficiary IDs to track last-mile adoption journeys in detail.
* **Longitudinal Impact Evaluation:** Tracking long-term employment rates and economic outcomes 6–12 months post-intervention.
* **Predictive Performance Modeling:** Applying machine learning models to forecast state-level target shortfalls based on early operational indicators.


## Repository Structure

```text
project-name/
│
├── data/
│   └── dataset.csv
│
├── dashboard/
│   └── dashboard.xlsx
│
├── sql/
│   └── analysis.sql
│
├── screenshots/
│   └── dashboard.png
│
├── README.md
└── LICENSE
