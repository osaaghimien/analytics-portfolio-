# Hospital Readmission Analytics

## Business Problem
Hospitals across the United States continue to experience **high 30-day all-cause readmission rates**, averaging approximately **14.7%**, meaning nearly one in seven patients is readmitted shortly after discharge. These readmissions drive **significant healthcare costs**, strain hospital resources, and expose patients to **avoidable complications and patient stress**.

The core challenge is the inability to **reliably identify high-risk patients at the point of discharge** using existing operational and clinical data. Without early risk identification, hospitals struggle to **deploy targeted transitional care interventions effectively**.

This project addresses that gap by leveraging **routinely collected demographic and clinical data** to surface patients at **elevated risk of readmission**, enabling **earlier intervention and more informed discharge planning**.

## Business Objective
The objective of this project is to support hospitals in **reducing avoidable 30-day readmissions** by identifying patients who are at **elevated risk of readmission at the time of discharge**.

Using **routinely collected demographic and clinical data**, the analysis aims to generate a reliable **readmission risk signal** that can inform **discharge planning and post-discharge care decisions**. The goal is not only predictive accuracy, but **operational usefulness** — enabling care teams to prioritize high-risk patients for targeted interventions such as follow-up appointments, care coordination, or transitional support.

Success is measured by the model’s ability to **differentiate high-risk and low-risk patients** in a way that is **interpretable, actionable, and scalable** within a hospital analytics environment.

## Dataset Overview
The dataset used in this project contains **de-identified hospital encounter data** representing patient demographics, clinical conditions, utilization history, and discharge outcomes. Each record corresponds to a patient hospitalization and includes an indicator of whether the patient was readmitted within **30 days of discharge**.

Key data elements include **demographic attributes**, **clinical characteristics**, and **encounter-level information** relevant to discharge outcomes. All data fields reflect information that would typically be available to hospitals **during or shortly before the discharge process**.

This dataset is well-suited for readmission risk analysis because it mirrors the type of **routinely collected operational and clinical data** hospitals rely on for population health management and quality improvement initiatives.

## KPIs & Metrics
The following **Key Performance Indicators (KPIs)** are used to evaluate hospital performance related to **30-day readmissions**, **operational efficiency**, and the **financial impact of readmissions**.

- **30-Day Readmission Rate (%)**  
  The percentage of patients readmitted within 30 days of discharge, used as the primary indicator of care effectiveness and discharge quality.

- **Average Cost per Readmission**  
  The mean billing amount associated with readmitted patients, highlighting the financial burden of preventable readmissions.

- **Average Length of Stay (LOS)**  
  The average number of days patients remain hospitalized, used to assess operational efficiency and resource utilization.

- **High-Risk Patient Percentage**  
  The proportion of patients identified as high risk for readmission based on predictive indicators or clinical risk factors.

- **Total Patients Admitted**  
  The total number of patient admissions within the reporting period, used as a baseline for trend and volume comparisons.

- **Year-over-Year (YoY) Change Metrics**  
  Year-over-year deltas and directional indicators used to track changes in readmission rate, readmission costs, and high-risk patient share over time.
  
## Data Modeling Approach
The data model was designed to support reliable KPI calculation, flexible slicing, and scalable reporting within Power BI. A structured analytical model was created to separate **patient attributes**, **encounter details**, and **readmission outcomes**, ensuring clarity and consistency across metrics.

Core tables were organized around patient encounters, with supporting dimension-style attributes used for demographic, clinical, and time-based analysis. This approach enables consistent calculation of readmission rates, length of stay, cost metrics, and high-risk patient indicators across different views and reporting periods.

The model was optimized for analytical performance by applying clean relationships, standardized keys, and reusable calculations, allowing the dashboard to support trend analysis, year-over-year comparisons, and executive-level summaries without metric duplication.

## Analysis & Methodology
The analysis focused on identifying patterns and drivers associated with 30-day hospital readmissions using a combination of descriptive analytics, risk segmentation, and trend analysis. Patient encounters were evaluated across demographic, clinical, and utilization dimensions to understand how different factors contribute to readmission outcomes.

Data preparation included standardizing encounter records, validating admission and discharge timelines, and ensuring consistency across cost, length of stay, and readmission indicators. Metrics were analyzed at both the aggregate and segmented levels to surface meaningful differences across patient groups.

Risk stratification techniques were applied to classify patients into high-risk and low-risk categories based on observed characteristics and historical outcomes. Trend and year-over-year analyses were then used to evaluate changes in readmission rates, costs, and high-risk patient proportions over time, supporting operational and performance-based insights.
## Key Insights

