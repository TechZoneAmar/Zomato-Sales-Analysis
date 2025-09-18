# Zomato-Sales-Analysis
This project presents a dynamic Excel-based Zomato Sales Dashboard that analyzes customer preferences, restaurant performance, order trends, and revenue distribution to deliver actionable business insights.
# Zomato Sales Dashboard
---

## 🚀 Project Overview
This repository contains the files, documentation, and instructions to reproduce a professional, interactive sales dashboard built in **Microsoft Excel** using a Zomato orders dataset (10,000 records). The dashboard leverages Pivot Tables, Pivot Charts, Slicers, and Timelines to provide dynamic business insights for stakeholders.

---

## 📁 Repository Structure (suggested)
Zomato-Sales-Dashboard/
├── data/
│ └── zomato_orders.csv # cleaned CSV used for Excel
├── excel/
│ └── Zomato_Sales_Dashboard.xlsx # final dashboard workbook (if permitted)
├── images/
│ └── dashboard_screenshot.png
├── reports/
│ └── Zomato_Sales_Report.docx # full written report (optional)
├── README.md
└── README-template.md # this file


---

## 📊 What’s Included
- `data/zomato_orders.csv` — cleaned dataset with key columns: `Order_ID`, `Order_Date`, `Cuisine`, `Restaurant_Name`, `Order_Amount`, `Payment_Method`, `Rating`, `Is_Discount_Applied`, `Delivery_Time_Minutes`, etc.
- `excel/Zomato_Sales_Dashboard.xlsx` — interactive Excel workbook (Pivot Tables, charts, slicers & timeline).
- `images/dashboard_screenshot.png` — screenshot of the dashboard for README preview.
- `reports/Zomato_Sales_Report.docx` — full project report and business recommendations (optional).

> ⚠️ If your organization restricts sharing raw data or the full workbook, include a sanitized sample CSV and screenshots instead.

---

## 🔧 How to Reproduce (Excel - Step by Step)

1. **Open the data**
   - Open `zomato_orders.csv` in Excel or import the raw workbook.

2. **Data preparation**
   - Ensure dates are real Excel dates.  
     `Order_Date` → Format: `Date`
   - Add helper columns:
     - `Order_Month` → `=TEXT([@Order_Date], "YYYY-MM")`
     - `Order_Week` → `=TEXT([@Order_Date],"YYYY-WW")` (optional)

3. **Create Table**
   - Select your data → `Insert` → `Table` (helps pivot auto-refresh and slicer linking).

4. **Pivot Tables**
   - Insert multiple Pivot Tables on a new sheet:
     - Cuisine vs Count of Order_ID (Order Count)
     - Cuisine vs Average of Order_Amount (Avg Order Value)
     - Order_Month vs Count of Order_ID and Avg of Order_Amount (trends)
     - Payment_Method vs Sum of Order_Amount (payment contribution)
     - Restaurant_Name vs Sum of Order_Amount (Top restaurants)
     - Rating vs Count of Order_ID (ratings distribution)
     - Is_Discount_Applied vs Avg Order_Amount & Avg Rating

5. **Pivot Charts**
   - Convert Pivot Tables to charts:
     - Bar/Column charts for cuisine/restaurant comparisons
     - Line chart for monthly trends (Orders & Avg amount — secondary axis if needed)
     - Pie/Donut chart for Ratings and Payment Method shares
     - Scatter plot for Delivery_Time vs Rating (data chart, not pivot)

6. **Add Slicers & Timeline**
   - `PivotTable Analyze` → `Insert Slicer` for `Cuisine`, `Payment_Method`, `Restaurant_Name`, `Is_Discount_Applied`.
   - `Insert Timeline` for `Order_Date`.
   - Connect slicers/timeline to all pivot tables (Report Connections).

7. **Dashboard Layout**
   - Create `Dashboard` sheet and place:
     - Top-left: Project title and screenshot/logo
     - Top-right: KPIs (Total Orders, Total Revenue, Avg Rating, Avg Delivery Time) using small pivot tables
     - Middle: Main charts (Cuisine, Top 10 restaurants, Ratings, Payment Methods)
     - Bottom: Trend chart (Monthly Orders & Avg Amount) and scatter (Delivery vs Rating)
     - Place slicers/timeline at the top for clear interaction

8. **Formatting & UX**
   - Use consistent fonts, bold chart titles, add data labels where helpful.
   - Ensure slicers are sized uniformly and aligned.
   - Freeze panes and hide intermediate pivot sheets if sharing the workbook.

---

## 📈 Visualizations & KPIs
- KPI Cards: Total Orders, Total Revenue, Average Order Amount, Average Rating, Average Delivery Time.
- Visuals:
  - Cuisine-wise Order Count (Bar)
  - Cuisine-wise Avg Order Value (Bar)
  - Top 10 Restaurants by Revenue (Bar)
  - Monthly Orders & Avg Order Amount (Line chart with dual axis)
  - Ratings Distribution (Pie chart)
  - Payment Method Contribution (Pie chart)
  - Delivery Time vs Rating (Scatter plot)

---

## 📝 Key Insights (summary)
- Indian, Italian, and American cuisines lead order volume.
- Italian cuisine shows the highest average order value.
- A small set of restaurants contributes disproportionately to revenue (top 10).
- Ratings distribution suggests opportunities to improve customer experience.
- Most customers use digital payment methods (UPI, Debit/Credit).

---

## 💡 Business Recommendations
- Focus marketing on high-demand, high-value cuisines (Indian & Italian).
- Negotiate exclusive deals with top-performing restaurants.
- Investigate low-rating orders for operational improvements (delivery times, packaging).
- Promote digital payments with small incentives and cashback.

---

## 🔁 How to Update Data
1. Replace `data/zomato_orders.csv` with a new file (same column structure).
2. Open the Excel workbook and click `Data` → `Refresh All` (pivots and slicers will update).
3. If table range changed, convert to Table and reconnect pivots/slicers as needed.

---

## 🛠️ Tools & Skills Demonstrated
- Microsoft Excel: Table, Pivot Table, Pivot Chart, Slicer, Timeline, formulas.
- Dashboard design & data storytelling.
- Basic exploratory analysis and business recommendations.

---

## 📚 Future Enhancements
- Publish dashboard to Power BI for cloud sharing and advanced interactions.
- Add forecasting (seasonal trends) and cohort analysis.
- Create automated refresh using Power Query (for scheduled updates).
- Add sentiment analysis of review text (requires Python or Power BI R script).

---

## 📞 Contact
**Author:** Your Name (replace)  
**Email:** your.email@example.com (replace)  
**Organization:** (optional)

---

## 📜 License
Add a license (e.g., MIT) if you want others to reuse your dashboards and code.  
Example: `LICENSE` → MIT License.

---

### Example Git commands to push this README and files:
```bash
git init
git add .
git commit -m "Initial commit: Zomato Sales Dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/Zomato-Sales-Dashboard.git
git push -u origin main
