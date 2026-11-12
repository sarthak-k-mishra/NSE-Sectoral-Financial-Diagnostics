# NSE-Sectoral-Financial-Diagnostics

**End-to-End Analytics Pipeline | Python · SQL · Power BI · Excel**

---

### Business Problem

Investors often misjudge NSE-listed companies by focusing purely on top-line growth or surface-level valuation. The objective was to build a multi-dimensional diagnostic pipeline to uncover hidden leverage risks ("Danger Zones"), expose high-growth valuation traps, and screen for fundamentally robust "Hidden Gems" across 393 companies.

---

### Key Findings

* **E-Commerce sector** identified as a severe valuation trap trading at a **41x PE/ROE ratio** vs Mining at a heavily discounted **0.6x**

* **Zomato** masked poor profit growth (16%) behind high sales growth (56%), yielding a **0.26 Growth Quality Ratio** (worst among Top 50 companies)

* **18 non-financial companies** identified in the "Danger Zone" with highly leveraged structures (**D/E > 3.0**), including Adani Green and JSW Steel

* **Only 19 companies (4.6%)** screened as "Hidden Gems" passing all 4 stringent fundamental criteria

* **200bps interest rate hike** stress test revealed severe net profit margin compression risk for high-leverage non-financial entities

<br>

### Power BI Dashboard<img width="1297" height="727" alt="image" src="https://github.com/user-attachments/assets/5a90cdc8-5cb0-454c-b085-9d5f7d679ff4" />


---

### Tools & Technologies

| Tool | Purpose |
| :--- | :--- |
| Python (Pandas) | Metric engineering, data merging |
| SQL (Window Functions) | 3D composite ranking, screening |
| Power BI (DAX) | Financial intelligence dashboard |
| Excel (Scenario Manager, XLOOKUP) | Stress-testing, financial lookup |

---

### Project Structure

#### Python Analysis Highlights

* Merged **6 financial datasets** across **393 NSE-listed companies**
* Engineered **Valuation Trap Score** (`PE / ROE`) exposing sector extremes
* Calculated **Growth Quality Ratio** revealing fundamental mismatches between sales CAGR and profit growth
* Exported clean tables for SQL and Power BI consumption

#### SQL Highlights

* **3-dimensional composite sector ranking** using `RANK()` window functions across ROE, ROCE, and Debt/Equity
* **Danger Zone identification** filtering non-financial companies with `WHERE Debt_Equity > 3.0`
* **Hidden Gems screening** applying strict `AND` conditions to filter the top 4.6% of companies

#### Power BI Dashboard

* **3-page financial intelligence dashboard**
* **PE vs ROE bubble chart** plotting 393 companies to visually expose valuation traps
* **Sector heatmap matrix** evaluating performance across 4 financial dimensions
* **Classification table** contrasting Hidden Gems vs Danger Zone with an integrated promoter signal tracker

#### Excel Modeling

* **Company financial lookup tool** built using `XLOOKUP`
* **Scenario Manager** stress-testing 18 Danger Zone companies
* **What-If Analysis** quantifying the net profit impact of a 200bps interest rate rise on the high-leverage non-financial sector

---

### Dataset

Source: Key Insights of 400 NSE Listed Companies-Uploaded by Yashregressor on Kaggle

---

### Key Business Recommendation

Avoid sectors exhibiting severe Valuation Trap Scores (e.g., E-Commerce at 41x) and strictly monitor highly leveraged non-financial companies (D/E > 3.0, such as Adani Green) for margin compression under rising interest rate scenarios. Reallocate capital towards the 4.6% "Hidden Gems" that demonstrate sustainable leverage, clean promoter signals, and true profit-backed growth.
