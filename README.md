# 🍔 Uber Eats Azure Data Warehouse

![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Microsoft%20Azure-blue)
![Language](https://img.shields.io/badge/Language-SQL%20%7C%20Python-orange)
![Reporting](https://img.shields.io/badge/Reporting-Power%20BI-yellow)

---

## 📌 Project Overview

An end-to-end cloud-based data warehouse solution for **Uber Eats** built on **Microsoft Azure**. The solution ingests raw CSV files into **Azure Blob Storage**, orchestrates ETL pipelines using **Azure Data Factory**, transforms data into a **Star Schema** inside **Azure SQL Database**, and visualizes insights through **Power BI dashboards**.

---

## 🏗️ Architecture

```
Raw CSV Files
      │
      ▼
Azure Blob Storage
      │
      ▼
Azure Data Factory (ETL Orchestration)
PL_Master_Orchestrator
├── PL_Child_Staging
├── PL_Child_Dimensions
├── PL_Child_DateDimension
└── PL_Child_Facts
      │
      ▼
Azure SQL Database
├── Staging Schema
├── Dimension Schema
└── Fact Schema
      │
      ▼
Power BI Dashboard
```

---

## 🛠️ Technology Stack

| Layer | Technology |
|-------|------------|
| Cloud Platform | Microsoft Azure |
| Storage | Azure Blob Storage |
| ETL Orchestration | Azure Data Factory |
| Database | Azure SQL Database |
| Data Modeling | Star Schema |
| Visualization | Power BI Desktop |
| Version Control | Git & GitHub |

---

## 📂 Repository Structure

```
uber-eats-azure-datawarehouse/
│
├── architecure/         # Architecture diagrams
├── csv files/           # Source CSV datasets
├── screenshots/         # ADF pipeline & dashboard screenshots
├── scrips/              # SQL scripts and ADF pipeline configs
│
├── README.md
├── CHANGELOG.md
└── .gitignore
```

---

## 🔄 Data Pipeline

### Source Layer
Raw CSV files uploaded to Azure Blob Storage:
- `customers_raw.csv`
- `deliveries_raw.csv`
- `order_items_raw.csv`
- `orders_raw.csv`
- `restaurants_raw.csv`
- `users_raw.csv`

### Ingestion Layer
Azure Data Factory orchestrates all ETL:
- Dynamic Lookup + ForEach ingestion
- Metadata-driven processing
- Modular & reusable pipelines

---

## 📊 Data Model — Star Schema

**Staging Schema:**
`stg_customers`, `stg_deliveries`, `stg_order_items`, `stg_orders`, `stg_restaurants`, `stg_users`

**Dimension Schema:**
`dim_customer`, `dim_restaurant`, `dim_product`, `dim_user`, `dim_date`

**Fact Schema:**
`fact_orders`, `fact_order_items`

---

## 📈 Power BI Dashboard

- Total Revenue & Orders
- Average Delivery Time
- Fast Delivery Percentage
- Monthly Sales Trends
- Orders by Restaurant
- Delivery Performance
- Top Selling Products

---

## 💡 Key Design Decisions

| Decision | Reason |
|----------|--------|
| Modular pipelines | Easier debugging & maintenance |
| Staging layer | Preserve raw source data |
| Star schema | Optimized analytical queries |
| Surrogate keys | Improved dimensional modeling |
| Dynamic ingestion | Scalable for new tables |
| Upsert dimensions | Prevent duplicates |
| Insert-only facts | Preserve historical transactions |

---

## 🚀 Future Improvements

- Incremental loading
- CI/CD pipeline deployment
- Real-time streaming ingestion
- Azure Synapse integration
- Data quality monitoring

---

## 👤 Author

**Kulani Baloyi**
Data Engineering | Microsoft Azure | Azure Data Factory | Power BI | SQL

---

*Uber Eats Azure Data Warehouse | 2026*
