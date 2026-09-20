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

<em>معاينة للصفحة الرئيسية للوحة التحكم التفاعلية في Power BI</em>

</div>

مشروع تحليل بيانات شامل لتقييم المخاطر الائتمانية وتحليل محفظة القروض والودائع لـ **3,000 عميل بنكي**، بهدف مساعدة المؤسسات المالية على اتخاذ قرارات إقراض مدروسة وتقليل مخاطر التخلف عن السداد.

> 📝 استبدل الصورة في الأعلى بسكرين شوت حقيقي من الداشبورد بتاعك — ضعه داخل مجلد `images/` باسم `dashboard-preview.png`.

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

تواجه البنوك والمؤسسات المالية مخاطر عدم سداد القروض من قِبل بعض العملاء بمختلف شرائحهم، مما يؤدي إلى خسائر مالية متراكمة. يهدف هذا المشروع إلى:

- 🔍 **تحليل المخاطر الائتمانية**: تقديم رؤى حول سلوك الاقتراض والودائع لمختلف شرائح العملاء (دخل مرتفع، متوسط، منخفض).
- 📉 **تقليل مخاطر التعثر**: مساعدة إدارة البنك على اكتشاف الأنماط والسلوكيات عالية المخاطر لتقليل الخسائر أثناء منح القروض.
- 📊 **بناء لوحة تحكم تفاعلية**: توفير مؤشرات أداء رئيسية (KPIs) لمختلف المستويات الإدارية لمتابعة محفظة القروض والودائع لحظياً.

---

# 📊 Dataset Overview

<div align="center">

| الخاصية | القيمة |
|---|---:|
| 📦 عدد السجلات | **3,000 عميل** |
| 📐 عدد الأعمدة | **25 عمود** |
| 🌍 نوع البيانات | **مالية وديموغرافية** |

</div>

### أهم الأعمدة

```text
✓ معلومات العملاء       → العمر (17–85)، الموقع، الجنسية، المهنة، تاريخ الانضمام
✓ العلاقة المصرفية      → تجزئة / مؤسسات / بنك خاص / تجاري، المستشار الاستثماري، هيكل الرسوم
✓ البيانات الائتمانية   → الدخل المقدر، رصيد التقاعد، عدد بطاقات الائتمان، تقييم CIBIL، عدد العقارات
✓ الحسابات والقروض     → القروض المصرفية، إقراض الأعمال، رصيد بطاقة الائتمان، الودائع، الحسابات الجارية/التوفير، العملات الأجنبية
```

> ⚠️ **ملاحظة**: البيانات المستخدمة في هذا المشروع بيانات تعليمية/محاكاة (Simulated Dataset) لأغراض التحليل والتدريب، وليست بيانات عملاء حقيقيين.

---

# 🛠️ Tech Stack

<div align="center">

| الأداة | الاستخدام |
|---|---|
| 🐍 **Python 3.x** (pandas, matplotlib, seaborn) | التحليل الاستكشافي (EDA) وهندسة الخصائص |
| 🗄️ **MySQL** | تخزين البيانات والاستعلام عنها |
| 📊 **Power BI Desktop** (Power Query, DAX) | نمذجة البيانات وبناء لوحة التحكم التفاعلية |
| 🎨 **Canva** | تصميم الخلفيات والمخططات الهيكلية للداشبورد |
| 🔗 **PyMySQL / mysql-connector-python** | الربط البرمجي بين Python وMySQL |

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

### خطوات العمل بالتفصيل

1. **إدخال البيانات وقاعدة البيانات**: تحويل البيانات إلى CSV واستيرادها إلى قاعدة بيانات MySQL باسم `banking_case`.
2. **الربط والتحليل الاستكشافي (EDA)**: ربط Python بـ MySQL عبر `pd.read_sql`، وإجراء تحليل أحادي ومتعدد المتغيرات.
3. **هندسة الخصائص**: تصنيف الدخل المقدر إلى شرائح (`High`, `Mid`, `Low`) باستخدام `pd.cut`، وتحويل المعرفات الرقمية إلى تسميات نصية.
4. **التصميم والتخطيط**: رسم سكتشات للواجهات وتصميم خلفيات Canva لإنشاء 5 صفحات (الرئيسية، القروض، الودائع، الملخص، الأسئلة والأجوبة).
5. **بناء لوحة التحكم**: ربط Power BI بقاعدة البيانات، تفعيل التنقل بين الصفحات، وصياغة مقاييس DAX.

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

