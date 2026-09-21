# 🏦 Bank Loan Analysis

An end-to-end data analytics project that analyzes bank loan data to track lending performance, borrower behavior, and portfolio risk. The same analysis is built across **SQL, Excel, Power BI, and Tableau**, so results can be compared across tools.

---

## 📌 Project Overview

Banks need to monitor how many loans they issue, how much money is funded and recovered, and which borrower segments carry more risk. This project answers those questions with interactive dashboards and SQL queries built on loan application data.

**Objectives**
- Track key lending KPIs (applications, funded amount, amount received, interest rate, DTI)
- Measure growth using **MTD (Month-to-Date)** and **MoM (Month-over-Month)** trends
- Separate **Good Loans** from **Bad Loans** to understand portfolio health
- Break down applications by month, state, term, employment length, purpose, and home ownership
- Build reusable dashboards in Excel, Power BI, and Tableau

---

## 📊 Key Metrics (KPIs)

| KPI | Description |
|-----|-------------|
| Total Loan Applications | Number of loan applications received |
| Total Funded Amount | Total money lent to borrowers |
| Total Amount Received | Total payments collected from borrowers |
| Average Interest Rate | Mean interest rate across loans |
| Average DTI | Mean Debt-to-Income ratio of borrowers |
| Good Loan % | Share of loans that are Fully Paid or Current |
| Bad Loan % | Share of loans that are Charged Off |

Each KPI is also tracked as **MTD** and **MoM**.

---

## 📈 Dashboard Views

- **Summary**: KPI cards, applications by month, state, term, employment length, purpose, and home ownership
- **Overview**: Trends and comparisons across loan segments
- **Details**: Loan-level data table for drill-down

**Filters / Slicers:** Grade (A to G), Purpose, and more.

**Charts used:** Line chart (monthly trend), filled map (state-wise), doughnut (loan term), bar charts (employment length, purpose), treemap (home ownership).

---

## 📁 Repository Structure

```
Bank-Loan-Analysis/
│
├── assets/     # Screenshots, dashboard previews, icons
├── data/       # Raw and cleaned loan datasets
├── docs/       # Project documentation and requirements
├── excel/      # Excel dashboard (pivot tables, slicers)
├── powerBI/    # Power BI report (.pbix)
├── sql/        # SQL queries for KPIs and analysis
├── tableau/    # Tableau workbook
├── REQUIREMENTS.md
└── README.md
```

---

## 🛠️ Tools & Technologies

- **SQL** (MySQL / SQL Server): data querying and KPI calculation
- **Microsoft Excel**: pivot tables, pivot charts, slicers, dashboard
- **Power BI**: DAX measures, interactive report
- **Tableau**: calculated fields, dashboard

See [REQUIREMENTS.md](REQUIREMENTS.md) for full details and versions.

---

## 🚀 How to Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/faizanjutt473/Bank-Loan-Analysis.git
   cd Bank-Loan-Analysis
   ```
2. **Explore the data** in the `data/` folder.
3. **Run SQL queries** from the `sql/` folder on your database (import the dataset first).
4. **Open the dashboards:**
   - Excel: `excel/` → open the `.xlsx` file
   - Power BI: `powerBI/` → open the `.pbix` file in Power BI Desktop
   - Tableau: `tableau/` → open the `.twbx` file in Tableau Desktop / Public
5. Use the **slicers/filters** to explore by grade, purpose, and other fields.

---

## 🔍 Sample Insights

- Loan applications show a steady upward trend across the year.
- **Debt consolidation** is the most common loan purpose by a large margin.
- Borrowers with **10+ years** of employment apply the most.
- **36-month** loans are more common than 60-month loans.
- Most borrowers are on **Rent** or **Mortgage**, with far fewer owning their homes.

> Update these points with the exact figures from your final analysis.

---

## 👤 Author

**Muhammad Faizan Farooq**
- GitHub: [faizanjutt473](https://github.com/faizanjutt473)
- LinkedIn: [Muhammad Faizan Farooq](https://www.linkedin.com/in/muhammad-faizan-farooq-8bab35372)
- Email: faizanprogrammer12@gmail.com

---

## 📄 License

This project is for learning and portfolio purposes.
