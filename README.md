# Data Analytics & BI Portfolio

## Sergey Koverzen

**Data Analyst / BI Analyst → Analytics Engineering**

I build analytical solutions that connect **business understanding, SQL, Python, data modelling and BI**.

My background in financial accounting gives me strong domain knowledge in financial data, reporting and business processes. I am now developing this experience toward a more technical analytics role, with a focus on **data pipelines, analytical modelling and Analytics Engineering**.

---

## Career Direction

```text
Financial Accounting
        ↓
Business & Financial Analysis
        ↓
BI / Data Analytics
        ↓
Analytics Engineering
        ↓
Data Engineering
```

My current focus is not only on building dashboards.

I am increasingly working on the layers behind the dashboard:

```text
Raw Data
   ↓
Ingestion
   ↓
Cleaning & Validation
   ↓
Data Modelling
   ↓
SQL Transformation
   ↓
KPI / Analytics Layer
   ↓
BI / Reporting
```

---

# Featured Projects

# 01 — Financial BI Analysis

### Apple · Microsoft · Amazon

**`Real SEC data` | `Python` | `PostgreSQL` | `SQL` | `Power BI`**

**Repository:**  

[Financial BI Analysis](https://github.com/SergeyKoverzen/financial-bi-analysis)

An end-to-end financial analytics pipeline built using real SEC EDGAR Company Facts data.

The project demonstrates the complete workflow from external API data to a BI-ready analytical layer.

### Architecture

```text
SEC EDGAR API
     ↓
Python ingestion
     ↓
Data validation
     ↓
Standardized datasets
     ↓
PostgreSQL
     ↓
SQL analytical layer
     ↓
KPI layer
     ↓
Power BI
```

### Technical focus

- Python API ingestion
- Pandas data transformation
- PostgreSQL
- SQL data modelling
- analytical views
- KPI calculations
- data validation
- Power BI
- DAX
- real-world XBRL data handling

### Why this project matters

The project goes beyond dashboard creation.

It demonstrates how raw external data can be transformed into a structured analytical model that can be consumed by BI tools.

**Key technologies:**

`Python` `Pandas` `PostgreSQL` `SQL` `Power BI` `DAX` `Git`

---

# 02 — DEX Analytics

### Web3 / DeFi Analytics

**`SQL` | `Dune` | `On-chain Data` | `KPI Analysis`**

📄 [Download PROJECT №1 "DEX Analytics Build Process" as PDF](docs/DEX_Analytics_Build_Process_01092026.pdf)

📄 [Download PROJECT №1 "Dashboard of Trader Behavior"as PDF](docs/Top_Trades.pdf)

**Pipeline: Dune Analytics (SQL) → PostgreSQL (staging table + SQL views) → Power BI (3-page dashboard)**

A blockchain analytics project focused on decentralized exchange activity and user behaviour.

The analysis explores:

- trading activity
- transaction volume
- user behaviour
- protocol performance
- time-based trends
- key Web3 KPIs

The project demonstrates the ability to work with large, event-oriented datasets and translate blockchain activity into business-style analytical metrics.

**Key technologies:**

`SQL` `Dune Analytics` `Blockchain Data` `Web3 Analytics`

---

# 03 — Ethereum Staking Analytics

### St_ETH / Ethereum

**`SQL` | `Blockchain Analytics` | `Financial KPIs`**

📄 [Download PROJECT №2 "Ethereum Staking Behavior Build Process" as PDF](docs/Ethereum_Staking_Behavior_Analysis_Build_Process.pdf)

📄 [Download PROJECT №2 "Dashboard Ethereum Staking Behavior Analysis"as PDF](docs/Ethereum_Staking_Behavior_Analysis.pdf)

**Pipeline: Dune Analytics (SQL) → PostgreSQL (staging table + SQL views) → Power BI (5-page dashboard)**

An analytical project focused on Ethereum staking activity and liquid staking data.

The project explores:

- staking activity
- token balances
- user behaviour
- protocol metrics
- financial and operational KPIs
- time-series trends

The project demonstrates analytical thinking in a financial technology and blockchain environment.

**Key technologies:**

`SQL` `Dune Analytics` `Ethereum` `DeFi`

---

# 04 — iGaming Analytics

### Product & Financial Analytics

**`SQL` | `Power BI` | `Python` | `KPI Analysis`**


### The process in short

Each step has its own page with a detailed diagram and notes — see the **Details** column.

| Step | What happens | Output | Details |
|---|---|---|---|
| **1. Goals & metrics** | Align with product/marketing on the question being answered; lock the KPI set, segments and comparison period | Defined KPI list, W/W period | [Open →](docs/01-goals-and-metrics.md) |
| **2. Data collection** | SQL extracts from the DWH (players, sessions, bets, deposits/withdrawals, bonuses) + marketing data from GA/GTM and affiliate reports | Raw datasets | [Open →](docs/02-data-collection.md) |
| **3. Cleaning & validation** | Deduplication, test-account exclusion, outlier handling, reconciliation against the finance report | Trusted dataset | [Open →](docs/03-cleaning-and-validation.md) |
| **4. Analysis** | Cohorts by registration date, player segmentation, funnel breakdown, week-over-week comparison, root-cause of deviations | Findings | [Open →](docs/04-analysis.md) |
| **5. Visualisation** | Build/refresh the Power BI dashboard: DAX measures, geo & channel slicers, drill-down to segment | Dashboard | [Open →](docs/05-visualisation.md) |
| **6. Conclusions** | What went up, what went down, why, and what to do next | Summary + 3–5 recommendations | [Open →](docs/06-conclusions.md) |


An analytical workflow focused on product and financial performance in an iGaming environment.

Key analytical areas include:

- Revenue
- GGR / NGR
- Deposits and withdrawals
- Conversion
- Retention
- Churn
- LTV
- Cohort analysis
- Product KPIs

The project demonstrates the ability to translate business questions into measurable analytical metrics.

**Key technologies:**

`SQL` `Power BI` `Python` `Pandas` `Cohort Analysis`

---

# 05 — DeFi Analytics Data Platform (Medallion Architecture)

### Web3 / DeFi Analytics Engineering  

**`Python` | `Google BigQuery` | `dbt` | `SQL` | `Looker Studio` | `Medallion Architecture`**

**Repository:** [DeFi Analytics Data Platform](https://github.com/SergeyKoverzen/defi-analytics-dbt-bigquery)  

![Dashboard Preview](docs/TVL_Dashboard.pdf)   -AND-   **Live Interactive Dashboard:** [📊 Looker Studio Report](https://datastudio.google.com/s/s_BfMsyFwoo)

An end-to-end Analytics Engineering pipeline that ingests raw DeFi market protocol data, cleans and transforms it through a **Medallion Architecture (Bronze → Silver → Gold)**, and serves business-ready data marts to Looker Studio.

#### Pipeline Architecture

```
[ External DeFi API ]
         │
         ▼ (Initial Prototyping & Staging on Databricks / Power BI Ready)
[ Databricks / PySpark Environment ]
         │
         ▼ (Python Ingestion Script to Production DWH)
[ BigQuery: Bronze Layer ]  ──>  `bronze_protocols_raw` (Raw JSON Payload)
         │
         ▼ (dbt Models: JSON Parsing & Deduplication)
[ BigQuery: Silver Layer ]  ──>  `stg_protocols` (Cleaned & Structured SQL Views)
         │
         ▼ (dbt Models: Aggregations & Data Marts)
[ BigQuery: Gold Layer ]    ──>  `mart_protocols_summary` (Materialized Data Mart)
         │
         ▼ (BI Integration)
[ Looker Studio / Power BI ] ──> Interactive Executive Dashboards ($570B+ TVL Analyzed)
```

#### Technical Focus & Analytics Engineering Features
- **Medallion Architecture:** Multi-layer ELT pipeline designed for scalable data processing.
- **Data Ingestion & Extraction:** Automated Python script fetching raw protocol data into BigQuery Bronze layer.
- **JSON Parsing & Cleaning:** Extracted nested JSON attributes (`JSON_VALUE`) in dbt Silver layer.
- **Data Quality & Deduplication:** Applied SQL Window Functions (`ROW_NUMBER() OVER (PARTITION BY ... ORDER BY ...)`) to remove redundant API snapshots.
- **Analytical Data Marts:** dbt Gold models aggregating Total Value Locked (TVL), protocol counts, and chain/category distributions.
- **BI Layer:** Interactive Looker Studio dashboard featuring market concentration and sector breakdowns ($570B+ TVL analyzed).

#### Key Technologies:
`Python` `Google BigQuery` `dbt` `SQL` `Looker Studio` `Medallion Architecture` `Data Modelling`


# Technical Skills

## Analytics Engineering

dbt (data build tool) — data transformation, staging, materialization models

Medallion Architecture (Bronze, Silver, Gold layers)

Data Quality & Deduplication (SQL Window Functions)

ELT / ETL pipeline design

Cloud Data Warehousing (Google BigQuery)

Unified Data Analytics Platforms (Databricks, PySpark)

## Data Analytics & Querying

SQL & Advanced SQL (CTEs, Window Functions, JSON parsing, aggregation logic)

KPI analysis & Business metrics definition

Cohort analysis & Time-series analysis

Financial & Product analytics

## BI & Visualization

Power BI & DAX

Google Looker Studio

Dimensional Data Modelling (Star Schema, Data Marts)

Interactive Dashboards & Business Storytelling

## Data & Scripting

Python (Pandas, Requests, Cloud Client Libraries)

REST APIs & Unstructured JSON Parsing

Data Ingestion & Cleaning

Git / GitHub Version Control

## Cloud & Databases

Google BigQuery

Databricks (PySpark / Spark SQL)

PostgreSQL

Staging layers & Analytical Views

---

# What I Am Building Toward

My goal is to move from traditional BI and Data Analysis toward **Analytics Engineering and eventually Data Engineering**.

The technical progression I am following is:

```text
SQL
 │
 ├── PostgreSQL & Cloud DWH (BigQuery)
 │
 ├── Data Modelling (Dimensional & Medallion)
 │
 ├── Python / APIs / Databricks
 │
 ├── ETL / ELT Concepts
 │
 ├── dbt (Data Transformation)
 │
 ├── Workflow Orchestration
 │
 └── Data Engineering
```

The emphasis is on building reliable data workflows rather than producing dashboards alone.

---

# Domain Experience

My analytical projects combine several areas:

### Finance

Financial accounting, reporting, financial KPIs and company performance.

### Product Analytics

Retention, conversion, LTV, churn and cohort analysis.

### Web3 / Crypto

On-chain data, DeFi protocols, DEX activity and staking.

### Business Intelligence

Power BI & Looker Studio dashboards, BigQuery + dbt data modeling, Databricks processing, and management reporting.

This combination allows me to approach data from both the business side and the technical side. **

---

# Portfolio Architecture

The projects in this portfolio demonstrate different stages of the analytical workflow:

```text
               DATA ANALYTICS
                       │
          ┌────────────┼────────────┐
          │            │            │
       Finance      Product       Web3
          │            │            │
          └────────────┼────────────┘
                       │
                  SQL / Python
                       │
        Databricks / Google BigQuery
                       │
           dbt (Analytics Engineering)
                       │
             Power BI / Looker Studio
```

The Financial BI Analysis project represents the current step toward a more engineering-oriented workflow.

---

# Tools

| Area | Tools |
|---|---|
| SQL | PostgreSQL, SQL |
| Programming | Python, Pandas |
| BI | Power BI, DAX |
| Data Sources | REST APIs, SEC EDGAR, Blockchain / Dune |
| Data Modelling | SQL analytical layers, dimensional modelling |
| Version Control | Git, GitHub |
| Analytics Engineering | dbt, ELT/ETL concepts |
| Domains | Finance, Product, Web3, iGaming |

---

# Current Focus

I am currently focusing on:

- Advanced SQL & Cloud Data Warehousing (BigQuery)

- Databricks & PySpark processing

- dbt data modeling & materialization

- Python data ingestion pipelines

- ELT Architecture & Medallion patterns

- Analytics Engineering best practices

---

# Contact

**Sergey Koverzen**

Data Analyst / BI Analyst → Analytics Engineering

- GitHub: https://github.com/SergeyKoverzen

- LinkedIn: www.linkedin.com/in/serhii-k-51680032a

- Twitter: www.x.com/koverzen

- Email: sergeykoverzen@gmail.com

---

> **I am interested in analytical roles where business understanding and technical data skills meet — especially BI, Data Analytics and Analytics Engineering.**
