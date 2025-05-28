# 🏦 Banking Customer 360° View – Azure Data Factory Project

## 🚀 Project Overview

This project demonstrates how a modern bank can consolidate data from various operational sources to build a 360° customer profile using **Azure Data Factory (ADF)** and **Azure Data Lake**. It mimics a real-world data engineering workflow, featuring ingestion, transformation, and orchestration patterns across various ADF activities.

---

## 📊 Business Use Case

Banks collect customer data from multiple systems:

- 🧾 **Core Banking** (SQL Server)
- 📞 **Customer Support Logs** (CSV on Blob)
- 🌐 **Digital Channels** (JSON via REST API)
- 📈 **Credit Score Services** (REST API)

The goal is to build a unified gold table for **Customer 360 View**, which includes:

- Personal details  
- Account balance & transactions  
- Customer sentiment score  
- Credit score  
- Engagement level

---

## 🛠️ Tech Stack

- **Azure Data Factory**
- **Azure Data Lake Gen2**
- **Azure SQL Database**
- **REST API Integration**
- **Blob Storage**
- **Data Flows for Transformation**
- **Event Triggers, Variables, Expressions**

---

## 🧱 Architecture

1. **Raw Layer** – Data landing from multiple sources (CSV, JSON, SQL).
2. **Staging Layer** – Intermediate cleaned data.
3. **Gold Layer** – Unified customer view.

---

## 🔄 Pipeline Flow

```text
[Blob CSV] --->           |
[Azure SQL] --> [Copy Activity] --> [Staging Zone]
[REST API] -->            |

[Staging Zone] --> [Data Flow Transformation] --> [Gold Table: Customer_360]

