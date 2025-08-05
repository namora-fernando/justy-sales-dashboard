
# 🧃 Dashboard 2: Top-Selling Menus – Key Findings  
> **Date range**: July 2025  
> **Data source**: 1027 rows from Table #2 (`Penjualan Menu per Hari`)

---

## 🧮 Key Measures Used:
```DAX
Total Revenue Menus = SUM('Penjualan Menu per Hari'[Revenue])
Total Units Sold = SUM('Penjualan Menu per Hari'[Jumlah Terjual])
```

---

## 🔍 Key Observations
- **Most sold item** was _Alpukat (Blenger)_ with **77 units**, followed closely by _Alpukat (Puas)_, _Jambu Merah (Blenger)_, and _Refreshing Juice (Blenger)_.
→ These four dominated both in terms of volume and revenue, indicating strong consumer preference for rich, creamy juice flavors.
- **Top revenue contributor** was also **Alpukat (Blenger)** with over **Rp1.5M** in sales, contributing over 12% of total monthly menu revenue
→ High performance in both quantity and price signals **strong demand elasticity**
- **Juice category** dominates with **87%+* of total revenue
→ Juice is the café’s flagship product line
- Items like **Dimsum** generate decent revenue despite lower units sold
→ Indicates higher price point, suitable for **entry-level** or **bundling**
- Overall sales: **764 units**, **Rp12.816M** revenue → average menu item = ~Rp16.7K
→ Lower than average basket value (from Dashboard 1), implying **multiple items per transaction**

---

## 💡Business Implications
- **Alpukat** (Avocado) menus are the hero products — consider:
> - Premium line (“Signature Alpukat” series)
> - Seasonal variants (mix-ins, toppings)
- **Underperforming items** like Air Mineral or Telur Gulung need re-evaluation — are they:
> - Add-ons with niche purpose?
> - Poorly positioned in menu layout?
- **Overdependence on Juice** (87% revenue) poses both **risk and opportunity**:
> - Risk: lack of diversification
> - Opportunity: apply same product strategy to grow Extra / Board Game items
- Price optimization opportunity for items with high unit sales but modest revenue
→ Possibly underpriced or under-promoted
- Recommend **menu board redesign** and **cashier suggestions** to guide toward margin-positive items

---

## 🧼 Filtering Notes
To ensure clarity, the following item types were excluded:
> Modifiers such as `No Ice`, `Less Sugar`, `Less Ice`, etc.
> → These entries typically represent **preparation preferences**, not standalone items, and are typically priced at Rp0.

---

## ⚠️ Data Quality Note
One anomaly spotted: A **Take Away Sirsak** transaction recorded **0 revenue**, which is likely a **manual POS input error**
→ Suggest periodic checks or validation rules to maintain data hygiene

---

## 📸 Dashboard Screenshot

*(See below for a snapshot of the Power BI dashboard)*  
⬇️  
![Top Selling Menus Dashboard]( https://github.com/namora-fernando/justy-sales-dashboard/blob/main/outputs/top_menus.jpg)
