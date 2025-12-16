# Background 

GameGalaxy has grown rapidly across platforms and markets, but lacks a unified view of sales performance, customer value, and fulfillment efficiency. As competition and operating costs rise, leadership needs clear, data-driven insight into revenue-driving products, high-value acquisition channels, and logistics bottlenecks impacting customer loyalty.

# Overview 

This analysis will identify key trends, growth patterns, performance metrics, and KPIs across the business, such as: 

  - Identification of the products, platforms, and customer segments that generate the highest revenue and repeat purchases.
  - Evaluation of the marketing channels and acquisition methods that attract the most valuable users.
  - Assessment of countries, platforms, and customer segments with the strongest growth potential.

These insights will allow GameGalaxy to optimize pricing and product strategy, allocate marketing spend more efficiently, improve logistics performance, and strengthen revenue through targeted customer strategies.

# GameGalaxy E-Commerce Data Model: Orders, Customers, Products, Marketing, and Logistics

The data is structured around a central Orders fact table linked to customer, product, marketing, and logistics dimensions, enabling cross-functional analysis across 19,851 records.

![GameGalaxy Entity-Relationship Diagram (ERD)](images/GameGalaxy_ERD.jpg)

The Orders table is the central transaction record that links all business activity.

 - Users → Orders: Enables customer behavior, retention, and regional analysis.
 - Products → Orders: Supports product performance and demand evaluation.
 - Date → Orders: Enables trend, seasonality, and growth analysis over time.
 - Marketing Channels → Orders: Provides visibility into channel performance and marketing effectiveness.
 - Shipping → Orders: Measures fulfillment speed and operational efficiency.

Together, these relationships create a unified view of revenue, customers, marketing, and fulfillment performance.

Before beginning the analysis, a variety of checks were conducted for quality control and familiarization with the datasets. The SQL queries utilized to inspect and perform quality checks can be found (here).

# Executive Summary

**Objective**

The objective of this analysis is to summarize GameGalaxy’s historical sales, marketing, product, and logistics performance to identify key trends, patterns, and areas of opportunity across the business.

**Data Scope & Timeframe**

 - Data Source: GameGalaxy transactional order data
 - Grain: Order-level data
 - Timeframe: January 2019 – March 2021
 - Key Dimensions: Product, Marketing Channel, Platform, Region, Account Creation Method
 - Key Metrics: Total Revenue, Average Order Value, Top Products by Revenue, Revenue by Marketing Channel, Revenue by Platform, Conversion Proxy, Time to Ship, Average Revenure per User, and Regional Revenue Performance. 

_Assumption: Each ORDER_ID represents a completed purchase._

# Pertinent Findings for Business Objectives

***Sales Performance***

photo here 

- Revenue grew 161% year over year (2019 → 2020), signaling strong sales momentum and successful business scaling.


 - Total revenue trends upward consistently, with clear spikes in September, November, and December, likely driven by birthdays and holiday purchasing behavior.


 - Customer behavior is heavily web-based, with 97% purchasing via the website, 75% using desktop devices, and 84% of traffic originating from direct marketing channels.


 - Average Order Value (AOV) remains stable, indicating revenue growth is driven primarily by higher order volume rather than pricing changes.


- Average Revenue Per User (ARPU) varies by less than $5, highlighting an opportunity to increase customer lifetime value through repeat purchases and retention strategies.

***Product Performance***

Photo Here 

 - Revenue is highly concentrated, with the top three products accounting for 84.6% of total sales.
 - The 27-inch 4K gaming monitor, Nintendo Switch, and Sony PlayStation 5 bundle consistently outperform across platforms, indicating strong product-market fit.
 - From 2019 to 2020, revenue grew sharply across all four products, led by the Sony PlayStation 5 Bundle (+351%), followed by the Lenovo IdeaPad Gaming 3 (+198%), the 27in 4K Gaming Monitor (+120%), and the Nintendo Switch (+103%), highlighting especially strong momentum in console bundles and gaming hardware.

***Marketing Channel & Platform Performance***

