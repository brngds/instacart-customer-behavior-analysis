# 🛒 Instacart Customer Behavior Analysis

Exploratory data analysis of Instacart customer shopping behavior using **Python**, **Pandas**, and **Matplotlib**, with a focus on data cleaning, purchasing patterns, reorder behavior, and customer habits.

## 📌 Context

Understanding how customers shop is essential for grocery delivery platforms to improve product recommendations, inventory decisions, and the overall customer experience.

In this project, transactional data from **Instacart**, an online grocery delivery platform, was analyzed to identify patterns in when customers place orders, which products they purchase most frequently, and how often previously purchased products are reordered.

The project was developed as part of my Data Science studies and reorganized for portfolio presentation, preserving the analytical process and results.

## 🎯 Problem

The main objective was to explore Instacart customer purchasing behavior and answer questions such as:

- When do customers usually place their orders?
- How frequently do customers return to place another order?
- How many orders do customers typically make?
- Which products are purchased most frequently?
- Which products are most frequently reordered?
- How many items are typically included in an order?
- Which products are most often added first to the cart?
- How does reorder behavior vary across customers and products?

Before answering these questions, the datasets required preprocessing to identify and handle missing values, duplicated records, and data type inconsistencies.

## 📊 Dataset

The analysis uses five related datasets describing orders, products, departments, aisles, and the relationship between products and orders.

### `instacart_orders.csv`

Contains information about customer orders, including:

- `order_id` — unique order identifier
- `user_id` — unique customer identifier
- `order_number` — order sequence for each customer
- `order_dow` — day of the week when the order was placed
- `order_hour_of_day` — hour when the order was placed
- `days_since_prior_order` — number of days since the customer's previous order

### `products.csv`

Contains product information:

- `product_id`
- `product_name`
- `aisle_id`
- `department_id`

### `order_products.csv`

Connects products to orders and includes:

- `order_id`
- `product_id`
- `add_to_cart_order`
- `reordered`

### `aisles.csv`

Contains aisle identifiers and names.

### `departments.csv`

Contains department identifiers and names.

## 🔎 Approach

The project followed a structured exploratory data analysis workflow:

1. Data loading and initial inspection
2. Data type validation
3. Identification and treatment of missing values
4. Identification and removal of duplicated records
5. Validation of order dates and times
6. Analysis of purchasing behavior by hour and day
7. Analysis of reorder intervals
8. Customer order frequency analysis
9. Product popularity analysis
10. Basket size analysis
11. Reorder behavior analysis
12. Interpretation of customer purchasing patterns

## 🧹 Data Preparation

Before performing the exploratory analysis, the datasets were inspected for quality issues.

The preprocessing stage included:

- validation and correction of data types;
- identification of duplicated records;
- removal of confirmed duplicates;
- investigation of missing values;
- treatment of missing values according to their meaning;
- validation of identifier columns;
- verification of expected ranges for day-of-week and hour-of-day variables.

This step ensured that the subsequent analyses were based on consistent and reliable data.

## 📈 Analysis

### Order activity throughout the day

Order volume was analyzed across the 24 hours of the day to identify periods with higher and lower customer activity.

### Orders by day of the week

Customer purchasing activity was compared across the seven days of the week.

### Time between orders

The distribution of `days_since_prior_order` was analyzed to understand how long customers typically wait before placing another order.

### Wednesday vs. Saturday behavior

Order-hour distributions for Wednesday and Saturday were compared to identify differences in purchasing behavior between the two days.

### Orders per customer

The number of orders associated with each customer was analyzed to better understand customer purchasing frequency.

### Most purchased products

Products were ranked according to how frequently they appeared in customer orders.

### Basket size

The number of products included in each order was analyzed to understand typical basket sizes and their distribution.

### Reorder behavior

Reorder patterns were analyzed from multiple perspectives:

- products most frequently reordered;
- reorder proportion by product;
- reorder proportion by customer.

### First products added to the cart

The analysis also identified which products customers most frequently added as the first item in their shopping carts.

## 💡 Key Findings

The exploratory analysis reveals several behavioral patterns within the available Instacart data:

- customer activity varies depending on the hour of the day and the day of the week;
- purchasing activity is concentrated during specific daytime periods;
- many customers show recurring purchasing behavior;
- a relatively small group of products appears very frequently across orders;
- frequently purchased products also show meaningful reorder behavior;
- basket sizes vary considerably across orders;
- reorder behavior differs across both products and customers;
- the first product added to a cart provides another perspective on recurring shopping habits.

These findings describe patterns observed in the analyzed dataset and should not automatically be generalized beyond the available data.

## 🚀 Business Applications

The patterns identified in this analysis could support business decisions such as:

- improving personalized product recommendations;
- identifying products with strong recurring demand;
- optimizing promotional campaigns according to purchasing periods;
- supporting inventory and assortment decisions;
- developing reorder reminders;
- improving cross-selling strategies;
- understanding customer purchasing frequency;
- identifying products that play an important role in recurring shopping routines.

## ⚠️ Limitations

This project is an exploratory analysis of an adapted version of the Instacart dataset.

The results describe behavioral patterns present in the available data and should not be interpreted as causal relationships or as representative of all Instacart customers.

Additionally, the analysis focuses primarily on descriptive statistics and exploratory visualization rather than statistical inference or predictive modeling.

## 🛠️ Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## 📁 Repository Structure

instacart-customer-behavior-analysis/
│
├── README.md
│
├── data/
│   ├── README.md
│   ├── instacart_orders.csv
│   ├── products.csv
│   ├── order_products.csv
│   ├── aisles.csv
│   └── departments.csv
│
└── notebook/
    ├── README.md
    └── instacart_customer_behavior_analysis.ipynb
