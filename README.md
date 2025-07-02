# Healthcare Analytics - Reducing Hospital Readmissions Using Python, SQL & Tableau

**Live Dashboard:** [**View on Tableau Public**](https://public.tableau.com/views/HealthcareAnalytics-ReducingHospitalReadmissions/ReducingHospitalReadmissions?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

![image](https://github.com/user-attachments/assets/9e948843-ca4f-4524-873a-850acad60815)


---

### Introduction

This project is an end-to-end analysis designed to identify the primary factors driving unplanned 30-day hospital readmissions. Unplanned readmissions are a critical challenge in healthcare, leading to decreased quality of patient care and significant financial costs.

The objective was to move beyond simply tracking the readmission rate and instead identify *why* it happens. By analyzing patient data, key drivers of readmission were identified, allowing for the creation of a dashboard that empowers care managers to proactively identify at-risk patients and apply targeted, data-driven support. This reflects a commitment to patient-centered care, accountability, and operational excellence.

* **Tools:** Python (Pandas, Seaborn), SQL (PostgreSQL), Tableau
* **Dataset:** [Hospital Readmission Dataset from Kaggle](https://www.kaggle.com/datasets/vanpatangan/readmission-dataset)

---

### Methodology

A three-prong approach was used to move from raw data to actionable insights.

1.  **Python for Data Exploration & Preparation:**
    * Initial data loading, validation, and cleaning were performed using Pandas to ensure data quality.
    * Exploratory data analysis (EDA) was conducted with Matplotlib and Seaborn to visualize high-level trends and identify initial relationships between patient attributes and readmission outcomes.

2.  **SQL for Deep-Dive Analysis:**
    * The prepared dataset was loaded into a PostgreSQL database to perform more complex and granular analysis.
    * Advanced SQL queries, including **Common Table Expressions (CTEs)** and **Window Functions (`RANK`)**, were used to answer specific business questions, analyze multi-factor risk, and formally rank risk drivers.

3.  **Tableau for Visualization & Storytelling:**
    * The insights from both the Python and SQL analyses were used to build a final, interactive dashboard.
    * The dashboard was designed for a business audience (e.g., care managers), focusing on clarity and providing actionable information at a glance.

---

### Insights

The combined analysis revealed several key findings:

* The baseline 30-day readmission rate for this patient cohort is **18.8%**.
* **Clinical factors are the strongest predictors.** A patient's primary diagnosis, such as **Kidney Disease** (19.9% readmission rate) and **Diabetes** (19.5%), is a primary driver of risk.
* **Patient complexity matters.** For patients with a high comorbidity score (3 or more), **COPD** becomes the highest-risk diagnosis, highlighting the need for segmented analysis.
* **Post-discharge care is critical.** A patient's discharge destination is a significant factor. Those discharged to **Home Health Care** have a slightly higher readmission rate (19.35%) than those sent to a **Skilled Nursing Facility** (17.35%).

---

### Recommendations

Based on the findings, the dashboard enables care managers to form data-driven strategies. The following actions are recommended:

* **Targeted Outreach:** Focus proactive follow-up calls on patients with a primary diagnosis of **Kidney Disease** or **Diabetes**, as this cohort has the highest overall readmission rate. For patients with high comorbidity, prioritize those with **COPD**.

* **Enhanced Discharge Planning:** Implement enhanced discharge education for patients in the **71-90 age group** with a **high comorbidity score**, as they show a significantly elevated risk.

* **Partnership Review:** Review transition-of-care protocols with **Rehabilitation and Skilled Nursing Facilities**, as the data shows these are key transition points that can influence readmission rates.
