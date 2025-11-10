# Fabric Medallion Logistics Pipeline

## 1. Overview

**Fabric Medallion Logistics Pipeline** is an **End-to-End Data Lakehouse Solution** built on **Microsoft Fabric**, simulating the analytical workflow of a logistics enterprise.  
The project focuses on designing a **Medallion data architecture (Bronze–Silver–Gold)**, developing **data transformation pipelines using PySpark**, and building **Power BI dashboards** to perform **Root Cause Analysis (RCA)** on **Delivery Performance** metrics.

---

## 2. Data Privacy & Simulation Notice

This project was developed for academic purposes using a **Microsoft Fabric student license**.  
Due to data privacy and license restrictions, several components are simulated or anonymized.

### 2.1. Data Source
- The dataset used is **synthetic**, modeled after the operational structure of a logistics company (e.g., *Ahamove*).  
- The **Raw Data** is not publicly shared to ensure compliance with data protection and intellectual property policies.

### 2.2. Substitute Documentation
In place of raw datasets, detailed schema structures and transformation logic are documented in:

```
docs/02_Fabric_Data_Pipeline_Design_Specs.pdf
docs/03_Data_Preparation_and_EDA_Insights.pdf
```

### 2.3. Fabric Workspace Access
The ETL pipelines and Power BI dashboards were deployed within a restricted **Microsoft Fabric Education Tenant**.  
External access cannot be granted.  

**Alternative Access:** The final **Power BI (.pbix)** file is provided via Google Drive (see below).

---

## 3. Data Engineering Architecture

### 3.1. Platform & Design Overview

| Aspect | Implemented Technique | Demonstrated DE Skill |
|---------|----------------------|------------------------|
| Platform | Microsoft Fabric (OneLake) | Implemented a unified Lakehouse architecture |
| Data Model | Medallion Architecture (Bronze–Silver–Gold) | Used Delta Parquet format ensuring ACID compliance |
| Data Modeling | Snowflake Schema | Designed one Fact Table and eight Dimension Tables with City → District hierarchy |
| Historical Data | SCD Type 2 | Applied to 6/8 Dimension Tables to preserve historical attribute changes |
| BI Access | Direct Lake Mode (Power BI) | Connected Power BI directly to the Gold Layer for near real-time performance |

---

## 4. Pipeline Implementation

### 4.1. Notebook Structure

| Notebook | Processing Objective |
|-----------|----------------------|
| NB_Bronze_to_Silver.ipynb | Data Cleansing (Bronze → Silver) |
| NB_Silver_to_Gold.ipynb | Dimensional Modeling (Silver → Gold) | 

### 4.2. Data Quality & EDA Insights

Detailed preprocessing logic is provided in: docs/03_Data_Preparation_and_EDA_Insights.pdf
---

## 5. Business Analytics & Deliverables

| File / Directory | Description |
|------------------|-------------|
| `docs/01_Strategic_Operational_RootCause_Report.pdf` | *Design and Implementation of a Data-Driven BI Framework* — presents the full workflow from Data Warehouse to BI Dashboard, performing **Root Cause Analysis (RCA)** with **5 Whys** and a **Fishbone Diagram**. |
| `docs/02_Fabric_Data_Pipeline_Design_Specs.pdf` | Technical documentation detailing **Medallion Architecture**, **Snowflake Schema**, **SCD Type 2** logic, and **pipeline orchestration** in Microsoft Fabric. Serves as the primary **Data Engineering (DE)** evidence. |
| `docs/03_Data_Preparation_and_EDA_Insights.pdf` | *Data Preparation & Exploratory Data Analysis (EDA)* — documents the preprocessing and analytical exploration prior to Lakehouse integration, including:<br>• Data Profiling & Consistency Checks<br>• Missing Value & Outlier Handling<br>• Feature Standardization & Data Dictionary<br>• EDA Visual Insights supporting Delivery Performance analysis. |
| `Power BI (.pbix)` | Final interactive dashboard visualizing key logistics KPIs, data model, and validated DAX measures. |

**Download Power BI (.pbix):** [Download via Google Drive](https://drive.google.com/file/d/1PXxWqyPSE5NYQwd1d6QTRpJUi3OiFvoA/view?usp=sharing)

---

## 6. Key Learning Outcomes

- Mastered the full **Bronze → Silver → Gold pipeline** within **Microsoft Fabric (OneLake)**.  
- Implemented **SCD Type 2**, **Surrogate Key Generation**, **Direct Lake Mode**, and **Delta Parquet ACID transactions**.
- Designed a **Power BI** dashboard emphasizing **data visibility, user interactivity, and KPI interpretability**, aligning visual design with business objectives.
- Gained a deep understanding of the synergy between **Data Engineering**, **Business Intelligence**, and **Analytical Decision-Making** in logistics.  
- Applied **Root Cause Analysis (RCA)** to connect operational data insights with strategic business improvements.

---

## 7. Repository Structure

```
Fabric-Medallion-Logistics-Pipeline/
│
├── docs/
│   ├── 01_Strategic_Operational_RootCause_Report.pdf
│   ├── 02_Fabric_Data_Pipeline_Design_Specs.pdf
│   └── 03_Data_Preparation_and_EDA_Insights.pdf
│
├── notebooks/
│   ├── NB_Bronze_to_Silver.ipynb
│   └── NB_Silver_to_Gold.ipynb
│
├── PowerBI/
│   └── Logistics_Performance_Dashboard.pbix
│
└── README.md
```

---

## 8. Acknowledgement

This project was developed as part of the **Data Visualization** course at the **University of Economics and Law (UEL)**.  
I expresses sincere gratitude to the instructors who provided guidance and the academic environment necessary to experiment with **Microsoft Fabric** for end-to-end analytics implementation.
