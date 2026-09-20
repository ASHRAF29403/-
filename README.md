<div align="center">

# 🏦 Banking Risk Analytics

### Credit Risk & Banking Portfolio Analysis

<p>
  <strong>End-to-End Data Analytics Project</strong>
</p>

<p>
  <a href="#-project-overview">Overview</a> •
  <a href="#-dataset">Dataset</a> •
  <a href="#-workflow">Workflow</a> •
  <a href="#-key-insights">Insights</a> •
  <a href="#-dashboard">Dashboard</a> •
  <a href="#-project-structure">Structure</a>
</p>

<br>

<img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black">
<img src="https://img.shields.io/badge/Pandas-Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white">

<br><br>

<img src="images/dashboard-preview.png" alt="Banking Risk Analytics Dashboard" width="900">

</div>

---

# 📌 Project Overview

**Banking Risk Analytics** is an end-to-end data analytics project designed to analyze customer financial behavior, credit exposure, loans, deposits, and banking relationships.

The project processes data for **3,000 banking customers** and transforms raw customer information into meaningful business insights through:

- 🐍 Python
- 🗄️ MySQL
- 📊 Power BI
- 📐 DAX
- 🎨 Data Visualization

The main objective is to help financial institutions better understand their customer portfolio, identify financial patterns, and monitor credit and deposit exposure.

---

# 🎯 Business Objectives

The project focuses on answering important banking business questions:

| Business Question | Analysis |
|---|---|
| 💳 How do customers use credit cards? | Credit Card Analysis |
| 💰 How large is the loan portfolio? | Loan Exposure Analysis |
| 🏦 How large is the deposit portfolio? | Deposit Analysis |
| 👥 Which customer segments hold more assets? | Customer Segmentation |
| 📈 How are financial variables distributed? | Statistical Analysis |
| 🔗 Which financial variables are correlated? | Correlation Analysis |
| ⚠️ Which customers have higher financial exposure? | Risk Analysis |
| 🏢 Which banking relationships dominate the portfolio? | Banking Relationship Analysis |

---

# 📊 Dataset

The dataset contains:

<div align="center">

| Metric | Value |
|---|---:|
| 👥 Customers | **3,000** |
| 📋 Columns | **25** |
| 💰 Loan Portfolio | **≈ 4.38B** |
| 🏦 Deposit Portfolio | **≈ 3.77B** |

</div>

### Main Data Categories

**Customer Information**

- Age
- Location
- Nationality
- Occupation
- Gender
- Joined Bank Date

**Banking Relationship**

- Relationship Type
- Fee Structure
- Investment Advisor
- Banking Relationship ID

**Financial Information**

- Estimated Income
- Superannuation Savings
- Bank Loans
- Business Lending
- Credit Card Balance
- Bank Deposits

**Bank Accounts**

- Checking Accounts
- Savings Accounts
- Foreign Currency Accounts
- Properties Owned

---

# 🛠️ Tech Stack

<div align="center">

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Data Cleaning & Exploratory Data Analysis |
| 🐼 **Pandas** | Data Manipulation |
| 📊 **Matplotlib / Seaborn** | Data Visualization |
| 🗄️ **MySQL** | Database Storage & SQL Analysis |
| 📈 **Power BI** | Interactive Dashboard |
| 📐 **DAX** | KPI & Business Metrics |
| 🎨 **Canva** | Dashboard UI Design |

</div>

---

# 🔄 Project Workflow

<div align="center">

```text
              ┌─────────────────────┐
              │   Raw Data          │
              │   CSV / Excel       │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │       MySQL         │
              │   Data Storage      │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │       Python        │
              │  Cleaning + EDA     │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │ Feature Engineering │
              │ Customer Segments    │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │      Power BI       │
              │ Data Model + DAX    │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │ Interactive         │
              │ Banking Dashboard   │
              └─────────────────────┘
