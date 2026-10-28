# Zomato Order & Restaurant Analysis (Power BI & Excel)

##  Project Overview

This project provides an end-to-end data analysis solution for **Zomato's restaurant operations and ordering behavior**. By combining **Excel Data Processing & Cleaning** with **Power BI Visual Analytics**, raw ordering and geographical data were transformed into actionable business insights.

The interactive Power BI dashboard helps analyze customer preferences, pricing impacts, order trends over time, and location-based performance to drive strategic decision-making in the food delivery ecosystem.

##  Key Business Objectives & Insights

* **Revenue Metrics:** Tracked **?15.57M** in total revenue generated across **15,000 orders** and **500 restaurants**.

* **Geographical Demand:** Evaluated restaurant density vs. order volume across major metro cities (Bangalore, Mumbai, Delhi, Kolkata, Chennai).

* **Customer Behavior:** Analyzed order patterns across pricing tiers (Low, Medium, High) and tracked overall customer ratings (Average: **3.00**).

* **Time Series Trends:** Monitored order volume fluctuations throughout 2024 to identify seasonal spikes and peak ordering windows.

##  Tech Stack & Tools Used

* **Data Cleaning & Processing:** Microsoft Excel (Data Cleaning, Formatting, Aggregation)

* **Data Transformation & Modeling:** Power Query (Power BI)

* **Data Visualization & Analytics:** Power BI Desktop (DAX Calculations, Interactive Dashboards, Map Visuals)

##  Repository Structure

```
Data/
Zomato_Orders.csv          # Raw order-level data
Zomato_Restaurants.csv     # Raw restaurant-level data
README.md                  # Project documentation

```

##  Workflow & Implementation

### 1. Data Cleaning & Transformation (Microsoft Excel)

Duplicate Removal & Null Handling:** Identified and removed duplicate rows while filling or handling missing values in order dates, costs, and customer ratings.

Data Merging: Combined `Zomato_Orders` and `Zomato_Restaurants` datasets 

Calculations: Calculated total restaurant sales, average order values per city, and restaurant density stats directly within Excel prior to importing into Power BI.

* **Data Export:** Saved the final processed dataset into `Zomato_Transformed.xlsx`.

 2. Power BI Data Modeling & DAX

* Imported cleaned Excel sheets into Power BI and verified data types using **Power Query Editor**.

* Established a **1:N (One-to-Many)** relationship using `restaurant_id` between `Zomato_Restaurants` and `Zomato_Orders`.

* Developed custom DAX metrics:

  * **Total Revenue:** `SUM(Zomato_Orders[total_cost])`

  * **Total Orders:** `COUNT(Zomato_Orders[order_id])`

  * **Average Order Value (AOV):** `AVERAGE(Zomato_Orders[total_cost])`

  * **Average Rating:** `AVERAGE(Zomato_Restaurants[avg_rating])`

### 3. Interactive Dashboards Overview

The report is split into distinct visual pages:

* **Executive Highlights Dashboard:** Displays high-level KPI cards, timeline metric distributions, order breakdowns by city, and top 5 revenue-generating restaurants.

* **Geographic Revenue & Area Analysis:** Features map visualizations and waterfall charts detailing city-wise order densities across specified zones (`Area_A` through `Area_E`).

##  Key Visual Insights Highlights

| Dashboard View | Description | 
| ----- | ----- | 
| **KPI Cards** | Quick snapshot of Total Revenue (\$15.57M), Total Orders (15K), Restaurants (500), and Avg Rating (3.00). | 
| **Timeline Metrics** | Line plot showing daily/monthly trends in order costs throughout 2024. | 
| **Order Breakdown by City** | Detailed tabular view breakdown by City, Order Count, AOV, and Price Tiers. | 
| **Geographic Breakdown** | Interactive map plot and pie-chart breakdowns across Areas A, B, C, D, and E. | 

## How to Replicate This Project

1. **Clone the repository:**

   ```
   git clone https://github.com/your-username/zomato-analysis-powerbi.git
   
   ```

2. **Open Processed Data:**

   * Check `Data/Zomato_Transformed.xlsx` for cleaned records and formulas used in Excel.

3. **Open Power BI Dashboard:**

   * Open `Reports/Zomato Business Insights.pbix` using **Power BI Desktop**.

   * Update the file path to point to your local `.xlsx` file if prompted.

##  Author

* **R.Yesodha** 



