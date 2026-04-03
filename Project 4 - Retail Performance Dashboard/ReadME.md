# Retail Performance Dashboard



A multi-page Power BI dashboard built to monitor retail sales performance across a network of 13+ stores in the UK. Designed for area managers and senior leadership to track sales trends, store-level KPIs, and fulfilment performance in real time.



\---



\## Dashboard Pages



\### 1. Area Overview

High-level view of performance across all stores in the area.



\- \*\*Heat map matrix\*\* — week-by-week YoY % variance per store, with conditional formatting (red = underperformance)

\- \*\*Store table\*\* — Sales £, LFL %, LFL LY %, Compound growth, Target, Footfall LFL, Conversion LFL

\- \*\*UK map\*\* — geographic distribution of stores using Bing Maps integration

\- \*\*KPI cards\*\* — Total Sales TY vs Goal, Target vs Goal



\### 2. Store Overview

Drill-down view for individual store performance.



\- \*\*KPI cards\*\* — Sales TY, Sales LY, Target, Projected, VAR £/%, Compound growth

\- \*\*LFL benchmarks\*\* — Store LFL vs Location, City, and Area averages

\- \*\*Footfall \& Conversion\*\* — Store vs Location, City, and Area benchmarks

\- \*\*Weekly line chart\*\* — Store / Area / City LFL % trends over time

\- \*\*Sales by Quarter\*\* — bar chart showing quarterly performance



\### 3. Fulfilment

Tracks online order fulfilment performance per store.



\- \*\*Gauge charts\*\* — Click \& Collect and Shipped completion rates

\- \*\*KPI cards\*\* — LFL Inc/Exc, Fulfilment TY/LY, Penetration TY/LY, VAR £/%

\- \*\*Dual-axis weekly chart\*\* — Fulfilment value (bars) vs Completion % (line)



\---



\## Key Technical Features



\### DAX Measures

\- \*\*LFL (Like-for-Like)\*\* — year-on-year sales comparison, with organic store classification logic to exclude new/closed stores from the base

\- \*\*Organic filter\*\* — custom slicer using a disconnected table to toggle organic vs all-store views without breaking filter context across pages

\- \*\*SALES LY with filter isolation\*\* — uses `REMOVEFILTERS` and `VAR CurrentStores = VALUES()` to correctly scope prior year comparisons

\- \*\*Projected sales\*\* — forward-looking measure based on current run rate

\- \*\*Compound growth\*\* — multi-year CAGR calculation per store

\- \*\*Benchmarking measures\*\* — Location, City, and Area LFL aggregations for contextual comparison



\### Data Model

\- `fact\_sales` (many) → `store\_detail` (one) via `store\_no`

\- Week-based time axis using `fact\_sales\[week]` — no date table required

\- Organic classification handled via `store\_detail` attributes



\### Design

\- Dark theme with gold/amber accent palette — consistent across all 3 pages

\- 8 slicers: Store, City, Week, Quarter, Organic, Location, Month, Year

\- Conditional formatting on heat map and KPI cards

\- Dual-axis charts for fulfilment page



\---



\## Tools \& Skills



| Tool | Usage |

|------|-------|

| Power BI Desktop | Report build, data model, visualisations |

| DAX | All measures — LFL, YoY, Compound, Projected, Benchmarks |

| Power Query | Data transformation and source connection |

| Bing Maps | Store geography visual |



\---



\## Background



Built using real-world retail operations data structures, informed by 10+ years of multi-site retail management experience. The dashboard replicates the kind of area-level performance reporting used in large UK retail networks, with a focus on actionable insight at both area and store level.



\---



\## Screenshots



> \*(Add screenshots of each page here)\*



!\[Area Overview](Screenshots/Dashboard_1.png)

!\[Store Overview](Screenshots/Dashboard_2.png)

!\[Fulfilment](Screenshots/Dashboard_3.png)