The analysis surfaced actionable readmission patterns across demographic, geographic, and payer segments. Insights were organized into targeted business cases to evaluate risk concentration, cost exposure, and return on intervention.

---

### Case 1 – Targeted Readmission Reduction in Younger Populations

**Objective:**  
Reduce excessive readmission costs among young adults in high-risk states while scaling effective care models observed in low-risk populations.

**Positive Insight:**  
African American patients insured by **Aetna** exhibit a **30-day readmission rate of 6.0%**, compared to the overall system average of **10.3%**, representing a **42% reduction**. This suggests that payer-specific care coordination or benefit structures may be contributing to improved post-discharge outcomes within this demographic.
<img width="1320" height="643" alt="image" src="https://github.com/user-attachments/assets/a8c6088b-0764-4083-8a00-706075a6f82d" />


**Negative Insight:**  
Patients aged **20–39 in Oklahoma** show the **highest 30-day readmission rate at 34.8%**, which is **238% higher than the system average**. This group also incurs an **average cost per readmission of $25,000**, approximately **20% higher** than the typical $21,000 per readmission.
<img width="1072" height="621" alt="image" src="https://github.com/user-attachments/assets/f07f1569-da53-4e8b-ab46-358fc439c0bc" />

**ROI Opportunity:**  
Reducing the 34.8% readmission rate among Oklahoma patients aged 20–39 to the system average of 10.3% would prevent approximately **24.5 unnecessary readmissions per 100 patients**. At **$25,000 per readmission**, this represents **$612,500 in potential annual savings**.  
If care models similar to those observed in the African American Aetna population were adopted, total savings could exceed **$700,000**, yielding an estimated **ROI of 280%**, assuming a **$250,000 intervention cost**.

---

### Case 2 – Risk Containment in Aging Populations

**Objective:**  
Reduce future readmission costs and high-risk exposure among aging populations while maintaining recovery efficiency.

**Positive Insight:**  
Patients aged **60–79 in Michigan** demonstrate a **30-day readmission rate of 8.8%**, representing an **18.8% decrease** compared to the previous period and well below the system average of 10.3%. This indicates that existing care plans for this population are producing positive outcomes.
<img width="1065" height="652" alt="image" src="https://github.com/user-attachments/assets/aac4fdef-0b2e-464e-b72a-3e1ab0a05781" />

**Negative Insight:**  
Despite favorable readmission performance, **55.6% of patients aged 60–79 in Michigan are classified as high risk**, reflecting a **1.8% increase**. This elevated risk concentration poses a threat to sustaining current performance and could drive future cost increases if left unaddressed.
<img width="1320" height="655" alt="image" src="https://github.com/user-attachments/assets/91d072ab-90b7-4f58-9c87-9bae2b4c6fbd" />

**ROI Opportunity:**  
Reducing the high-risk population by **10%** within this age group could lower projected future readmission costs by approximately **$260,000**, based on an average cost of **$26,000 per readmission per 100 patients**. With a projected **$30,000 investment** in predictive monitoring and follow-up care, this scenario yields an estimated **ROI of 766%**.

## Dashboard Overview
The Power BI dashboard provides an interactive view of 30-day hospital readmissions, patient risk distribution, and associated cost exposure. It is designed to support both **executive-level monitoring** and **operational analysis** by translating complex clinical and utilization data into clear, actionable visuals.

The dashboard includes **KPI cards** summarizing readmission rates, high-risk patient share, average cost per readmission, and length of stay. **Trend visuals** and **stacked column charts** enable comparison across time, demographics, payers, and geographic segments, while **scatter plots and heatmaps** highlight risk and cost concentration across patient groups.

Interactive **slicers** allow users to dynamically filter results by age group, insurance type, location, and reporting period. A dedicated **business case comparison view** supports ROI-driven decision-making by allowing stakeholders to evaluate the potential financial impact of targeted interventions across high-risk populations.

<img width="946" height="552" alt="Final Readmission Dashboard" src="https://github.com/user-attachments/assets/6a62ce5a-88ab-4292-a9b7-c960cc49fff1" />

## Files Included
- **Power BI Report (.pbix)** – Interactive dashboard containing readmission KPIs, risk segmentation, trend analysis, and ROI scenarios.
- **Dataset (CSV / SQL Extract)** – De-identified patient encounter data used for readmission analysis and KPI calculation.
- **Project Documentation** – Supporting notes outlining business objectives, assumptions, and analytical approach.
- **Dashboard Screenshots** – Static images highlighting key views and insights from the Power BI report.

