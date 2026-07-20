# Project Background
Dataset including orders information
# Project Objective 
Using SQL queries to extract insights from a dataset.
# Executive Summary
## Overview of findings
```sql
--Result to Highest payment method used from all orders
SELECT PaymentMethod, count(PaymentMethod) as No_of_orders FROM Dataset
GROUP BY PaymentMethod
ORDER BY No_of_orders DESC;
```

```sql
--Result to Highest product sold for 2,5 years
SELECT Product, sum(Quantity) as No_of_total_products FROM Dataset
GROUP BY Product
ORDER BY No_of_total_products DESC;
```

```sql
--Result to Highest Profitable Product
SELECT Product, sum(TotalPrice) as Total_Price FROM Dataset
GROUP BY Product
ORDER BY Total_Price DESC;
```

```sql
--Returns Highest order status company faces
SELECT OrderStatus, count(OrderStatus) as No_of_orders FROM Dataset
GROUP BY OrderStatus
ORDER BY No_of_orders DESC;

```

```sql
--Results Highest item in cart that makes customers purchase more
SELECT ItemsInCart, count(ItemsInCart) as No_of_orders FROM Dataset
GROUP BY ItemsInCart
ORDER BY No_of_orders DESC;
```
# Insights
- Online payments are the most frequently used payment method, accounting for 21.5% of all 1,200 recorded payments, making them the preferred payment option among customers.
- Chairs are the best-selling product category, representing 15.90% of the 3,535 products sold over the past 2.5 years, demonstrating consistent high customer demand.
- Chairs generate the highest product revenue, contributing 15.47% of the total revenue of 1,264,761.96, outperforming all other product categories.
- Cancelled orders account for 20.80% of the 1,200 total orders, representing the highest order status after completed orders and highlighting a significant area for operational improvement.
- Customers are most likely to complete purchases when their cart contains five products, with 15.92% of all 1,200 orders consisting of exactly five items, indicating an optimal basket size.

# Recommendations
- Prioritize the chair product category by increasing inventory availability, enhancing marketing campaigns, and introducing complementary product bundles to capitalize on its strong sales and revenue performance.
- Investigate the root causes of order cancellations through customer feedback, order analysis, and checkout process reviews to identify pin points and reduce cancellation rates.
- Leverage the five item purchasing trend by implementing promotions such as "Buy 5 and Save," product bundles, or personalized recommendations that encourage customers to reach a five-item cart.
- Promote online payment methods by offering incentives such as discounts, loyalty rewards, or faster checkout experiences to further encourage adoption and improve customer convenience.

# Tools Used 
- SQL

# What this project shows 
- SQL fundamentals, querying data, filtering and grouping.
- Proving ability to bridge the gap between massive datasets and specific answers through pure relational logic.
