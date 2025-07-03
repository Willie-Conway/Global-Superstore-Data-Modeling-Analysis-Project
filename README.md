# 🌍 Global Super Store: Data Modeling and Analysis Project

## 📊 Overview
This project involves the data modeling and analysis of sales data for the Global Super Store, a fictional company operating in the USA. The goal was to design and implement a relational database, and then use Tableau to create interactive visualizations for analyzing sales performance across various regions, products, and time periods.

In September 2024, I completed the following steps:
- **Data Restructuring**: Transforming raw business data into a structured database. 🗃️
- **Database Implementation**: Building the database schema in MySQL. 🖥️
- **Sales Analysis**: Using Tableau to create visualizations that provide insights into sales performance. 📈

## 🛠️ Project Steps and Breakdown

### Step 1: Create an ER Diagram 📝
The first step was to design the **Entity-Relationship (ER) Diagram** for the database. This diagram identifies the key entities and their relationships within the store's operations.

#### Entities:
- **Orders** 🛍️
- **Customers** 👥
- **Time** ⏱️
- **Location** 🗺️
- **Sales** 💰
- **Products** 🏷️

#### Relationships:
- **Orders** are linked to **Customers** and **Products**.
- Each **Order** has an associated **Shipment**.
- **Sales** are linked to **Products** and **Locations**.

I used **MySQL Workbench** to create the ER diagram and normalized the database schema to the **third normal form (3NF)** for efficiency.

#### ER Diagram🔍 :

![ER Diagram](https://github.com/Willie-Conway/Data-Modeling-and-Analysis-Project/blob/b9cb01d08d75e80f0b60579968585e5a7a16fc38/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/ER%20Diagram.png)


---

### Step 2: Implement the Data Model 🛠️
Once the ER diagram was designed, the next step was to implement the data model in **MySQL Workbench**.

#### Steps:
1. **Forward Engineer**: Export the schema to MySQL and create the necessary tables. 💾
2. **SQL Execution**: Execute the SQL script to generate the database on the live server. 📜

The database schema was successfully created, and data could be imported and analyzed.

#### New Database Schema🔧:

![Data Model](https://github.com/Willie-Conway/Data-Modeling-and-Analysis-Project/blob/e45ff7c59a5656bdafc3684bd06aad7cd495aadd/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/Screenshot%202024-09-22%20225420.png)

---

### Step 3: Create a Star Schema ⭐
To facilitate efficient querying and analysis, I implemented a **Star Schema** for the sales data. This schema is designed to support dimensional analysis across key business metrics.

#### Components:
- **Fact Table**: `Sales` (stores total sales, profit, etc.) 💵
- **Dimension Tables**:
  - `Product`: Details about the products. 🏷️
  - `Location`: Information about geographical regions (City, State, Country). 📍
  - `Time`: Time-related information (Year, Quarter, Month). 📅

This schema allowed for efficient aggregation and analysis, particularly focused on sales performance by **Product**, **Location**, and **Time**.

#### Star Schema Diagram Example🌟:
![Star Schema](https://github.com/Willie-Conway/Global-Superstore-Data-Modeling-Analysis/blob/2b678605cf36461f2b8e92a4d25d9c09748973cf/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/Star%20Schema%20Diagram.png)

---

### Step 4: Create a Map Chart in Tableau 🗺️
The first interactive visualization was a **Map Chart** showing the sales performance across different states in the USA.

#### Steps:
1. Drag the **Country** field to the filter card (select USA). 🇺🇸
2. Place **State** and **Sales** into the **Detail** and **Color** sections, respectively. 🎨

This map chart gave a visual representation of sales distribution across states, highlighting regions with higher or lower performance.

#### Map Chart🌍:

![Map chart](https://github.com/Willie-Conway/Data-Modeling-and-Analysis-Project/blob/fb93b9f509e02ae3d1b09d69860fd745197bb707/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/Screenshot%202024-09-22%20223609.png)


---

### Step 5: Create a Bubble Chart in Tableau 🟠
Next, I created a **Bubble Chart** to visualize **profits by state**, with additional details like **quantity sold** and **shipping costs** displayed dynamically.

#### Steps:
1. Apply the **Country** filter (USA). 🇺🇸
2. Add **State** to the Color section, **Profit** to the Size section, and other data to the Tooltip for interactivity. 🔍

This chart helped identify regions with the highest and lowest profit margins and allowed users to explore the data interactively.

#### Bubble Chart🫧:

![Bubble chart](https://github.com/Willie-Conway/Data-Modeling-and-Analysis-Project/blob/c29491f513696034c5e1f84bcf15971fb5506cba/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/Screenshot%202024-09-22%20225037.png)

---

### Step 6: Create a Line Chart for Sales Trends 📉
To analyze **sales trends over time**, I created a **Line Chart** that focused on states with sales greater than $40,000.

#### Steps:
1. Drag **Order Date** into the Columns section and **Sales** into the Rows section. 📅
2. Apply filters to focus on the USA and select states with sales over $40,000. 💵

The line chart helped to visualize how sales performed over time, with a clear focus on the highest-performing states.

#### Sales Trend Chart📊:

![Sales Trend chart](https://github.com/Willie-Conway/Data-Modeling-and-Analysis-Project/blob/c29491f513696034c5e1f84bcf15971fb5506cba/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/Screenshot%202024-09-22%20224817.png)

---

### Step 7: Create an Interactive Dashboard 📲
The final step was to combine all the visualizations into an **interactive dashboard**. This dashboard allows users to view:

- **Sales in USA** (Map Chart) 🌎
- **Profits in USA** (Bubble Chart) 💸
- **Sales Trend in USA** (Line Chart) 📈

Interactivity was enabled by using filters. For example, clicking on a specific state in the map chart dynamically updated both the bubble chart and line chart, allowing for a comprehensive view of sales performance.

#### Interactive Dashboard🖥️:

![Interactive Dashboard](https://github.com/Willie-Conway/Data-Modeling-and-Analysis-Project/blob/c29491f513696034c5e1f84bcf15971fb5506cba/Data%20Modeling%20Project/Data%20Modeling%20Project/Screenshots/Screenshot%202024-09-22%20231109.png)


# 📹 Demo Video

<div>
    <a href="https://www.loom.com/share/e74c2e9d68dc461a92feec2ad3997318">
      <p>Global Super Store - Interactive Dashboard - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/e74c2e9d68dc461a92feec2ad3997318">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/e74c2e9d68dc461a92feec2ad3997318-a22232212d972304-full-play.gif">
    </a>
  </div>


---

## 🏆 Conclusion and Key Takeaways
By completing this project, I achieved the following:

- **Database Restructuring**: Designed and implemented a normalized database schema to support scalable queries and analysis. 🔧
- **Data Modeling**: Created both an ER diagram and a star schema, forming a strong foundation for business intelligence analysis. 📊
- **Tableau Visualizations**: Developed interactive visualizations that provided actionable insights into sales performance, profits, and trends. 📈
- **Interactive Dashboard**: The interactive dashboard facilitated data exploration, allowing business users to focus on specific regions or time periods for decision-making. 🎯

This project demonstrated my ability to design efficient data models, implement them in MySQL, and use Tableau to build impactful, interactive data visualizations for business analysis.

---

## 🛠️ Tools and Technologies Used
- **MySQL Workbench**: For designing and implementing the database schema. 💻
- **Tableau**: For creating interactive visualizations and dashboards. 📊
- **SQL**: For querying and manipulating the data. 👨🏿‍💻
  
## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
