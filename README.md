# Super-Store-Sales-Dashboard
- The Super Store Sales Dashboard is a comprehensive tool focusing on five main sections: Sales Analysis, Product Analysis, Shipping Analysis, Customer Order Tracker and Sales Forecast.

## Table of Content
- [Problem Statement](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#problem-statement)
- [Tools Used](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#tools-used)
- [Data Source](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#data-source)
- [Data Preparation](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#data-preparation)
- [DAX Codes](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#dax-codes)
- [Dashboards](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#dashboards)
- [Insights](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/edit/main/README.md#insights)

## Problem Statement
Build a Super Store Sales Analytics Dashboard, Product Analysis Dashboard, Shipping Analysis Dashboard, Customer Order Tracker Dashboard and Sales Forecast Dashboard.

## Tools Used
Microsoft Power BI

## Data Source
HR Aanlytics Dataset: https://public.tableau.com/app/sample-data/sample_-_superstore.xls

## Data Preparation
After importing the csv file `superstore_sales`, cleaned the data in the power query.

Dataset contains `3` tables namely `Orders`, `Returns` and `People`; `21 columns` and `9994 rows`.
- The headers were promoted.
- Data types were adjusted.
 
## DAX Codes

### Measures Used:
- Total Orders = `COUNTROWS('Orders')`
- Total Products Returned = 
  `COUNTROWS(
      FILTER(
          Returns,
          Returns[Returned] = "Yes"
      )
  )` 

### Columns used:
- Average Delivery Duration = `DATEDIFF('Orders'[Order Date], Orders[Ship Date], DAY)`
  
## Dashboards

### Sales Analysis:
- The `Total Sales` and `Total Profit` of the company from 2014 to 2017 stand at `$2.3 Million` and `$286 Thousand` respectively. 
- The YoY monthly sales increased from 2014 to 2017.
- The company sold worth `38 Thousand` units of products.
- Products were delivered with an average of `4` days.
- `Phones` and `Chairs` were the highest-selling items.
- `51%` of products were sold to the `Consumer` segment, followed by `31%` to the `Corporate` segment and `19%` to the `Home Office` segment.
  
![1](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/assets/163330089/3b426ace-f03d-4863-9e1b-8b9f28016622)

### Product Analysis:
- The highest number of products were sold from the `Technology` category.
- `Office Supplies` were among the highest selling products.
- `Binders` were given the highest discount.
- `8%` of the total products ordered were returned.

![2](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/assets/163330089/0b08995b-36f3-48c1-b9f9-38f83c1dfbb6)

### Shipping Analysis:
- `Office Supplies` were highly shipped.
- The highest number of shipping were done through `Standard` mode at `60.19%`.

![3](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/assets/163330089/8bb5d059-9c85-420c-ae90-276991ec2ce2)

### Forecast:
- The sales forecast analysis dashboard shows the forecast for the next 15 days.

![4](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/assets/163330089/152d7091-9b90-462d-8001-cf5ee4e93cc2)

### Customer Order Tracker:
- This dashboard shows the Customer order tracker.
- It provides details about customers' product purchases, order dates, shipping dates, along with the other product details.

![5](https://github.com/gargie-anand/Super-Store-Sales-Dashboard/assets/163330089/c4d57cf0-ad15-429f-bec4-a6d673d7c2ea)

## Insights
- The sales analysis dashboard reveals strong sales growth and effective management of product sales and delivery operations over the years.
- Focusing on top-selling products and understanding customer segments can drive revenue growth and optimize resource allocation.
- Optimizing delivery processes, with an average delivery time of 4 days, enhances customer satisfaction and supports long-term profitability.
- Leveraging these insights to refine sales strategies and streamline operations will sustain growth and achieve greater success in the future.
