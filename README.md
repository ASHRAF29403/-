<div align="center">

# 🏦 Banking Risk Analytics & Portfolio Dashboard

### Python • MySQL • Power BI • Credit Risk Analysis

<p>
  <strong>End-to-End Banking Risk Analytics & Interactive Dashboard Project</strong>
</p>

<p>
  <a href="#-problem-statement--objective">Overview</a> •
  <a href="#-dataset-overview">Dataset</a> •
  <a href="#-methodology--workflow">Workflow</a> •
  <a href="#-key-insights--findings">Insights</a> •
  <a href="#-dax-measures">DAX</a>
</p>

<br>

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![MySQL](https://img.shields.io/badge/MySQL-Database-orange?logo=mysql)](https://www.mysql.com/)
[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-yellow?logo=powerbi)](https://powerbi.microsoft.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen)]()

<br><br>

<img src="images/dashboard-preview.png" alt="Banking Dashboard Preview" width="900">

<br>

<em>Preview of the main page of the interactive Power BI dashboard</em>

</div>

A comprehensive data analytics project to assess credit risk and analyze the loan and deposit portfolio for **3,000 banking customers**, aimed at helping financial institutions make informed lending decisions and reduce default risk.

> 📝 Replace the image above with a real screenshot of your dashboard — place it inside the `images/` folder as `dashboard-preview.png`.

---

# 📋 Table of Contents

- [🎯 Problem Statement & Objective](#-problem-statement--objective)
- [📊 Dataset Overview](#-dataset-overview)
- [🛠️ Tech Stack](#️-tech-stack)
- [🔄 Methodology & Workflow](#-methodology--workflow)
- [🧠 SQL & Python Techniques](#-sql--python-techniques)
- [📐 DAX Measures](#-dax-measures)
- [💡 Key Insights & Findings](#-key-insights--findings)
- [🧩 Skills Demonstrated](#-skills-demonstrated)
- [📁 Project Structure](#-project-structure)
- [⚙️ How to Run / Installation](#️-how-to-run--installation)
- [🚀 Future Improvements](#-future-improvements)
- [✉️ Contact / Author](#️-contact--author)

---

# 🎯 Problem Statement & Objective

Banks and financial institutions face the risk of loan default from certain customer segments, leading to accumulated financial losses. This project aims to:

- 🔍 **Credit Risk Analysis**: Provide insights into borrowing and deposit behavior across different customer segments (high, medium, and low income).
- 📉 **Default Risk Reduction**: Help bank management detect high-risk patterns and behaviors to reduce losses during loan approval.
- 📊 **Interactive Dashboard**: Deliver key performance indicators (KPIs) for various management levels to monitor the loan and deposit portfolio in real time.

---

# 📊 Dataset Overview

<div align="center">

| Metric | Value |
|---|---:|
| 📦 Records | **3,000 customers** |
| 📐 Columns | **25 columns** |
| 🌍 Data Type | **Financial & Demographic** |

</div>

### Key Columns

```text
✓ Customer Info       → Age (17–85), Location, Nationality, Occupation, Joined Bank Date
✓ Banking Relationship → Retail / Institutional / Private Bank / Commercial, Investment Advisor, Fee Structure
✓ Credit & Financial Data → Estimated Income, Superannuation Savings, Number of Credit Cards, CIBIL Rating, Properties Owned
✓ Accounts & Loans     → Bank Loans, Business Lending, Credit Card Balance, Bank Deposits, Checking/Savings Accounts, Foreign Currency Accounts
```

> ⚠️ **Note**: The data used in this project is a simulated/educational dataset for analysis and training purposes, and does not represent real customer data.

---

# 🛠️ Tech Stack

<div align="center">

| Technology | Purpose |
|---|---|
| 🐍 **Python 3.x** (pandas, matplotlib, seaborn) | Exploratory Data Analysis (EDA) and feature engineering |
| 🗄️ **MySQL** | Data storage and querying |
| 📊 **Power BI Desktop** (Power Query, DAX) | Data modeling and building the interactive dashboard |
| 🎨 **Canva** | Designing dashboard backgrounds and structural layouts |
| 🔗 **PyMySQL / mysql-connector-python** | Programmatic connection between Python and MySQL |

</div>

---

# 🔄 Methodology & Workflow

<div align="center">

```text
                  ┌─────────────────────────┐
                  │   Data Ingestion        │
                  │   Excel / CSV           │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   MySQL Database        │
                  │   (banking_case)        │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Python EDA            │
                  │   pandas / seaborn      │
                  │   pd.read_sql           │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │  Feature Engineering    │
                  │  Income Bands (pd.cut)  │
                  │  High / Mid / Low       │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │    Canva Design         │
                  │    UI Sketches          │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Power BI Dashboard    │
                  │   5 Pages               │
                  └─────────────────────────┘
```

</div>

### Step-by-Step Workflow

1. **Data Ingestion & Database Setup**: Converted the data to CSV and imported it into a MySQL database named `banking_case`.
2. **Connection & Exploratory Data Analysis (EDA)**: Connected Python to MySQL via `pd.read_sql`, and performed univariate and multivariate analysis.
3. **Feature Engineering**: Segmented estimated income into bands (`High`, `Mid`, `Low`) using `pd.cut`, and converted numeric IDs into text labels.
4. **Design & Planning**: Sketched UI layouts and designed Canva backgrounds to build 5 pages (Home, Loans, Deposits, Summary, Q&A).
5. **Dashboard Development**: Connected Power BI to the database, enabled page navigation, and authored DAX measures.

---

# 🧠 SQL & Python Techniques

## 1️⃣ SQL — Database Setup

```sql
CREATE DATABASE banking_case;
USE banking_case;

CREATE TABLE customer (
    customer_id        INT PRIMARY KEY,
    age                INT,
    location            VARCHAR(100),
    nationality         VARCHAR(100),
    occupation          VARCHAR(100),
    joined_bank         DATE,
    banking_relationship VARCHAR(50),
    estimated_income    DECIMAL(15,2),
    superannuation_savings DECIMAL(15,2),
    credit_card_balance DECIMAL(15,2),
    bank_loans          DECIMAL(15,2),
    business_lending    DECIMAL(15,2),
    bank_deposits       DECIMAL(15,2),
    checking_account    DECIMAL(15,2),
    savings_account     DECIMAL(15,2),
    foreign_currency_account DECIMAL(15,2),
    properties_owned    INT,
    cibil_rating         VARCHAR(10)
);
```

## 2️⃣ SQL — Portfolio KPIs

```sql
SELECT
    SUM(bank_loans + business_lending + credit_card_balance) AS total_loan_portfolio,
    SUM(bank_deposits + savings_account + checking_account + foreign_currency_account)
        AS total_deposit_portfolio
FROM customer;
```

## 3️⃣ SQL — Segmentation by Banking Relationship

```sql
SELECT
    banking_relationship,
    COUNT(*) AS total_customers,
    AVG(estimated_income) AS avg_income,
    SUM(bank_loans) AS total_loans
FROM customer
GROUP BY
    banking_relationship
ORDER BY
    total_loans DESC;
```

## 4️⃣ Python — EDA Connection

```python
import pandas as pd
import mysql.connector

connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="banking_case"
)

df = pd.read_sql("SELECT * FROM customer", connection)
```

## 5️⃣ Python — Income Band Feature Engineering

```python
bins = [0, 50000, 150000, df["estimated_income"].max()]
labels = ["Low", "Mid", "High"]

df["income_band"] = pd.cut(
    df["estimated_income"],
    bins=bins,
    labels=labels
)
```

## 6️⃣ Python — Correlation Check (Deposits)

```python
deposit_cols = [
    "bank_deposits",
    "checking_account",
    "savings_account",
    "foreign_currency_account"
]

correlation_matrix = df[deposit_cols].corr()
print(correlation_matrix)
```

### 🧮 Concepts Demonstrated

```text
✓ Database Design & Schema Creation
✓ Aggregations (SUM, AVG, COUNT)
✓ GROUP BY / ORDER BY
✓ Python–MySQL Integration (pd.read_sql)
✓ Feature Engineering (pd.cut)
✓ Exploratory Data Analysis (EDA)
✓ Correlation Analysis
✓ Univariate & Multivariate Analysis
```

---

# 📐 DAX Measures

```dax
Total Loan = 
SUM(banking_case[bank_loans]) 
+ SUM(banking_case[business_lending]) 
+ SUM(banking_case[credit_card_balance])

Total Deposit = 
SUM(banking_case[bank_deposits]) 
+ SUM(banking_case[savings_account]) 
+ SUM(banking_case[checking_account]) 
+ SUM(banking_case[foreign_currency_account])

Year of Joining = YEAR(banking_case[joined_bank])
```

---

# 💡 Key Insights & Findings

## 1️⃣ 💳 Credit Card Distribution

About **66%** of customers hold only one credit card; females are more inclined to hold a single card, while the proportion of males holding two or more cards is higher.

## 2️⃣ 📊 Financial Skewness

All numeric financial variables (loans, deposits, balances) show a **right-skewed** distribution.

## 3️⃣ 🔗 Deposit Correlation

A strong positive correlation exists between bank deposits, checking accounts, savings accounts, and foreign currency accounts (**correlation ≈ 0.41**).

## 4️⃣ 🧩 Credit Usage Independence

No strong correlation exists between income or loan size and credit card balance.

## 5️⃣ 🏦 Overall Portfolio Indicators

| Indicator | Value |
|---|---:|
| 💰 Total Loan Portfolio | **≈ 4.38 Billion** |
| 💵 Total Deposit Portfolio | **≈ 3.77 Billion** |
| 🏆 Top Banking Relationship Segments | **Private Bank and Commercial Bank** |

---

# 🧩 Skills Demonstrated

```text
✓ SQL (MySQL) — Schema Design & Queries
✓ Python (pandas, matplotlib, seaborn)
✓ Exploratory Data Analysis (EDA)
✓ Feature Engineering
✓ Power Query
✓ DAX
✓ Power BI Development
✓ Data Modeling
✓ Business Intelligence
✓ KPI Development
✓ Dashboard Design (UI/UX)
✓ Data Storytelling
```

---

# 📁 Project Structure

```text
banking-risk-analytics/
│
├── data/
│   ├── raw_banking_data.xlsx        # Original raw data
│   └── banking.csv                  # File prepared for import
│
├── notebooks/
│   └── banking_eda_analysis.ipynb   # Python analysis notebook (EDA + MySQL Connector)
│
├── sql/
│   └── schema_and_queries.sql       # Database creation script and queries
│
├── dashboard/
│   ├── banking_dashboard.pbix       # Interactive Power BI file
│   └── canva_backgrounds/           # Backgrounds and design assets
│
├── images/
│   └── dashboard-preview.png        # Preview images for the README
│
├── requirements.txt                 # Required Python libraries
└── README.md
```

---

# ⚙️ How to Run / Installation

### 1. Clone the Repository

```bash
git clone https://github.com/ASHRAF29403/banking-risk-analytics.git
cd banking-risk-analytics
```

### 2. Set Up the Database (MySQL)

```sql
CREATE DATABASE banking_case;
USE banking_case;
```

Then import `data/banking.csv` into the `customer` table.

### 3. Set Up the Python Environment

```bash
pip install -r requirements.txt
jupyter notebook notebooks/banking_eda_analysis.ipynb
```

### 4. Run the Dashboard

Open `dashboard/banking_dashboard.pbix` in Power BI Desktop, refresh the MySQL connection (`localhost:3306`), then click **Refresh**.

---

# 🚀 Future Improvements

- 🤖 Add a Machine Learning model to predict customer default probability (Credit Default Prediction).
- ☁️ Publish the dashboard to Power BI Service for online access.
- ⏱️ Automate data refresh (Automated ETL Pipeline).

---

# ✉️ Contact / Author

**Ashraf Nabil Mohamed**
Data Analyst | Machine Learning
🎓 Faculty of Computers and Informatics, Zagazig University — AI & Data Science

- 💻 GitHub: [@ASHRAF29403](https://github.com/ASHRAF29403)
- 🔗 LinkedIn: [add your link here]
- 📧 Email: [add your email here]

</div>
