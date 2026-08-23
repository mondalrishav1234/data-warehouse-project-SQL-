# Data Catalog for Gold Layer

## Overview

The **Gold Layer** contains the final, business-ready representation of the data warehouse. It is designed primarily for **analytics, reporting, and business insights**.

This layer is organized using **dimension tables** and **fact tables**, which together form the analytical data model used for reporting.

---

### 1. **gold.dim_customers**

* **Purpose:** Contains customer-related information along with demographic and geographical attributes.

* **Columns:**

| Column Name     | Data Type    | Description                                                                       |
| --------------- | ------------ | --------------------------------------------------------------------------------- |
| customer_key    | INT          | A surrogate key used to uniquely identify a customer record within the dimension. |
| customer_id     | INT          | A unique numeric identifier assigned to each customer.                            |
| customer_number | NVARCHAR(50) | An alphanumeric customer identifier used for tracking and reference purposes.     |
| first_name      | NVARCHAR(50) | The first name of the customer.                                                   |
| last_name       | NVARCHAR(50) | The customer's last or family name.                                               |
| country         | NVARCHAR(50) | The country where the customer resides, such as 'Australia'.                      |
| marital_status  | NVARCHAR(50) | Indicates the customer's marital status, such as 'Married' or 'Single'.           |
| gender          | NVARCHAR(50) | Represents the customer's gender, such as 'Male', 'Female', or 'n/a'.             |
| birthdate       | DATE         | The customer's date of birth stored in YYYY-MM-DD format.                         |
| create_date     | DATE         | The date and time when the customer record was originally created in the system.  |

---

### 2. **gold.dim_products**

* **Purpose:** Contains product information and the main attributes associated with each product.

* **Columns:**

| Column Name          | Data Type    | Description                                                                                    |
| -------------------- | ------------ | ---------------------------------------------------------------------------------------------- |
| product_key          | INT          | A surrogate key that uniquely identifies each product record in the dimension table.           |
| product_id           | INT          | A unique identifier assigned to the product for tracking and reference.                        |
| product_number       | NVARCHAR(50) | An alphanumeric product code used to identify and reference the product.                       |
| product_name         | NVARCHAR(50) | The descriptive name of the product, including relevant details such as type, color, and size. |
| category_id          | NVARCHAR(50) | An identifier that associates the product with its corresponding category.                     |
| category             | NVARCHAR(50) | The main category used to group similar products, such as Bikes or Components.                 |
| subcategory          | NVARCHAR(50) | A more specific classification of the product within its main category.                        |
| maintenance_required | NVARCHAR(50) | Indicates whether the product requires maintenance, such as 'Yes' or 'No'.                     |
| cost                 | INT          | The base cost or price associated with the product, represented in monetary units.             |
| product_line         | NVARCHAR(50) | Identifies the product series or line to which the product belongs, such as Road or Mountain.  |
| start_date           | DATE         | The date from which the product became available for sale or use.                              |

---

### 3. **gold.fact_sales**

* **Purpose:** Stores sales transaction information that can be used for analytical and reporting purposes.

* **Columns:**

| Column Name   | Data Type    | Description                                                                            |
| ------------- | ------------ | -------------------------------------------------------------------------------------- |
| order_number  | NVARCHAR(50) | An alphanumeric identifier used to uniquely identify a sales order, such as 'SO54496'. |
| product_key   | INT          | A surrogate key that connects the sales transaction to the product dimension.          |
| customer_key  | INT          | A surrogate key that connects the sales transaction to the customer dimension.         |
| order_date    | DATE         | The date on which the customer placed the order.                                       |
| shipping_date | DATE         | The date on which the order was shipped to the customer.                               |
| due_date      | DATE         | The date by which the payment for the order was due.                                   |
| sales_amount  | INT          | The total sales value of the individual order line, expressed in whole currency units. |
| quantity      | INT          | The number of units of the product included in the order line.                         |
| price         | INT          | The selling price of one unit of the product, represented in whole currency units.     |
