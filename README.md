# Olist E-Commerce Sales Dashboard (Power BI)

An interactive Power BI dashboard analyzing ~100k orders from **Olist**, the largest department store marketplace in Brazil (2016–2018). It covers revenue, order volume, delivery time, product categories, payment methods and geographic distribution.

## Dataset

- **Source:** [Brazilian E-Commerce Public Dataset by Olist, on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Provider:** Olist
- **License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
- **Period:** September 2016 to October 2018
- **Size:** ~100k orders across 9 CSV files

The raw CSV files are **not included** in this repository because of their size. To reproduce the report, download the dataset from Kaggle and extract it into an `archive/` folder at the project root.

## Dashboard: E-Commerce Overview

| Visual | What it shows |
|---|---|
| KPI cards | Total Revenue, Total Orders, Avg Order Value, Avg Delivery Days |
| Line chart | Monthly revenue trend |
| Bar chart | Revenue by product category (translated to English) |
| Donut chart | Order payments by payment type |
| Map | Revenue and average delivery days by customer state |

## Data Model

A star schema built in Power BI with these tables:

- **Fact tables:** `olist_orders_dataset`, `olist_order_items_dataset`, `olist_order_payments_dataset`
- **Dimension tables:** `olist_customers_dataset`, `olist_products_dataset`, `product_category_name_translation`, `Dim_Date`
- **Measures table:** `_Measures` holds all DAX measures

## Tools

- Power BI Desktop
- Power Query for data cleaning and transformation
- DAX for measures

## Project Structure

```
.
├── Olist Power BI Project.pbix   # Power BI report
├── README.md
└── archive/                      # Raw CSVs (not tracked, download from Kaggle)
```

## How to Use

1. Install [Power BI Desktop](https://www.microsoft.com/power-bi/desktop) (free, Windows).
2. Download this repository.
3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) and extract the CSVs into `archive/`.
4. Open `Olist Power BI Project.pbix`. If Power BI asks, update the data source paths under **Transform data > Data source settings**.

## Acknowledgements

The data was made available by [Olist](https://olist.com/) on Kaggle. All credit for the data goes to them.
