# 🍕 Interactive Pizza Sales Dashboard (Power BI)

<table>
  <tr>
    <td width="50%"><img src="https://github.com/user-attachments/assets/8c8f38fe-7747-40f1-9074-3959acb4fd11" alt="Home View"></td>
    <td width="50%"><img src="https://github.com/user-attachments/assets/b0847f17-0c31-4d18-adbc-3c051bd1a067" alt="Pizza Detail View"></td>
  </tr>
</table>

## 📌 Project Overview

This project features an interactive sales dashboard for a fictional pizza restaurant, analyzing a full year of sales data from 2015. For many restaurant owners, sales data is often recorded but rarely analyzed, leading to decisions based on gut-feel rather than concrete evidence. This Power BI dashboard solves that problem by transforming raw transaction data into a centralized, easy-to-understand tool that reveals key patterns and insights at a glance.

The dashboard is built for a **restaurant owner or manager** to quickly answer critical business questions and make informed, data-driven decisions to improve profitability and efficiency. For example, a manager can:

* **Optimize Staffing & Operations:** Instantly identify the busiest days (**Friday**) and months (**July**) to optimize staff scheduling and prepare for peak periods.
* **Improve Inventory Management:** Understand which pizza categories (`Classic`) and sizes (`Large`) are the most popular, ensuring key ingredients for these items are always in stock while reducing waste.
* **Drive Menu Engineering:** Analyze the most and least profitable/popular pizzas to make strategic decisions, such as promoting a best-seller like the "Thai Chicken Pizza" or considering the removal of an underperformer like the "Brie Carre Pizza."
* **Create Targeted Marketing:** Use insights on customer preferences to launch effective marketing campaigns, such as a special offer on the most frequently ordered pizza combinations.

## 💡 Key Business Questions & Insights

This dashboard answers critical questions about the restaurant's performance and provides the following key insights:

1.  **Overall Performance:** The business generated **$817.9K in total revenue** from **49.6K pizzas sold** across **21.35K total orders** in 2015.
2.  **Peak Periods:** The busiest day of the week for orders is consistently **Friday**. On a monthly basis, sales peaked in **July**.
3.  **Top Sellers:** The **'Classic'** category is the undisputed leader, driving the highest number of sales and a significant portion of revenue. By size, the **'Large'** pizza contributes the most to total revenue (over 45%).
4.  **Menu Opportunities:** The **'Thai Chicken Pizza'** is one of the most profitable items, making it an ideal candidate for promotion. Conversely, the **'Brie Carre Pizza'** is among the worst-selling items, presenting an opportunity for menu optimization.

## 🛠️ Technical Skills & Tools Used

This project was developed end-to-end using **Microsoft Power BI**, showcasing skills in data cleaning, data modeling, and DAX.

### 1. Data Transformation and Modeling
* **Data Source:** The project utilizes the [Pizza Sales Dataset from Kaggle](https://www.kaggle.com/datasets/nextmillionaire/pizza-sales-dataset).
* **Data Normalization (Star Schema):** Recognizing that the initial flat-file dataset was denormalized and redundant, it was transformed into a proper **Star Schema**. This involved creating several Dimension Tables from the main data, `Dim_Pizza_Category` with power query and, `Dim_Date` with dax, leaving a clean Fact Table (`Fact_Sales`) at the center. This optimized model reduces redundancy and improves report performance.
* 
<table>
  <tr>
    <td width="50%">
      <img src="https://github.com/user-attachments/assets/e5e21a10-31bc-448d-923c-f35301e08908" alt="Creating Pizza Category Dimension in Power Query">
      <p align="center">Creating Dim_Pizza_Category in Power Query</p>
    </td>
    <td width="50%">
      <img src="https://github.com/user-attachments/assets/a7e6f46d-2615-4d79-af7c-59ba016bef26" alt="Data Model Star Schema">
      <p align="center">Data Model - Star Schema</p>
    </td>
  </tr>
</table>


### 2. DAX (Data Analysis Expressions)
All key performance indicators (KPIs) were written as custom measures using DAX. The primary measures include:

```DAX```

```Average Order Value = SUM(fact_pizza_sales[total_price]) / DISTINCTCOUNT(fact_pizza_sales[order_id]) -- Calculates the average number of pizzas sold per unique order```

```Average Pizza Per-Order = SUM(fact_pizza_sales[quantity]) / DISTINCTCOUNT(fact_pizza_sales[order_id]) ```


## 🎨 Report Design and Interactivity

The report was designed with a focus on user experience, featuring a custom, on-brand theme and a high degree of interactivity.

![power bi pizza sales](https://github.com/user-attachments/assets/9e23a591-e434-4283-8c86-cc2b0c63dd6d)

* **Dynamic Views with Bookmarks:** **Bookmarks** and buttons are used to show and hide different sets of visuals, allowing the user to switch between a "Home" overview and a "Pizza Detail" view without leaving the page.
* **Custom Theme:** A custom report theme was developed using a pizza-inspired color palette (yellows, reds, oranges) to create a visually appealing experience.
* **Filtering:** Interactive **Slicers** for "Month" and "Pizza Category" allow users to easily drill down and explore the data.

## 📂 Report Structure

The report uses a single-page design for a seamless user experience, with bookmarks used to navigate between two main views:

* **Home View:** Presents a high-level summary of all key performance indicators and overall sales trends.
* **Pizza Detail View:** Offers a granular look at individual pizza performance to support menu engineering decisions.

## 🚀 How to Use

This report is designed for local viewing using Power BI Desktop.

**Prerequisites:**
* You must have **Microsoft Power BI Desktop** installed on your machine.

**Instructions:**
1.  Clone or download this repository to your local machine.
2.  Open the `.pbix` project file in Power BI Desktop.
3.  To navigate between the "Home" and "Pizza Detail" views, **hold down the CTRL key and click** the navigation buttons at the top of the report.

## 👤 Contact

* **Author:** Adam Astiti
* **LinkedIn:** [linkedin.com/in/adam-astiti-a3787312a/](https://www.linkedin.com/in/adam-astiti-a3787312a/)
* **GitHub:** [github.com/adam-astiti](https://github.com/adam-astiti)
