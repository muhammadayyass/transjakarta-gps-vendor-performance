# GPS Fleet Vendor Performance & Data Integrity Analytics
### Industry Placement Case Study — PT TransJakarta (in partnership with PPKD Jakarta Selatan & JakLingko)

> **Note on confidentiality:** This project was completed as part of a supervised industry placement using PT TransJakarta's internal operational data. Vendor names, the underlying dataset, and the full dashboard file are not published here out of respect for that confidentiality. This page describes the **methodology, technical approach, and skills demonstrated**

## Business Problem
TransJakarta's fleet-tracking system depends on GPS data delivered by multiple third-party vendors under contractual Service Level Agreements (SLAs). When passengers see inaccurate real-time bus locations, it's historically been unclear whether the root cause is network infrastructure, vendor hardware, or specific vendor-operator combinations — evaluations tended to rely on anecdote rather than evidence.

## Approach
- Designed a **Star Schema** data model and **Power Query (M-Code)** ETL pipeline to transform raw GPS telemetry logs into analysis-ready fact and dimension tables
- Built **Advanced DAX measures** using `REMOVEFILTERS` and `ALL` to control filter context, enabling apples-to-apples comparisons between vendor categories regardless of which dashboard filter was active
- Applied **Pareto/Top-N filtering** on scatter plots and heatmaps to focus executive attention on the highest-impact vendors and routes rather than overwhelming the dashboard with every data point
- Ran a **Kruskal-Wallis non-parametric statistical test** to determine, rather than assume, whether delay differences were statistically attributable to specific vendor-fleet interactions
- Cross-referenced performance data against a calendar of national events to separate genuine vendor underperformance from external network-load effects (e.g. public holidays)

## Key Skills Demonstrated
- End-to-end BI pipeline ownership: ETL → data modeling → advanced DAX → executive dashboard design
- Data-integrity auditing: identifying a multi-month vendor data-corruption incident that had gone undetected
- Statistical rigor: using hypothesis testing instead of anecdotal evaluation to support contractual/vendor-management decisions
- Translating a technical data problem ("missing GPS signal") into a business-risk framing (financial/payment exposure) that resonates with non-technical stakeholders
- Authored a structured, literature-grounded recommendation framework (drawing on U.S. Transportation Research Board / TCRP transit-performance standards) covering contract structure, monitoring cadence, and automated data-quality auditing

## Outcome
Presented directly to TransJakarta's Data and HR teams as part of the placement's final deliverable, with strong reception.

## Limitations
Because the underlying dataset and specific findings are confidential to this placement, this write-up necessarily omits quantitative detail that would otherwise strengthen the case for reproducibility — happy to discuss the full findings and methodology in an interview setting.

---
**Author:** Muhammad Yahya Ayyasy — [LinkedIn](https://linkedin.com/in/muhammadayyass) · muhammadayyas22@gmail.com