## 1️⃣ 💳 توزيع بطاقات الائتمان

حوالي **66%** من العملاء يحملون بطاقة ائتمانية واحدة فقط؛ الإناث أكثر ميلاً لبطاقة واحدة، بينما ترتفع نسبة الذكور الحاملين لبطاقتين أو أكثر.

## 2️⃣ 📊 الالتواء المالي

جميع المتغيرات المالية الرقمية (قروض، ودائع، أرصدة) تُظهر توزيعاً ملتوياً نحو اليمين (**Right-Skewed**).

## 3️⃣ 🔗 ارتباط الودائع

ارتباط إيجابي قوي بين الودائع المصرفية، الحسابات الجارية، حسابات التوفير، وحسابات العملات الأجنبية (**correlation ≈ 0.41**).

## 4️⃣ 🧩 استقلالية استخدام الائتمان

لا يوجد ارتباط قوي بين الدخل أو حجم القروض ورصيد البطاقة الائتمانية.

## 5️⃣ 🏦 المؤشرات الإجمالية للمحفظة

| المؤشر | القيمة |
|---|---:|
| 💰 إجمالي محفظة القروض | **≈ 4.38 مليار** |
| 💵 إجمالي محفظة الودائع | **≈ 3.77 مليار** |
| 🏆 أبرز فئات العلاقة المصرفية | **البنك الخاص والبنك التجاري** |

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
│   ├── raw_banking_data.xlsx        # البيانات الخام الأصلية
│   └── banking.csv                  # الملف المجهز للاستيراد
│
├── notebooks/
│   └── banking_eda_analysis.ipynb   # دفتر تحليلات بايثون (EDA + MySQL Connector)
│
├── sql/
│   └── schema_and_queries.sql       # سكريبت إنشاء قاعدة البيانات والاستعلامات
│
├── dashboard/
│   ├── banking_dashboard.pbix       # ملف Power BI التفاعلي
│   └── canva_backgrounds/           # الخلفيات والتصميمات
│
├── images/
│   └── dashboard-preview.png        # صور المعاينة للـ README
│
├── requirements.txt                 # مكتبات بايثون المطلوبة
└── README.md
```

---

# ⚙️ How to Run / Installation

### 1. استنساخ المستودع

```bash
git clone https://github.com/ASHRAF29403/banking-risk-analytics.git
cd banking-risk-analytics
```

### 2. إعداد قاعدة البيانات (MySQL)

```sql
CREATE DATABASE banking_case;
USE banking_case;
```

ثم استورد `data/banking.csv` إلى جدول `customer`.

### 3. إعداد بيئة Python

```bash
pip install -r requirements.txt
jupyter notebook notebooks/banking_eda_analysis.ipynb
```

### 4. تشغيل لوحة التحكم

افتح `dashboard/banking_dashboard.pbix` في Power BI Desktop، حدّث اتصال MySQL (`localhost:3306`)، ثم اضغط **Refresh**.

---

# 🚀 Future Improvements

- 🤖 إضافة نموذج تعلم آلي (Machine Learning) للتنبؤ باحتمالية تعثر العميل عن السداد (Credit Default Prediction).
- ☁️ نشر لوحة التحكم على Power BI Service لإتاحة الوصول الأونلاين.
- ⏱️ أتمتة تحديث البيانات (Automated ETL Pipeline).

---

# ✉️ Contact / Author

**Ashraf Nabil Mohamed**
Data Analyst | Machine Learning
🎓 Faculty of Computers and Informatics, Zagazig University — AI & Data Science

- 💻 GitHub: [@ASHRAF29403](https://github.com/ASHRAF29403)
- 🔗 LinkedIn: [أضف رابط حسابك هنا]
- 📧 Email: [أضف بريدك هنا]

</div>
