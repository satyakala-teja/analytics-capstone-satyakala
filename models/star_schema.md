# Star Schema Design for Sales Analytics

This document describes the star schema created for the sales analytics project.

---

## ⭐ Fact Table: fact_sales

Contains transactional data and numeric measurements.

**Columns:**
- order_id  
- order_date  
- customer_id  
- product  
- category  
- sub_category  
- region  
- quantity  
- unit_price  
- sales  
- total_revenue  
- profit  
- revenue_per_unit  
- high_value_order  
- month_name  
- quarter  
- is_weekend  
- order_weekday  

---

## ⭐ Dimension Tables

### 📌 dim_date
- date_id  
- order_date  
- month_name  
- quarter  
- order_weekday  
- is_weekend  

### 📌 dim_product
- product_id  
- product  
- category  
- sub_category  
- category_full  

### 📌 dim_customer
- customer_id  

### 📌 dim_region
- region_id  
- region  

---

           dim_product
                |
           dim_customer
                |

---

## ⭐ Why This Schema?

- Clear separation of transactions (fact) and descriptions (dimensions)  
- Fast aggregation for dashboards  
- Clean joins  
- Consistent metrics  
- Follows industry standards for Analytics Engineering  


## ⭐ ER Diagram (Star Schema)

