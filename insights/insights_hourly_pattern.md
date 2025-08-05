# ⏰ Dashboard 3: Hourly Pattern – Key Findings  
> **Date range**: July 2025  
> **Data source**: Aggregated hourly-level data from Table #3 (Penjualan Menu per Jam), cleaned of non-revenue-generating modifiers (e.g., Gula, Es, Penyaringan)

---

## 🧮 Key Measures Used:
```DAX
Total Revenue Hourly = SUM('Penjualan Menu per Jam'[Penjualan])
Total Transactions Hourly = SUM('Penjualan Menu per Jam'[Jumlah Transaksi])
Total Units Sold Hourly = SUM('Penjualan Menu per Jam'[Jumlah Terjual])
```

---

## 🔍 Key Observations:
- **Highest revenue** occurred during **7–8 PM (Rp1.096M)**, marking the most lucrative hour of the day.
- Revenue remains strong between **5–7 PM**, suggesting consistent customer visits post working hours.
- **Most units sold** occurred at **9–10 PM (153 units)**, even though its revenue is slightly lower (Rp0.81M), suggesting high quantity but more affordable menus.
- Morning hours (**11 AM–1 PM**) show very low sales performance, with under **Rp0.1M** and **<15 units sold per hour** — potential operational gap or weak morning demand.
- **Top menus sold** are dominated by variants of **Alpukat**, **Jambu Merah**, and **Refreshing Juice**, further confirming product consistency across all hours.
- Revenue by category shows **Juice** accounts for the vast majority (**>78%**) of total hourly sales — remaining the flagship category throughout the day.

---

## 💡 Business Implications:
- Consider reinforcing promotional campaigns or staff allocation during **5–8 PM**, the key sales window.
- Explore options to boost **late-night monetization** — while 9–10 PM had high volume, its revenue-per-transaction appears lower, offering upselling opportunities.
- Given the crowd surge at **9–10 PM**, potentially influenced by high traffic from a neighboring store open until 11 PM, the café could:
  - **Extend operational hours** slightly beyond 10 PM to fully capture late-night demand
  - **Offer performance bonuses** or shift incentives to motivate staff coverage in this high-volume window
- Evaluate whether current **opening hour at 11 AM** is optimal — low sales in early hours suggest potential to shift resources to better-performing time slots or introduce specific breakfast offerings
- Menu-level targeting (e.g., premiumizing Alpukat menus or offering time-bound combos) could leverage the popularity of bestsellers across time blocks
- Juice category dominance presents brand identity clarity — future product development and marketing can focus around this core offering

---

## 📸 Dashboard Screenshot

*(See below for a snapshot of the Power BI dashboard)*  
⬇️  
![Hourly Pattern Dashboard]( https://github.com/namora-fernando/justy-sales-dashboard/blob/main/outputs/hourly_pattern.jpg)

