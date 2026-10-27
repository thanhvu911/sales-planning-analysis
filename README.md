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

- **Facts:** Sales (about 58K transaction lines) and Plan (monthly targets)
- **Dimensions:** Store, Product, Category, Customer, Promotion, Date

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

<img src="https://github.com/user-attachments/assets/fbd4701f-b4f5-4039-847d-b2f5f0c1134b" alt="Power BI dashboard page 1" width="900"/>

<img src="https://github.com/user-attachments/assets/3b11928f-2851-4abe-a450-519c5c9b93f9" alt="Power BI dashboard page 2" width="900"/>

<img src="https://github.com/user-attachments/assets/208488d4-dd1d-43e6-aec8-1bc94831e94c" alt="Power BI dashboard page 3" width="900"/>

<img src="https://github.com/user-attachments/assets/c1421194-2ab0-415e-aea7-e5bf1489d807" alt="Power BI dashboard page 4" width="900"/>

<img src="https://github.com/user-attachments/assets/e03ece28-1ffe-4901-807a-4fbbb8f48d31" alt="Power BI dashboard page 5" width="900"/>

<img src="https://github.com/user-attachments/assets/001b2c94-db96-4932-b9bd-a573b0ecf010" alt="Power BI dashboard page 6" width="900"/>

## Gallery

_Diagrams are editable in draw.io: [`docs/diagrams/`](docs/diagrams)._

**Data flow: workbook to SQL Server to Power BI**

![Data flow: workbook to SQL Server to Power BI](assets/dataflow.png)

**Galaxy schema: sales and plan facts on shared dimensions**

![Galaxy schema: sales and plan facts on shared dimensions](assets/data-model.png)

**Actual vs. plan revenue**

![Actual vs. plan revenue](assets/insight-actual-vs-plan.png)

**Plan completion by district**

![Plan completion by district](assets/insight-plan-completion-by-district.png)

