![game-galaxy](https://github.com/user-attachments/assets/0bb8f2c7-dbab-411d-a0f9-e296ea3c03fd)

# Background 

GameGalaxy has grown rapidly across platforms and markets, but lacks a unified view of sales performance, customer value, and fulfillment efficiency. As competition and operating costs rise, leadership needs clear, data-driven insights into revenue-driving products, high-value acquisition channels, and logistics bottlenecks that impact customer loyalty.

**Objective**

The objective of this analysis is to summarize GameGalaxy’s historical sales, marketing, product, and logistics performance, identifying key trends, patterns, and areas of opportunity across the business.

**Data Scope & Timeframe**

 - Data Source: GameGalaxy transactional order data
 - Grain: Order-level data
 - Timeframe: January 2019 – March 2021 (Nine Quarters)
 - Key Dimensions: Product, Marketing Channel, Platform, Region, Account Creation Method
 - Key Metrics: Total Revenue, Average Order Value, Top Products by Revenue, Revenue by Marketing Channel, Revenue by Platform, Conversion Proxy, Time to Ship, Average Revenue per User, and Regional Revenue Performance. 

_Assumption: Each ORDER_ID represents a completed purchase._

# Overview 

This analysis will identify key trends, growth patterns, performance metrics, and KPIs across the business, such as: 

  - Identification of the products, platforms, and customer segments that generate the highest revenue and repeat purchases.
  - Evaluation of the marketing channels and acquisition methods that attract the most valuable users.
  - Assessment of countries, platforms, and customer segments with the strongest growth potential.

These insights will allow GameGalaxy to optimize pricing and product strategy, allocate marketing spend more efficiently, improve logistics performance, and strengthen revenue through targeted customer strategies.

Technical Documentation - Excel spreadsheets used to clean, organize, and visualize the data are available here: [gamegalaxy-orders-data.xlsx](https://github.com/user-attachments/files/24419572/gamegalaxy-orders-data.xlsx)

<img width="1920" height="1080" alt="GameGalaxy_ERD" src="https://github.com/user-attachments/assets/6bc1e98b-072e-4a9b-bd5b-b092b1bc28f1" />


# GameGalaxy E-Commerce Data Model: Orders, Customers, Products, Marketing, and Logistics

The data is structured around a central Orders fact table linked to customer, product, marketing, and logistics dimensions, enabling cross-functional analysis across 19,851 records.

The Orders table is the central transaction record that links all business activity.

 - Users → Orders: Enables customer behavior, retention, and regional analysis.
 - Products → Orders: Supports product performance and demand evaluation.
 - Date → Orders: Enables trend, seasonality, and growth analysis over time.
 - Marketing Channels → Orders: Provides visibility into channel performance and marketing effectiveness.
 - Shipping → Orders: Measures fulfillment speed and operational efficiency.

Together, these relationships create a unified view of revenue, customers, marketing, and fulfillment performance.

Before beginning the analysis, various checks were conducted for quality control and to familiarize myself with the datasets. The SQL queries utilized to inspect and perform quality checks can be found (here).

# Executive Summary

***Overview of Findings***

Overall revenue totaled **$5.49M over 9 quarters, with 2020 emerging as the strongest sales year**, driven by higher order volume rather than increases in pricing. Sales peaked in **September and December**, indicating strong seasonality likely tied to major game releases and holiday demand. North America (NA) accounted for the largest share of revenue, followed by Europe, the Middle East, and Africa (EMEA).

The **website platform generated 97%** of total revenue, confirming it as the primary sales channel, while mobile contributed a small but meaningful share. **Direct traffic dominated overall revenue**, followed by email and affiliate marketing. Notably, **email outperformed direct traffic on mobile**, suggesting channel effectiveness varies by device.

Revenue was highly concentrated among a few top products, led by the **27” 4K Gaming Monitor, Nintendo Switch, and Sony PlayStation 5 Bundle**. These products significantly outperformed all others, indicating a narrow but high-impact product mix. Lower-priced accessories contributed minimal revenue, highlighting an opportunity to expand complementary offerings to drive repeat purchases.


***Sales Performance***


<img width="1161" height="534" alt="Screenshot 2025-12-15 at 8 46 09 PM" src="https://github.com/user-attachments/assets/732b55f7-2de5-4179-ac48-6a6c9c2c383d" />


- Revenue grew 161% year over year (2019 → 2020), signaling strong sales momentum and successful business scaling.

 - Total revenue trends upward consistently, with clear spikes in September, November, and December, likely driven by birthdays and holiday purchasing behavior.

 - Customer behavior is heavily web-based, with 97% purchasing via the website, 75% using desktop devices, and 84% of traffic originating from direct marketing channels.

 - Average Order Value (AOV) remains stable, indicating revenue growth is driven primarily by higher order volume rather than pricing changes.

- Average Revenue Per User (ARPU) varies by less than $5, highlighting an opportunity to increase customer lifetime value through repeat purchases and retention strategies.

***Product Performance***

<img width="1421" height="622" alt="Screenshot 2025-12-16 at 12 47 29 AM" src="https://github.com/user-attachments/assets/90f821c8-3019-4a6a-9dc5-461825bb9524" />

 - Revenue is highly concentrated, with the top three products accounting for 84.6% of total sales.
   
 - The 27-inch 4K gaming monitor, Nintendo Switch, and Sony PlayStation 5 bundle consistently outperform across platforms, indicating strong product-market fit.
   
 - From 2019 to 2020, revenue grew sharply across all four products, led by the Sony PlayStation 5 Bundle (+351%), followed by the Lenovo IdeaPad Gaming 3 (+198%), the 27in 4K Gaming Monitor (+120%), and the Nintendo Switch (+103%), highlighting especially strong momentum in console bundles and gaming hardware.

***Marketing Channel & Platform Performance***

<img width="1425" height="619" alt="Screenshot 2025-12-16 at 11 46 09 PM" src="https://github.com/user-attachments/assets/cbb6f314-770b-4ff2-baa3-d1a49958419b" />
 
 - Global revenue growth ranked by sales (2019–2020): North America (NA) led with $759.7K → $1.9M (+150.5%), followed by  Europe, Middle East, Africa (EMEA) $411.5K → $1.09M (+165.1%), Asia Pacific (APAC) $150.1K → $448.8K (+199.0%), and Latin America (LATAM) $74.3K → $205.1K (+175.9%).
   
 - Drove multi-channel revenue growth YoY, led by Direct ($1.19M → $3.09M, +159%) and Email ($115K → $373K, +223%), while scaling Social Media (+138%) and Affiliate (+71%) channels.
   
 - Scaled platform revenue YoY, with the Website driving primary growth ($1.35M → $3.56M, +163%) and the Mobile App doubling performance ($42K → $87K, +106%).
   
 - Order Methods increased YoY: Desktop led ($990K → $2.82M, +185%), followed by Mobile ($318K → $642K, +102%), Unknown ($69K → $140K, +103%), Tablet ($18K → $44K, +138%), and TV ($1.1K → $3.4K, +207%), with TV showing the highest growth rate despite the lowest overall sales volume.

# Business Insights

***Caveats & Assumptions***

Approximately 2,000 of 19.851 records contained shipping dates occurring before purchase dates, indicating data quality issues that prevented a reliable calculation of average time-to-ship. For analysis purposes, it was assumed these dates were reversed due to entry or system errors; however, this introduces potential risk of misrepresenting fulfillment performance. To mitigate this risk, affected records should be excluded from time-based metrics or validated through data cleaning, along with implementing stronger data validation controls and routine quality audits going forward.

***Recommendations & Next Steps*** 

 - Expand the product ecosystem by vertically integrating refurbished and trending games/accessories for top consoles, turning one-time console buyers into repeat purchasers and increasing lifetime value.

- Optimize marketing spend by increasing investment in direct and email channels, especially during high-impact months (Aug–Sept and Nov–Dec), to fully capitalize on peak season demand.

 - Focus on retention initiatives, such as bundling offers, loyalty programs, or personalized email campaigns targeted to top-tier markets (North America/EMEA) to convert first-time buyers into repeat buyers.

 - Enhance mobile engagement given email’s strong relative performance on mobile devices; optimize campaigns and user experience for mobile.

 - Improve data quality processes to enable more reliable operational metrics (e.g., shipping performance), which are critical for strategic logistics decisions.
