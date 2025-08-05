# 🛍️ Dashboard 4: Sales Channel Analysis – Key Findings  
> **Date range**: July 2025  
> **Data source**: Table #1 (`Laporan Penjualan`) – 381 valid transactions (excluding void sales)

---

## 🧮 Key Measures Used:
> All DAX key measures that already created on Sales Overview Dashboard
```DAX
Total Revenue = SUM('Laporan Penjualan'[Total_Final])
Total Transactions = COUNTROWS('Laporan Penjualan')
Average Transaction Value = DIVIDE([Total Revenue], [Total Transactions])
```

---

## 🔍 Key Observations:
- **Online** remains the **top-performing channel**, generating **Rp6.098M revenue** from **168 transactions** (44% of total), despite many values being manually reconstructed due to POS setup.
- **Dine In** and **Take Away** contributed **Rp3.76M** and **Rp3.084M** respectively, with 123 and 90 transactions.
- **Average transaction value** across all channels is **Rp33.97K**, but a breakdown by channel shows:
  - **Online** revenue per transaction appears lower due to heavy promo or discounted items
  - **Dine In** may involve higher spend per visit, likely due to customer comfort or bundled items.
- **Saturday and Sunday** are peak revenue days across all channels — **Saturday especially strong on Dine In and Online.**
- **Monday** shows lowest engagement across all metrics (revenue and volume) — indicating potential operational lull.
- **Online** channel performs consistently throughout the week, unlike **Dine In** or **Take Away**, which fluctuate rapidly.

---

## 💡 Business Implications:
- **Online is clearly the strongest contributor**, but requires **accurate pricing input and tracking**, especially since café’s internal rule sets Online `Subtotal = 0`. Ensure proper validation to maintain future data quality.
- Given the **weekend surge**, especially in **Dine In**, the café could:
  - Launch **weekend dine-in bundles** or **in-store event promos**
  - Reinforce staffing or inventory prep on high-volume days
- **Take Away** seems underperforming compared to other modes — opportunities include:
  - Promoting quick grab-and-go sets
  - Collaborating with external food delivery platforms (if not already done)
- **Monday gap** suggests opportunity to introduce:
  - “Start of Week” promo
  - Loyalty punch cards with weekday bonuses
- Visual share chart shows that **Online contributes nearly half of revenue** — this over-reliance can be:
  - **A strength**, if leveraged well via targeted online campaigns or mobile ordering systems
  - **A risk**, if platform fees, input errors, or promo saturation reduce margins — this requires margin analysis beyond revenue

---

## 📸 Dashboard Screenshot

*(See below for a snapshot of the Power BI dashboard)*  
⬇️  
![Sales Channel Analysis Dashboard]( https://github.com/namora-fernando/justy-sales-dashboard/blob/main/outputs/sales_channel.jpg)
