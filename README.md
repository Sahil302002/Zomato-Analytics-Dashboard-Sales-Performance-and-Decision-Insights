# Zomato Analytics Dashboard : Sales Performance and Decision Insights
![Zomato-Logo](https://github.com/user-attachments/assets/4b1fbcb4-476e-4f1c-a118-aa0515b290d4)

# Project Overview:

This project involved building a comprehensive **Zomato Analytics Dashboard** to track sales performance and derive actionable insights. A relational database, `Zomato_DB`, was created and optimized in **SQL Server**, integrating datasets from five CSV files with over 10,000 records.

By leveraging **Power BI**, the project delivered interactive visualizations, including KPIs, trend analyses, and customer insights. Key highlights include peak sales trends, top-performing cuisines like **Chicken Biryani**, and city-level performance, with **Mumbai** leading in sales. The dashboard also provides dynamic filtering and conditional formatting for deeper exploration.

This tool empowers stakeholders to make data-driven decisions, enhance operational efficiency, and optimize marketing strategies based on key metrics and patterns.

## SQL Database Creation & Power BI Integration for Zomato Analytics

### **Database Creation:**

Created and optimized a relational database, `Zomato_DB`, to enable seamless data analysis and integration with Power BI.

### Imported data from 5 CSV files into SQL Server:

- **Orders :  10,000 records with 8 attributes**   <a href ="orders.csv"> Orders Dataset Link</a>
- **Customers : 33 records with 3 attributes**     <a href ="customers.csv"> Customers Dataset link</a>
- **Deliveries:  9,750 records with 5 attributes** <a href ="deliveries.csv"> deliveries Dataset link </a>
- **Restaurants : 72 records with 5 attributes.**  <a href ="restaurants.csv"> Restaurants Dataset link </a>
- **Riders : 34 records with 3 attributes**        <a href ="riders.csv"> Riders Dataset link </a>

### **Optimization:**

- Applied efficient data types (`INT`, `VARCHAR`, `DATE`, etc.) for storage and querying.
- Established **Primary Keys** for unique identification and **Foreign Keys** to ensure data integrity across tables.

### **Data Validation:**

- Performed data quality checks and exploratory analysis in SQL Server to ensure clean and consistent data.

### **Data Preparation:**

- **Power Query:**
    - Merged `Orders` and `Deliveries` tables to create a unified dataset.
    - Calculated a new column, `Delivery_Duration` (in minutes), based on `Order_Time` and `Delivery_Time`.
- **Date Table:**
    - Created a comprehensive date table for time-based analysis and filtering.

### **DAX Measures:**

- Developed custom measures for critical KPIs:
    - **Total Sales (in Lakhs):** Aggregate sales calculation.
    - **Total Orders:** Total order volume.
    - **Delivered Orders vs. Not Delivered Orders.**
    - **Fulfilled vs. Not Fulfilled Orders.**
- Delivery segmentation logic:
    - **Delivery Rating:** Segmented based on delivery duration:
        - Low delivery time = Good Rating  like 5,4
        - High delivery time = Bad Rating.  like 1, 2 ,3
- **Data Quality and Transformation:**
    - Conducted data cleaning and validation to ensure accuracy.
    - Optimized data model for scalability and querying efficiency.

### **Power BI Integration:**

- Connected `Zomato_DB` to Power BI for creating interactive visualizations.
- The structured database facilitated efficient data queries and insights generation.

---

# Features of Zomato Sales and Orders Dashboard

## **KPI (Key Performance Indicators) Cards**

- **Total Orders:** 10,000
- **Total Sales:** ₹32.28 L
- **Average Delivery Rating:** 2.31
- **Fulfilled Orders:** 9,750 (97.5%)
- **Unfulfilled Orders:** 250 (2.5%)
- **Delivered Orders:** 8,953
- **Undelivered Orders:** 543
- **Pending Orders:** 254

**Purpose:**

Quickly assess Zomato’s operational performance with core metrics such as total orders, sales, and fulfillment rates. These KPIs provide stakeholders with a snapshot of business health and support strategic decisions.

---

## **Clustered Column and Line Chart**

**Data:**

- **Monthly Sales (Columns)** vs **Total Orders (Line)**

**Purpose:**

Visualizes monthly sales alongside order volumes to uncover trends and correlations over time.

**Insight:**

Sales and orders peak in March, while February shows a dip, likely influenced by external factors like seasonality or market conditions.

---

## **Horizontal Bar Chart**

**Data:**

- **Sales by City**: Mumbai, Bengaluru, Delhi, etc.
- **Top 5 Cuisines:** Based on order volume

**Purpose:**

Showcases sales distribution across cities and highlights customer preferences by cuisine type.

**Insight:**

Mumbai leads with ₹15.22 L in sales, indicating a strong market. Chicken Biryani and Paneer Butter Masala rank as the most popular cuisines, offering direction for menu and marketing strategies.

---

## **Line Chart**

**Data:**

- **Weekly Order Distribution (Sunday to Saturday)**

**Purpose:**

Identifies demand patterns during the week to inform marketing and operational planning.

**Insight:**

Sunday has the highest orders (1,506), while Tuesday sees a noticeable dip, presenting an opportunity for targeted engagement on low-demand days.

---

## **Shaded Line Chart**

**Data:**

- **Hourly Order Distribution**

**Purpose:**

Depicts order volume across hours of the day, aiding in operational and marketing optimization.

**Insight:**

Peak orders occur at 2pm to 4 PM (1,188 orders), likely due to late lunch breaks, suggesting an ideal time for promotional offers.

## **Additional Features:**

This dashboard includes slicers for **Restaurant Name**, **Year**, and **City**, allowing stakeholders to filter metrics dynamically based on their specific interests. 

A **Clear Filter** button is also included, making it easy to reset all filters and explore new perspectives. These enhancements enable stakeholders to extract more granular insights from the data.

---

# Sales and Orders Overview Dashboard: Sales and Order Insights

### **Monthly Sales & Order Trends**:

- **Peak Sales**: March recorded the highest sales, indicating possible promotions or seasonal effects.
- **Low Sales**: February, possibly due to holidays or slower consumer activity.
- **Insight**: Seasonal adjustments or targeted campaigns could help improve low-performance months like February.

### **Weekly Order Distribution**:

- **Sunday** saw the most orders, likely linked to consumer habits on weekends.
- **Tuesday** had the fewest, suggesting a weekday slump.
- **Insight**: Targeted marketing on Sundays could increase engagement, while Tuesday promotions could help boost sales.

### **Hourly Order Distribution**:

- **Peak Time**: Between 2 PM - 6 PM, particularly at 4 PM.
- **Insight**: Focus marketing efforts on late afternoons for maximum impact, capitalizing on when customers are most likely to place orders.

### **City-Specific Insights**:

- **Mumbai** stands out as the major revenue generator.
- **Insight**: Additional investments or operational enhancements in **Bengaluru** and **Delhi** could help grow sales.

### **Top Cuisines**:

- **Chicken Biryani** and **Paneer Butter Masala** are top sellers, making them crucial menu items.
- **Insight**: Restaurants could optimize offerings to align with these preferences, or create bundles around these popular dishes.

---

# Features of  Details Dashboard

### **Tabular Visual**

- **Visual Used:** Matrix/Table Visual
- **Purpose:** Provide detailed information in tabular format.
- **Examples:**
    - **Cuisines Data:** Displays total orders, Average Order Value and % contribution for different cuisines (e.g., Chicken Biryani, Paneer Butter Masala).
    - **Customers:** Shows customer contributions in terms of total orders , total sales, Fulfilled Order, Not Fulfilled Order
    - **Rider Performance:** Displays each rider’s fulfilled, pending, and not delivered orders along with average delivery rating.
    - **Restaurant Performance:** Includes total sales, total orders, and city-wise data for restaurants.

---

### **Conditional Formatting (Color Coding)**

- **Visual Used:** Applied on tables, bars, and KPIs.
- **Purpose:** Highlight important patterns or trends using colors.
- **Examples:**
    - **Cuisines:** Heatmap effect on % contribution to total sales (red for high values).
    - **Customers & Restaurants:** Conditional formatting for total sales to visually emphasize performance.
    - **Rider Ratings:** Green and yellow bars to indicate order delivery status.

---

### **Slicers**

- **Visual Used:** Slicer Visual
- **Purpose:** Allow filtering of data dynamically.
- **Examples:**
    - Filters for **Year, Restaurant, and City** to allow users to narrow down data.

---

### **Combination of Colors and Layout**

- **Purpose:** Ensure clear visual communication and intuitive navigation.
- **Examples:**
    - Bright red header for attention-grabbing KPIs.
    - Green for positive metrics (fulfilled orders).
    - Yellow and gray for pending and not delivered orders respectively.

# Detail Dashboard : Insights based on Customer, Restaurant and Orders details

### **Cuisine Insights**

- **Top-Selling Cuisine:** Chicken Biryani (754 orders, ₹2.39L revenue).
- **Highest Avg Order Value:** Lamb Kebab at ₹329.11.
- Popular items with significant sales percentages include Paneer Butter Masala (7.17%), Pasta Alfredo (7.17%), and Masala Dosa (7.32%).
- **Insights:**
    - High-demand cuisines like Chicken Biryani need promotions to retain dominance.
    - High avg-order-value items like Lamb Kebab can be bundled to improve sales.

### **Customer Insights**

- **Top Customer:** Sneha Desai (₹2.69L, 807 orders).
- Avg Order Value across top customers ranges between ₹314 and ₹339.
- Insights: Loyal customers contribute substantially; personalized offers can boost retention.

### **Rider Efficiency**

- **Top Rider (by Fulfilled Orders):** Arvind Joshi (313 orders fulfilled).
- **Pending Orders Issue:** Riders like Manoj Tiwari (23 pending orders) and Sandeep Rao (22 pending orders) have inefficiencies causing delays.
- **Avg Delivery Duration:** Most riders are rated below **3**, indicating delivery time or service issues.

### **Restaurant Contributions**

- **Highest Sales:**
    - Bademiya, Mumbai (₹1.57L from 485 orders).
    - Gajalee, Mumbai (₹1.57L from 480 orders).
- **Insights:**
    - Restaurants in Mumbai dominate with consistent high sales.

---

# **Overall Recommendations**

### **Marketing & Campaigns**

- **Target Peak Times:** Focus campaigns on **Sundays** and late afternoon slots (2 PM - 6 PM) to boost visibility during high-traffic hours.
- **Replicate Success:** Analyze the effective strategies from **March** and implement them in underperforming months like **February** to drive consistent growth.

### **Operational Enhancements**

- **Boost Fulfillment Rates:** Although the current **97.5% fulfillment rate** is commendable, strive to improve it further to enhance customer satisfaction.
- **Resolve Delivery Challenges:** Investigate the **543 undelivered orders** to address recurring issues, ensuring smoother operations and fewer order cancellations.

### **City-Specific Growth Strategies**

- **Focus on High-Performing Cities:** Invest more in cities like **Bengaluru** and **Delhi** to consolidate their strong market presence.
- **Tap into Underperforming Cities:** Explore strategies to boost engagement and sales in **Hyderabad** and **Chennai**, which currently show lower performance.

### **Menu Optimization**

- **Promote Popular Dishes:** Highlight bestsellers like **Chicken Biryani** and **Paneer Butter Masala**, and introduce combo offers to increase the average order value.
- **Encourage Upselling:** Pair high-value items, such as **Lamb Kebab**, with popular dishes to drive upselling opportunities.
- **Reassess Underperforming Items:** Reduce promotions and optimize inventory for items with lower contribution to revenue.

### **Delivery Operations Improvements**

- **Enhance the Delivery Process:**
    - Provide **training programs** for delivery riders to improve punctuality and customer interaction.
    - Introduce **incentives** for riders based on delivery time and ratings.
    - Use customer feedback to identify and resolve specific pain points in the delivery process.
- **Address Order Issues:**
    - **Undelivered Orders:** Investigate the **543 undelivered orders** to identify causes such as incorrect addresses or lack of product availability, and implement corrective measures.
    - **Unfulfilled Orders:** Analyze the reasons behind the **250 unfulfilled orders**
    - **Pending Orders Resolution**: Assign delivery zones more efficiently to ensure workload balance among riders.
    - **Identify Bottlenecks**: Address issues like traffic congestion or slow restaurant prep times to streamline order processing.

### **Improve Average Delivery Rating (Currently 2.31)**

- Launch initiatives like **customer feedback surveys** to pinpoint and address areas of dissatisfaction.
- Prioritize **speedier deliveries** and improve the experience by resolving traffic and restaurant preparation bottlenecks.

### **Customer Retention Strategies**

- **Reward Loyal Customers:** Implement loyalty programs to retain high-value customers like Sneha Desai and Rahul Verma.
- **Engage Mid-Tier Customers:** Offer exclusive promotions to customers like Bhavna Agarwal and Ritu Patel, encouraging repeat purchases and greater spending.

[**Zomato SQL Analysis**](https://www.notion.so/Zomato-SQL-Analysis-185a2286622b8001b0f1f4c23018d8c0?pvs=21)

[Questions](https://www.notion.so/Questions-185a2286622b804d967cf0f4e185e83b?pvs=21)
