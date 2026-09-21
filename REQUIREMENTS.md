# Requirements: Bank Loan Analysis

This document lists the business requirements, data requirements, and software needed to run or reproduce the project.

---

## 1. Business Requirements

### 1.1 KPIs to Report
| # | KPI | MTD | MoM |
|---|-----|-----|-----|
| 1 | Total Loan Applications | ✔ | ✔ |
| 2 | Total Funded Amount | ✔ | ✔ |
| 3 | Total Amount Received | ✔ | ✔ |
| 4 | Average Interest Rate | ✔ | ✔ |
| 5 | Average Debt-to-Income (DTI) Ratio | ✔ | ✔ |

### 1.2 Loan Quality Analysis
- **Good Loans**: loan status = *Fully Paid* or *Current*
  - Good Loan Application %, Applications, Funded Amount, Amount Received
- **Bad Loans**: loan status = *Charged Off*
  - Bad Loan Application %, Applications, Funded Amount, Amount Received
- Loan Status grid view (Fully Paid, Current, Charged Off) with all KPIs

### 1.3 Required Charts / Views
| Chart | Purpose |
|-------|---------|
| Line chart | Total applications by month |
| Filled map | Total applications by state |
| Doughnut chart | Applications by loan term (36 / 60 months) |
| Bar chart | Applications by employment length |
| Bar chart | Applications by loan purpose |
| Treemap | Applications by home ownership |
| Detail table | Loan-level drill-down |

### 1.4 Filters / Slicers
- Grade (A to G)
- Purpose
- (Optional) State, Term, Home Ownership

---

## 2. Data Requirements

Place the dataset in the `data/` folder. The dataset should contain the following fields:

| Field | Description |
|-------|-------------|
| id | Unique loan ID |
| address_state | Borrower's state |
| application_type | Type of application |
| emp_length | Employment length |
| emp_title | Job title |
| grade / sub_grade | Loan grade |
| home_ownership | Rent / Mortgage / Own |
| issue_date | Loan issue date |
| last_credit_pull_date | Last credit check date |
| last_payment_date | Last payment date |
| loan_status | Fully Paid / Current / Charged Off |
| next_payment_date | Next payment date |
| member_id | Borrower ID |
| purpose | Reason for the loan |
| term | 36 or 60 months |
| verification_status | Income verification status |
| annual_income | Borrower's annual income |
| dti | Debt-to-income ratio |
| installment | Monthly installment |
| int_rate | Interest rate |
| loan_amount | Funded amount |
| total_acc | Total credit accounts |
| total_payment | Amount received |

> Field names may differ slightly depending on your dataset version. Adjust the SQL queries and measures accordingly.

### Data Quality Checks
- Remove duplicate loan IDs
- Convert date columns to proper date format
- Handle missing values in `emp_length`, `emp_title`, and payment dates
- Convert interest rate and DTI to percentages

---

## 3. Software Requirements

| Tool | Recommended Version | Used For |
|------|--------------------|----------|
| Microsoft Excel | 2019 / Microsoft 365 | Pivot tables, slicers, dashboard |
| MySQL Workbench or SQL Server (SSMS) | MySQL 8.0+ / SQL Server 2019+ | KPI queries |
| Power BI Desktop | Latest | Interactive report, DAX |
| Tableau Desktop / Public | 2023.x or later | Tableau dashboard |
| Git | Any recent | Version control |

> Note: The filled map chart in Excel needs an internet connection (Bing Maps).

---

## 4. Hardware Requirements

- 8 GB RAM recommended (4 GB minimum)
- Windows 10 / 11 (required for Power BI Desktop)
- Around 1 GB free disk space

---

## 5. Deliverables

- [x] SQL queries for all KPIs (`sql/`)
- [x] Excel dashboard (`excel/`)
- [x] Power BI report (`powerBI/`)
- [x] Tableau dashboard (`tableau/`)
- [x] Project documentation (`docs/`)
- [x] README with project overview

---

## 6. Assumptions

- The dataset covers loan applications for a single year.
- MTD is calculated for the latest month (December), and MoM compares it with the previous month (November).
- Good Loan = Fully Paid + Current, Bad Loan = Charged Off.
