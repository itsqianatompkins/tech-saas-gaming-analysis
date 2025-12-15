# SaaS Business Impact: A Cross-Functional Analysis in Gaming Commerce 

# Background 

GameGalaxy, a gaming retailer, operates across web, mobile, and console platforms using SaaS technology and has experienced rapid growth in customer base, sales, and operations. However, leadership lacks a unified understanding of sales trends, customer value, product performance, and logistics efficiency across different markets and channels. With increasing competition and rising operational costs, the company needs clear, data-driven visibility into which products drive revenue, which channels attract high-value users, and where operational bottlenecks are slowing fulfillment and eroding customer loyalty. The data provided offers an opportunity to uncover these insights and address existing blind spots.

# Overview 

This analysis will identify key trends, growth patterns, performance metrics, and KPIs across the business, such as: 

  - Which products, platforms, and segments generate the highest revenue and repeat purchases

  - Which marketing channels and acquisition methods attract the most valuable users

  - Where fulfillment delays occur and how operational speed affects customer retention

  - Which countries, platforms, and customer segments offer the strongest opportunities for growth

These insights will allow GameGalaxy to optimize pricing and product strategy, allocate marketing spend more efficiently, improve logistics performance, and strengthen revenue through targeted customer strategies.

**Behind the Analysis: Technical Resources**

 - An interactive PowerBI dashboard can be downloaded (here)
 - The SQL queries utilized to inspect and perform quality checks can be found (here)
 - Targeted SQL queries regarding relevant business questions can be found (here)

# GameGalaxy E-Commerce Data Model: Orders, Customers, Products, Marketing, and Logistics

The data is structured around a central Orders fact table linked to customer, product, marketing, and logistics dimensions, enabling cross-functional analysis across 19,851 records.

<img width="1414" height="2000" alt="Data Structure Overview" src="https://github.com/user-attachments/assets/44dbbbf7-e8a2-4430-95e4-598e1e5b9f53" />


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

**Pertinent Findings for Business Objectives**
