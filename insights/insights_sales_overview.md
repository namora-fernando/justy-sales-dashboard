# 📈 Dashboard 1: Sales Overview – Key Findings  
> **Date range**: July 2025  
> **Data source**: 381 unique transactions from Table #1 (`Laporan Penjualan`)  

---

## 🧮 Key Measures Used:
```DAX
Total Revenue = SUM('Laporan Penjualan'[Total_Final])
Total Transactions = COUNTROWS('Laporan Penjualan')
Average Transaction Value = DIVIDE([Total Revenue], [Total Transactions])
```

---

## 🔍 Key Observations

- **Highest daily revenue** occurred on **July 19**, peaking at **Rp1.044M**
- A clear **mid-month slowdown** was observed between **July 10–14**, likely due to **end-of-paycycle** (a common period of reduced spending behavior)
- **Average transaction value** stands at **Rp33.97K**, suggesting a relatively small purchase per visit
- **Weekday performance** (Saturday-Sunday) consistently surpassed weekdays in both transaction count and total revenue

---

## 💡 Business Implications

- The spike on July 19 (Saturday) may be linked to promotions or events — worth investigating historical campaign logs
- Weekday underperformance (especially Monday–Thursday) opens opportunities for:
> - Bundling promos
> -“Happy Hour” discounts
> - Loyalty point boosts during off-peak days
- Low average spend per transaction highlights a need for menu upselling, such as:
> -Add-on prompts (e.g., “Add +Stevia?”)
> -Bundle meals or combo packs

---

## 📸 Dashboard Screenshot

*(See below for a snapshot of the Power BI dashboard)*  
⬇️  
![Sales Overview Dashboard](../outputs/Justy_Cafe_Dashboard_page-01.jpg)
