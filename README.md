# Marketing Campaign Impact Analysis

## 🔍 Use Case
Identify which marketing campaigns and sales‑contact touchpoints drive the highest revenue, overall and by client segment, to optimize budget allocation and maximize ROI.

## 📊 Dataset
- **Source:** `marketing_data.csv`  
- **Key fields:**  
  - `calendar_date` (month, year)  
  - `Client_Type` (e.g. Small/Medium/Large Facility)  
  - `Campaign_Email`, `Campaign_Flyer`, `Campaign_Phone`  
  - `Sales_Contact_1` … `Sales_Contact_5`  
  - `Amount_Collected` (target)

## 🚀 Steps
1. **Data Ingestion & Cleaning**  
   - Read CSV, convert dates, handle missing values  
2. **Exploratory Data Analysis**  
   - Distribution by client type, average revenue comparisons  
3. **Correlation Analysis**  
   - Global and per‑segment correlation vs. `Amount_Collected`  
4. **Regression Modeling**  
   - OLS:  
     ```
     Amount_Collected ~ Campaign_* + Sales_Contact_*
     ```
   - Extract coefficients & p‑values  
5. **Recommendations**  
   - Translate coefficients into “$ return per $1 spent”  
   - Prioritize top drivers and pause low‑impact channels

## 🎯 Outcomes
- **Medium Facilities:** Flyer campaigns yield ~4× return  
- **Small Facilities:** Email campaigns yield ~3.2× return  
- **Large Facilities:** Sales Contact 5 yields ~2.8× return  
- **Actionable Insight:** Reallocate ~20% of low‑ROI spend to these top drivers for an estimated 10–15% uplift in collected revenue

## 🛠 Tools & Technologies
- **Languages & Libraries:** Python, Pandas, NumPy, statsmodels, Matplotlib/Seaborn  
- **Environment:** Jupyter Notebook  
- **Version Control:** Git & GitHub  
- **Visualization:** Static plots (can be extended to Tableau/PowerBI)
