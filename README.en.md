
# Sales Dashboard

An interactive two-page sales report built in Power BI.

Overview page

<img width="1963" height="1101" alt="Overview page" src="https://github.com/user-attachments/assets/41738360-b4d3-4150-bb5e-c816e310c3aa" />

Details page

<img width="1954" height="1087" alt="Details page" src="https://github.com/user-attachments/assets/cc879fc2-8485-4cc7-a7a0-d028a0a7f98b" />

Star schema (data model)

<img width="1271" height="874" alt="Star schema data model" src="https://github.com/user-attachments/assets/7a7aef8f-bf5f-4ba3-a668-24252f6406ac" />

## What's inside
- **2 report pages:** *Overview* (KPIs & trends) and *Details* (segments,
  top products, breakdown table).
- **Star-schema data model:** a `sales` fact table linked by one-to-many
  relationships to three dimensions  **Calendar**, **Products** and
  **Regions**. The Regions dimension adds a derived **"Zone"** attribute that
  does not exist in the source data.
- **DAX:** measures (`Margin %`, `Average Order Value`) and calculated tables;
  sort-by-column for correct month ordering.
- **Interactivity:** a slicer to filter the whole report.

## Data
`data/sales.csv` - 3,000 order lines (2024–2025): order date, region, customer
segment, product category & sub-category, quantity, price, discount, sales and
profit. 

## Tools & skills
- **Power BI Desktop** - visuals, two-page report, dashboard design
- **Power Query** - data cleaning, fixing column data types
- **Data modeling** - star schema, one-to-many relationships, dimension enrichment
- **DAX** - measures, calculated tables, sort-by-column
- KPI cards, time series, bar / donut charts, tables, conditional formatting, slicers
- Choosing the right aggregation and data storytelling

## Key findings
**Totals:** revenue **3.47M**, profit **560K** (~16% margin), **3,000** orders,
average order value **~1.2K**.

1. **Seasonality** - revenue peaks in November–December and dips in summer.
   --> *Plan inventory and staffing for Q4 in advance.*
2. **Top revenue category - Technology** (~63%), despite fewer orders; Office
   Supplies has many orders but little money.
   --> *Focus on high-margin categories.*
3. **High revenue ≠ high margin** - top sellers (Laptops, Phones) yield only
   ~12-13% margin, while small office supplies (Paper, Art) reach ~39%.
   --> *Revisit pricing and product mix.*
4. **Regional concentration** - Central ≈ 40% of revenue, Siberia ≈ 5%.
   --> *Dependency risk on one region + growth opportunity.*
5. **Discounts erode profit** - average profit per order turns **negative at 30%**
   discount.
   --> *Cap the maximum discount at ~20%.*
