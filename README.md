# superstore-analytics

<img width="1105" height="596" alt="superstore" src="https://github.com/user-attachments/assets/c362ad95-725-4cai-5-a75-4a75-1af519824a4d" />

## Project Overview
This project demonstrates a production-grade, "full-stack" data analytics pipeline built from scratch using the classic **Sample Superstore** dataset. The goal of this case study is to move beyond basic visualization and showcase an end-to-end data workflow: **Automated Data Cleaning (Python) -> Relational Storage & Querying (SQLite) -> Business Intelligence & Executive Dashboarding (Power BI via ODBC)**.

Through this analysis, we uncover critical operational inefficiencies—most notably, that high-volume product categories are severely leaking capital due to structural discounting and pricing issues.

---

## Key Business Findings & Insights
* **The Revenue vs. Profit Paradox:** While total enterprise revenue stands at **\$12.64M** with a healthy net profit of **\$1.47M** (11.6% overall profit margin), a deep dive into sub-categories revealed massive profit leakage.
* **The "Tables" Loss-Driver:** The **Tables** sub-category generated an impressive **\$757,034 in total sales**, but resulted in a staggering net loss of **-\$64,083.39**. 
* **Strategic Recommendation:** Operations and pricing strategy teams must immediately review shipping costs, heavy discounting rules, and manufacturer contracts on Furniture (specifically Tables and Bookcases) to protect bottom-line profitability.

---

## Technical Stack & Implementation Stages

### Stage 1: Business Modeling & Context (Excel / Power Pivot)
* Used Excel Power Pivot (`superstore 3.xlsx`) to build data models, establish relationships, and prototype core financial measures using **DAX** to understand baseline business logic.

### Stage 2: Automated Data Cleaning & ETL (Python / Pandas)
* Ingested the raw Kaggle CSV into a Google Colab / Python environment (`superstore.ipynb`).
* Handled data type conversions, forced numeric formatting on financial metrics (`Sales`, `Profit`), and cleaned column structures (`Sub.Category`) to ensure data integrity.

### Stage 3: Database Engineering & Querying (SQLite & SQL)
* Loaded the cleaned dataset into a local relational database (`superstore.db`).
* Used SQL queries with aggregate functions and `HAVING` clauses to isolate loss-making product lines programmatically.

### Stage 4: Executive Visualization (Power BI via ODBC)
* Established an enterprise-grade connection from **Power BI Desktop** (`superstore.pbix`) directly to the SQLite database via ODBC.
* Designed a clean, single-page executive dashboard featuring executive KPI cards, category macro views, and the loss-making sub-category highlight.

---

## Repository Files
* 🐍 **Python Cleaning Script:** `superstore.ipynb`
* 📊 **Power BI Report:** `superstore.pbix`
* 📑 **Excel Model:** `superstore 3.xlsx`
* 📂 **Cleaned Data Export:** `cleaned_superstore_data (2).csv`
