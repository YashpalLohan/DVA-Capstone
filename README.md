# 📊 Strategic Risk Analysis & Portfolio Optimization  

**Sector:** Financial Services / Peer-to-Peer Lending  
**Team:** G-14  
**Institute:** Newton School of Technology, Rishihood University  

---

## 📌 Executive Summary  

### 🔎 Problem  
The current loan portfolio has a **1.11% default rate**, with concentrated risk in:
- High-risk credit grades (F & G)  
- Long-term (60-month) loans  

These segments threaten overall portfolio profitability.

### 🛠 Approach  
- Analyzed LendingClub Q1 2018 dataset (10,000+ records)  
- Conducted Exploratory Data Analysis (EDA)  
- Identified risk drivers across:
  - Credit Grade  
  - Loan Tenure  
  - Loan Purpose  
  - Debt-to-Income (DTI) Ratio  

### 📈 Key Insights  
- **Grade F** → 10.34% default rate (highest risk)  
- **60-month loans** → 1.49% default rate  
- **36-month loans** → 0.95% default rate  
- **House loans** → 3.97% default rate  

### ✅ Key Recommendation  
Implement **DTI ≤ 25% cap for 60-month loans**.

### 💰 Impact  
- Reduce default rate from **1.11% → ~0.90%**
- Protect approximately **$3.4M in principal**

---

# 🏦 Sector & Business Context  

## Industry Overview  
Peer-to-Peer (P2P) lending offers:
- Alternative borrower financing  
- Higher investor yields  
- But carries unsecured credit risk  

## Current Challenges  
- Rising defaults in sub-prime segments  
- Difficulty pricing long-term loans  

## Business Need  
Optimize portfolio to balance:
- **Yield:** 12.43%  
- **Default Risk:** 1.11%  

---

# 🎯 Problem Statement  

## Objective  
Identify high-risk cohorts contributing disproportionately to defaults and reduce risk **without significantly reducing yield**.

## Scope  
- Portfolio Value: **$163,619,225**
- Focus Areas:
  - Credit Grade
  - Term
  - Purpose
  - DTI Ratio

## Success Criteria  
- Measurable default rate reduction  
- Protect at least **$1M+ in principal**

---

# 🗂 Data Description  

- **Source:** LendingClub Q1 2018 Dataset  
- **Records:** 10,000+ loans  
- **Variables:** 50+  

## Key Columns  
- `loan_status` (Target)
- `grade`
- `sub_grade`
- `term`
- `purpose`
- `dti`
- `int_rate`
- `annual_inc`

## Limitations  
- Only Q1 2018 snapshot  
- Historical trends may not predict macroeconomic shocks  

---

# 🧹 Data Cleaning & Preparation  

- Removed/imputed missing values  
- Treated extreme DTI & income outliers  
- Converted `term` into numeric format  
- Engineered `default_flag` (Binary Target)  

**Assumption:**  
"Charged Off" and "Default" are treated as loss events.

---

# 📊 KPI Framework  

| KPI | Definition | Formula | Current Value |
|------|------------|----------|---------------|
| Default Rate | % of loans defaulted | (Defaults / Total Loans) × 100 | 1.11% |
| Average Yield | Mean interest rate | Avg(int_rate) | 12.43% |
| Portfolio Value | Total principal | Sum(loan_amnt) | $163.6M |
| Loss Given Default | Loss per default | Loan × (1 - Recovery Rate) | Estimated |

---

# 🔍 Exploratory Data Analysis (EDA)

## Default Rate by Grade  

| Grade | Default Rate |
|--------|--------------|
| A | 0.37% |
| B | 0.72% |
| C | 1.24% |
| D | 2.14% |
| E | 2.69% |
| F | 10.34% |
| G | 8.33% |

**Insight:** Grades F & G carry disproportionate risk.

---

## Default Rate by Term  

| Term | Default Rate |
|--------|-------------|
| 36 Months | 0.95% |
| 60 Months | 1.49% |

**Insight:** 60-month loans increase risk exposure by ~57%.

---

## Default Rate by Purpose  

| Purpose | Default Rate |
|----------|-------------|
| House | 3.97% |

**Insight:** Real estate-linked loans underperform.

---

# 🧠 Advanced Analysis  

## Risk Segmentation  
Identified toxic segment:
- 60-month loans  
- DTI > 25%  

## Scenario Analysis  

| Scenario | Default Rate |
|----------|--------------|
| Status Quo | 1.11% |
| Optimized Portfolio | ~0.90% |

**Projected Savings:** $3.4M  

---

# 🚀 Recommendations  

## 1️⃣ Cap DTI at 25% for 60-month loans  

- Reduces default concentration  
- Easy underwriting rule implementation  

## 2️⃣ Tighten Grade F & House Loan Criteria  

- Review pricing  
- Adjust approval standards  

---

# 📈 Impact Estimation  

- Default Rate: 1.11% → ~0.90%  
- Principal Protected: ~$3.4M annually  
- Reduced underwriting inefficiencies  

---

# ⚠️ Limitations  

- Single-quarter dataset  
- Assumes historical patterns persist  
- Cannot predict macroeconomic shocks  

---

# 🔮 Future Scope  

- Build Logistic Regression model  
- Train Random Forest classifier  
- Use real-time credit bureau data  
- Improve DTI verification  

---

# 🏁 Conclusion  

By addressing concentrated risk in **Grade F**, **60-month loans**, and **high DTI borrowers**, the portfolio can reduce defaults to ~0.9% and protect ~$3.4M in capital — achieving a stronger balance between risk and return.

---

# 👥 Contribution Matrix  

| Team Member | Dataset | Cleaning | KPI & Analysis | Dashboard | Report | PPT | Role |
|-------------|---------|----------|---------------|-----------|--------|-----|------|
| Abhigya Sachdeva | Medium | Medium | High | High | Low | Low | Dashboard Lead |
| Udit Jain | Medium | Low | Medium | Medium | Low | Low | Strategy Lead |
| Yashpal | Medium | High | Medium | High | Low | Low | Analysis Lead |
| Karan Chhillar | High | High | Low | Low | Low | High | Data Lead |
| Rishav Dewan | Medium | Low | Low | Low | High | Medium | PPT Lead |
| Rishiwant Kumar Maurya | Medium | Low | Medium | Low | Low | Medium | Project Lead |

---

## 📎 Appendix  

- Data Dictionary: Link  
- Extra Charts:
  - Distribution of Loan Amounts  
  - Interest Rate vs Grade Scatter Plot  

---

**Declaration:**  
We confirm that the above contribution details are accurate and verifiable through version history and submitted artifacts.
