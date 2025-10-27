# 🧹 ERP Service Operations Data Wrangling Project

## 🧭 Project Overview

This project demonstrates advanced **data wrangling and preprocessing** using **Python** on **Google Colab**, simulating a complex ERP-style dataset inspired by real-world operations at any **Digital Solutions** corporation. 

The aim is to show how messy, inconsistent, and incomplete business data can be transformed into clean, integrated, and analysis-ready datasets through systematic data wrangling techniques.

---

## 🎯 Project Objective

The goal of this project is to **simulate, clean, and integrate multiple ERP-related datasets** to:

- Handle missing values and inconsistencies  
- Rename, merge, and join multiple datasets  
- Filter, transform, and aggregate data  
- Prepare clean, analysis-ready data  
- Visualize the transformation results (before vs. after cleaning)

By doing so, the project replicates real challenges encountered in ERP and business data analytics environments — such as project overruns, financial inconsistencies, and client support inefficiencies.

---

## 🧩 Business Context

At **Spopli**, data drives decision-making.  
The ERP team relies on structured data to:

- Monitor **project efficiency** (estimated vs actual timelines)
- Track **support ticket resolution** performance
- Analyze **financial and cost-efficiency** metrics
- Assess **employee workload** across ERP modules

However, raw ERP data often comes **messy and fragmented** across systems — requiring extensive cleaning and wrangling before insights can be extracted.

---

## ⚙️ Tools & Technologies Used

| Category | Tools / Libraries |
|-----------|-------------------|
| **Programming** | Python 3.10+ |
| **Data Wrangling & Analysis** | pandas, numpy |
| **Visualization** | matplotlib, seaborn, plotly |
| **Data Quality Auditing** | missingno |
| **Platform** | Google Colab |

---

## 🧱 Datasets Simulated

Four interrelated datasets were created to simulate a real ERP environment:

| Dataset | Description | Common Issues Simulated |
|----------|--------------|-------------------------|
| **Projects** | Project metadata with estimated vs actual duration | Missing values, duplicates, inconsistent names |
| **Support Tickets** | Client support requests and resolution times | Missing severity levels, wrong client IDs |
| **Financials** | Project costs, invoices, and payments | Inconsistent currency formats, missing costs |
| **Employees** | Staff assignments, roles, and logged hours | Missing roles, multiple project assignments |

---

## 🔍 Wrangling Workflow

### Step 1. Data Simulation
- Generated realistic but **messy** ERP datasets using `numpy` and `pandas`.  
- Introduced missing values, duplicates, inconsistent formats, and redundant rows.

### Step 2. Initial Exploration
- Inspected dataset structure and missing values using `pandas.info()` and `missingno`.

### Step 3. Data Cleaning
- Filled or dropped missing values.  
- Removed duplicates and standardized naming.  
- Converted text-based currency strings to numeric (`float`).  
- Renamed columns for clarity.

### Step 4. Merging and Integration
- Combined all datasets into a **single integrated DataFrame**.  
- Managed one-to-many relationships across Projects, Employees, Financials, and Support Tickets.

### Step 5. Feature Engineering
- Created analytical metrics:
  - `Delay_days = Actual_Duration - Est_Duration`
  - `Cost_Efficiency = Invoiced / Cost`
  - `Resolution_Efficiency = Resolution_Hours / Severity`

### Step 6. Aggregation
- Grouped by client to summarize:
  - Average project delay
  - Total support tickets
  - Total employee hours
  - Cost and invoicing efficiency

### Step 7. Visualization
- Before vs After wrangling comparisons:
  - Missing data heatmaps (`missingno`)
  - Project duration distributions
  - Cost vs Invoiced scatterplots
  - Employee workload heatmaps
  - Average project delay per client (interactive Plotly bar chart)

### Step 8. Export
- Saved both **messy** and **cleaned** versions of the datasets as CSV:
  - `Messy_Projects.csv`, `Messy_Support_Tickets.csv`, `Messy_Financials.csv`, `Messy_Employees.csv`
  - `Cleaned_ERP_Data.csv`

