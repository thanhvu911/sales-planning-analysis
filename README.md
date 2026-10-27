# Sales Planning Analysis (Power BI · Galaxy Schema)

A Power BI dashboard (Aug 2025) for the KPIM Mart retail chain that compares **actual sales against monthly plans** by store, product group, region, and time, so managers can see who is on track and where targets are at risk.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-742774?style=flat)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat&logo=microsoftsqlserver&logoColor=white)

## Business questions
- Which stores, regions, and product groups are meeting their monthly plan, and which are falling behind?
- How is performance trending year over year and over the last 12 months?

## Data model: galaxy schema
Two fact tables share conformed dimensions, so actual and planned figures can be compared at any grain:

- **Facts:** `fact_sales` (about 58K transaction lines) and `fact_sales_plan` (monthly targets by district)
- **Dimensions:** `dim_customer`, `dim_product`, `dim_promotion`, `dim_store`, `dim_date`, joined on surrogate keys (`customer_key`, `product_key`, `promotion_key`, `store_key`); the plan fact shares `dim_store` and `dim_date`

## Key measures (DAX)
- Plan completion % = Actual ÷ Plan
- Year-over-year growth %
- Rolling 12-month trend
- Store and region rankings

## Report features
KPI cards · actual-vs-plan monthly trend · store ranking · product-group and regional breakdowns · slicers and drill-through to store detail

## Files
| File | Description |
|---|---|
| `KPIM Mart Sales Report Datathon 3.pbix` | Main report |
| `Capstone Project.pbix` | Extended version of the report |
| `KPIM Mart Data.xlsx` | Source data and data dictionary |

## How to open
Open either `.pbix` file in Power BI Desktop. If prompted, point the data source to `KPIM Mart Data.xlsx`.

## Skills demonstrated
Galaxy-schema modeling · DAX time intelligence · Power Query data preparation · executive dashboard design

## Power BI dashboard

### Main report (`KPIM Mart Sales Report Datathon 3.pbix`)

**Sales report: this month and year to date vs. last year**

<img src="https://github.com/user-attachments/assets/208488d4-dd1d-43e6-aec8-1bc94831e94c" alt="Sales report page: monthly and year-to-date sales vs. last year" width="900"/>

**Decomposition tree: year-to-date sales by store, brand, loyalty group, income, and promotion**

<img src="https://github.com/user-attachments/assets/c1421194-2ab0-415e-aea7-e5bf1489d807" alt="Decomposition tree of year-to-date sales" width="900"/>

**Sales analysis: sales vs. last year and vs. plan, by district, product, and manager**

<img src="https://github.com/user-attachments/assets/e03ece28-1ffe-4901-807a-4fbbb8f48d31" alt="Sales analysis page: sales vs. last year and plan" width="900"/>

**Detailed analysis: order-level table**

<img src="https://github.com/user-attachments/assets/001b2c94-db96-4932-b9bd-a573b0ecf010" alt="Detailed analysis page: order-level table" width="900"/>

### Extended report (`Capstone Project.pbix`)

**District revenue plan: planned revenue by district, store, and month**

![District revenue plan](assets/powerbi-page-1-district-revenue-plan.png)

**District category table: revenue by district, store, and product category**

![District category table](assets/powerbi-page-2-district-category-table.png)

**Store and manager overview: actual vs. plan by district, store, and manager**

![Store and manager overview](assets/powerbi-page-3-store-manager-overview.png)

**Manager achievement: progress toward plan, growth by store, and monthly trends**

![Manager achievement](assets/powerbi-page-4-manager-achievement.png)

## Gallery

_Diagrams are editable in draw.io: [`docs/diagrams/`](docs/diagrams)._

**Data flow: workbook to SQL Server to Power BI**

![Data flow: workbook to SQL Server to Power BI](assets/dataflow.png)

**Galaxy schema: sales and plan facts on shared dimensions**

![Galaxy schema: sales and plan facts on shared dimensions](assets/data-model.png)

**Power BI Model view (from Power BI Desktop)**

![Power BI Model view](assets/powerbi-data-model.png)

**Actual vs. plan revenue**

![Actual vs. plan revenue](assets/insight-actual-vs-plan.png)

**Plan completion by district**

![Plan completion by district](assets/insight-plan-completion-by-district.png)

