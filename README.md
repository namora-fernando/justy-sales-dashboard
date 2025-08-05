# Justy Juice Café & Boardgame – Sales Dashboard (Power BI)

This is a business intelligence project built using Power BI, based on real sales transaction data from a café business in Bekasi (July 2025). The dashboard was created to evaluate operational performance using real transaction records (with permission) from the café. The café primarily sells juice, with additional snack items and rentable board games.

---

## 📊 Dashboard Features

This dashboard includes:

-	📈 **Sales Overview**: Daily transaction count and total revenue
-	🧃 **Top-Selling Menus**: Top most sold items by category and sales
-	🕒 **Hourly Pattern**: Most active sales hours throughout the day
-	🛍️ **Sales Channel Analysis**: Performance comparison across Online, Take Away, and Dine In

---

## Tools & Technologies 🛠️:

-	Power BI Desktop
-	Microsoft Excel (for data preprocessing and VBA macro work)
-	Git & GitHub (for version control and documentation)

---

## 🔄 Data Cleaning & Transformation

**Table #1 (Laporan Penjualan)**

-	Removed unused columns: `Bill_Number`, `Perusahaan`, `Brand`, `Cabang`, `Waiter`, `Cashier`, `Table`, `Diskon_Menu`, `Diskon_Nota`, `Service_Charge_Total`, `Pajak_Total`, `Biaya_Pengiriman`, `Biaya_Pemesanan`, and `Rounding_Total`.
-	Dropped `Net_Sales` and `Grand_Total` columns and used `Subtotal` instead, as all values were identical
-	Filtered out rows with `Sales_Type = 'Void Sales'` since these represent canceled transactions
-	Created a calculated column `Day_Name` using DAX:
> -	Translates `Sales_In_Date` into the corresponding weekday (e.g., Monday, Tuesday) for trend aggregation
-	Created a new column `Total_Final` to represent actual transaction revenue:
> -	For *Online* transactions, `Subtotal` is always 0 — this was intentionally designed during system setup to separate online financials
> -	As co-founder of the café, I implemented this logic to streamline reporting across sales channels
> -	Therefore, a custom DAX was written to replace `Subtotal` for Online using item-level breakdowns from Table #4 and pricing reference from Table #5 (Master Harga) (Master Harga)

**Table #2 (Penjualan Menu per Hari)**

-	Removed unused columns `Cabang`, `Cogs`, `Penjualan`, and `Margin`
-	Retained `Harga` and `Jumlah Terjual` for further analysis
-	Created a new calculated column `Revenue`:
> -	For **Online** transactions (where `Harga = 0`), unit prices were retrieved from Table #5 using the `LOOKUPVALUE` DAX function
> -	For other transactions type, `Revenue` is calculated using `Harga x Jumlah Terjual` directly from Table #2

**Table #3 (Penjualan Menu per Jam)**

-	Removed unused columns `Cabang`, `Cogs`, `Penjualan`, and `Margin`
-	Used only for hourly pattern visualization
-	Grouped by `Menu` and `Waktu` (hour range) during data extraction
-	Did not include a numeric time sorting column, so a separate dimension table (`Dim_Waktu`) was created to enable proper sorting of `Waktu`

**Table #4 (Detail Transaksi)**

-	Joined with Table #1 using `No_Transaksi` as the primary key
-	One-to-many relationship, as each transaction in Table #1 can contain multiple item rows in Table #4
-	Used Table #5 to retrieve accurate `Harga_Satuan` for Online transactions with default price of `0`

**Table #5 (Master Harga)**

-	Created manually in Excel based on the café’s internal price list
-	Contains unique menu names and corresponding unit prices
-	Connected with many tables via `Menu` column (one-to-many relationship)

**Table #6 (Dim_Waktu)**

-	Created as a separate dimension table to enable proper hourly sorting of text-based time ranges (e.g., “11:00-11:59”)
-	Contains two columns:
> -	`Waktu`: categorical time range label used as X-axis
> -	`Hour_Sort`: numeric column used for chronological sorting
-	Linked to Table #3 (`Penjualan Menu per Jam`) via `Waktu` (one-to-many relationship)

---

## Folder Structure📦

📁 pbix/
└── Justy_Cafe_Dashboard.pbix

📁 outputs/
├── sales_overview
└── top_menus
└── hourly_pattern
└── sales_channel
> _(both pdf and jpg versions)_

📁 insights/
├── insights_sales_overview.md
└── insights_top_selling_menus.md
└── insights_hourly_pattern.md
└── insights_sales_channel_analysis.md

📁 data_raw/
└── Transaksi_Juli_2025.xlsx

README.md

---

## Notes📌

This project was developed as part of a self-initiated business analytics portfolio.  
All data are used with permission and handled to avoid disclosing sensitive financial performance.