---

## 📈 Key Improvements (Before → After)

| Category | Before Cleaning | After Cleaning |
|-----------|-----------------|----------------|
| **Completeness** | Missing client names, inconsistent costs | Missing values imputed or labeled |
| **Consistency** | Mixed data formats | Standardized numeric + categorical formats |
| **Integration** | 4 separate sources | Unified single analytical dataset |
| **Analytical Readiness** | No derived KPIs | Created delay, cost, and efficiency metrics |
| **Visualization** | Unclear and fragmented | Clear visual storytelling via Seaborn & Plotly |

---

## 🧠 ### 🔍 Interpretation (Analyst’s Takeaways)

| Insight Type | Example Insight |
|---------------|----------------|
| **Operational** | Projects with more logged hours (e.g., Nova LLC) tend to have longer delays, indicating potential inefficiencies in resource allocation or project management. |
| **Financial** | Orion Ltd shows over-invoicing relative to cost, suggesting positive profit margins, whereas Acme Corp’s incomplete financial data could indicate underbilling or missing reconciliation. |
| **Support & Quality** | Resolution efficiency varies across clients — pointing to disparities in support processes or potential needs for targeted staff training and workload balancing. |

These takeaways mirror the types of insights an ERP analytics or operations team might extract in a real-world enterprise environment. The wrangled data not only improves analytical precision but also uncovers hidden operational and financial patterns that were obscured in the messy raw data.

---

## 🧾 Example Output Summary (Aggregated)

| Client_Name | Avg Delay (days) | Avg Cost (USD) | Avg Invoiced (USD) | Resolution Efficiency | Total Hours |
|--------------|------------------|----------------|---------------------|------------------------|--------------|
| Acme Corp | 8.0 | 60,833 | 63,333 | 4.25 | 338 |
| Nova LLC | 15.5 | 60,000 | 62,500 | 7.75 | 122 |
| Orion Ltd | 7.5 | 73,750 | 90,000 | 3.0 | 333 |

---
## 📊 Before vs After Visualization Highlights

1. **Missing Value Heatmap**
   - Visualizes data completeness improvement.
2. **Project Duration Distribution**
   - Shows cleaned distributions after imputation.
3. **Cost vs Invoiced Scatterplot**
   - Highlights financial efficiency per client.
4. **Employee Hours Heatmap**
   - Displays workload balance across roles and clients.
5. **Average Project Delay (Bar Chart)**
   - Simple business insight visualization.

---

### ✅ Summary of What the Cleaned Output Communicates

After the complete wrangling and integration workflow, the final cleaned dataset achieves the following:

- ✅ **Integrated, reliable, and analysis-ready data:** All inconsistencies and missing relationships across projects, financials, employees, and support tickets were resolved.  
- 📊 **Cross-departmental visibility:** Enables unified insight into project timelines, cost efficiency, employee workloads, and client satisfaction — a core requirement for ERP-driven performance management.  
- 🧩 **Enhanced analytical depth:** Derived KPIs (delay, cost efficiency, resolution efficiency) allow stakeholders to measure productivity, cost control, and service quality at both project and client levels.  
- 🧠 **Demonstration of data wrangling expertise:** The project exemplifies advanced cleaning, merging, transformation, and visualization techniques applied to real-world ERP-style datasets — a hallmark skill for data-driven consulting and ERP analytics roles.

---

### 🏁 Final Takeaway

This project showcases how **effective data wrangling transforms fragmented operational data into strategic business intelligence**.  
Through structured preprocessing, feature engineering, and visual storytelling, messy ERP data evolves into a clear narrative of **performance, efficiency, and decision-ready insights**.  

It demonstrates technical proficiency with Python and analytical tools and an understanding of how data quality directly impacts business strategy, particularly in **digital transformation and ERP implementation analytics**.

---



