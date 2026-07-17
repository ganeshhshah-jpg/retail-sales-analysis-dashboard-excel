# Zenith  Retail Annual Sales Report 2024

**A data cleaning and Retail sales analytics project built entirely in Excel — transforming messy raw transaction data into a clean, interactive sales dashboard.**

---

## 📌 Table of Content
- <a href="#overview">Overview</a>
- <a href="#problem-statement">Problem Statement</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#methods">Methods</a>
- <a href="#key-insights">Key Insights</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#results--conclusion">Results & Conclusion</a>
- <a href="#future-work">Future Work</a>
- <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

This project takes a full year (2024) of raw retail sales transactions from Zenith and turns them into a decision-ready reporting workbook. It covers the entire mini data pipeline: auditing data quality issues in the raw export, cleaning and standardizing the data, and building summary tables and a dashboard on top of the cleaned dataset — all using native Excel tools (no external BI software required).

---

<h2><a class="anchor" id="problem-statement"></a>Problem Statement</h2>

The raw sales export handed off by the source system was **not analysis-ready**. It contained inconsistent text casing, multiple date formats, stray currency symbols, mixed discount formats, duplicate/blank rows, and missing values — the kind of real-world mess that, left untouched, would silently break any pivot table or chart built on top of it. The goal of this project was to identify every one of these issues, document them, clean them systematically, and produce a reliable dataset for reporting on regional performance, store performance, product category trends, and payment method behavior.

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

The workbook contains **2,035 raw order records** for the year 2024, cleaned down to **2,020 validated records** after removing duplicates and blank rows. Key fields include:

| Column | Description |
|---|---|
| Order ID | Unique identifier for each order |
| Order Date | Date the order was placed |
| Customer Name | Name of the customer |
| Region | Sales region (Central, East, North, South, West) |
| Store | Physical store location |
| Product Category | Category of product sold (Electronics, Furniture, Clothing, etc.) |
| Product Name | Specific product sold |
| Quantity | Units sold in the order |
| Unit Price | Price per unit |
| Discount | Discount applied to the order |
| Payment Method | How the customer paid (Cash, Card, UPI, EMI, Net Banking) |
| Sales Rep | Sales representative who closed the order |

A full **Data Dictionary** sheet documents each column's known data quality issues (inconsistent casing, mixed date formats, text-formatted prices, mixed discount notation, negative quantities, duplicate/blank rows) alongside the exact method used to resolve each one.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- **Microsoft Excel** — data cleaning, formulas, and PivotTables
- **Power Query** — de-duplication and data type standardization
- Core functions used: `PROPER()`, `TRIM()`, `VALUE()`, `ABS()`, `IF()`, `XLOOKUP` / `VLOOKUP`, `DATEVALUE()`

---

<h2><a class="anchor" id="methods"></a>Methods</h2>

1. **Audit** — Reviewed the raw dataset and cataloged every data quality issue in a dedicated Data Dictionary sheet.
2. **Standardize text fields** — Applied `PROPER()` + `TRIM()` to fix inconsistent casing and stray whitespace in Region and Product Category.
3. **Normalize dates** — Converted five different date text formats into a single consistent Date type using Text to Columns / Power Query, and derived a Month column.
4. **Fix numeric fields** — Stripped currency prefixes from Unit Price and converted text to numbers; standardized Discount into a consistent decimal format; resolved negative Quantity values.
5. **Handle blanks and duplicates** — Removed ~20 fully duplicated rows and ~15 blank rows, and imputed or flagged missing Customer Name and Quantity values.
6. **Derive metrics** — Calculated a Total Amount field per order and rolled it up into summary tables.
7. **Build the dashboard** — Aggregated the cleaned data into Sales vs Orders (by month), Sales by Region, Payment Methods, Top 5 Stores, and Top Product Categories, then visualized them on a single Dashboard sheet.

---

<h2><a class="anchor" id="key-insights"></a>Key Insights</h2>

- **Total sales for 2024: ₹8.78 crore** (₹87,770,369.83) across 2,020 cleaned orders.
- **North** was the top-performing region (₹1.92 crore), followed closely by **West** (₹1.82 crore); **South** was the lowest at ₹1.57 crore.
- **December, January, and July** were the strongest months by revenue; **February** was the weakest.
- **Net Banking** was the leading payment method by revenue (₹1.63 crore), with the remaining methods (Cash, Credit Card, Debit Card, EMI, UPI) fairly evenly split.
- **Chandigarh Store** led all stores in total sales among the top 5.
- **Home Appliances and Electronics** led in units sold across product categories.

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

The workbook includes a consolidated **Dashboard** sheet combining:
- Monthly Sales vs Orders trend
- Sales by Region breakdown
- Payment Method distribution
- Top 5 Stores by revenue
- Top Product Categories by quantity sold

This gives a single-page view of business performance for 2024.

![alt text](/Users/ganeshshah/Desktop/Data\ Analytics/Retail\ Sales\ Analysis\ Project/images/Dashboard.png)


---

<h2><a class="anchor" id="results--conclusion"></a>Results & Conclusion</h2>

After cleaning, the dataset went from an unreliable raw export to a fully validated set of 2,020 orders ready for analysis. The resulting dashboard shows that Zenith's 2024 performance was fairly balanced across regions, with the North leading, and revenue peaking around the December and July shopping periods. The project demonstrates that rigorous, well-documented data cleaning in Excel alone is enough to produce trustworthy, decision-ready business reporting without needing a separate BI tool.

---

<h2><a class="anchor" id="future-work"></a>Future Work</h2>

- Automate the cleaning steps using Power Query so future monthly/quarterly data refreshes don't require manual rework.
- Add year-over-year comparisons once 2025 data becomes available.
- Build a customer-level segmentation (RFM analysis) on top of the cleaned dataset.
- Migrate the dashboard to Power BI or Tableau for more advanced interactivity.

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Ganesh Shah**
📧 *ganeshhshah@gmail.com*
🔗 [LinkedIn](https://www.linkedin.com/in/ganesh-shah-195774296//)



