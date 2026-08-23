# **Naming Conventions**

This document defines the naming standards followed for schemas, tables, views, columns, stored procedures, and other database objects within the data warehouse.

## **Table of Contents**

1. [General Principles](#general-principles)
2. [Table Naming Conventions](#table-naming-conventions)

   * [Bronze Rules](#bronze-rules)
   * [Silver Rules](#silver-rules)
   * [Gold Rules](#gold-rules)
3. [Column Naming Conventions](#column-naming-conventions)

   * [Surrogate Keys](#surrogate-keys)
   * [Technical Columns](#technical-columns)
4. [Stored Procedure Naming Conventions](#stored-procedure-naming-conventions)

---

## **General Principles**

The following general rules are applied throughout the project:

* **Naming Style:** Use `snake_case` with lowercase characters and underscores (`_`) between individual words.
* **Language:** All database object and column names should be written in English.
* **Reserved Words:** SQL reserved keywords should not be used as names for database objects or columns.

---

## **Table Naming Conventions**

### **Bronze Rules**

Tables in the Bronze layer retain the naming structure of their respective source systems.

* The table name must begin with the **source system name**.
* The original entity/table name from the source should be retained without modification.
* **Naming Pattern:** `<sourcesystem>_<entity>`

  * `<sourcesystem>`: Identifies the source system, such as `crm` or `erp`.
  * `<entity>`: Represents the original entity/table name from the source system.
  * **Example:** `crm_customer_info` → Customer information received from the CRM source.

### **Silver Rules**

Silver layer tables follow the same source-based naming approach as the Bronze layer.

* The table name should begin with the **source system name**.
* The original source entity name should be retained.
* **Naming Pattern:** `<sourcesystem>_<entity>`

  * `<sourcesystem>`: Name of the originating system, such as `crm` or `erp`.
  * `<entity>`: Original entity/table name from the source.
  * **Example:** `crm_customer_info` → Customer information originating from the CRM system.

### **Gold Rules**

Gold layer tables use descriptive names that represent their business purpose.

* Names should clearly describe the role and content of the table.
* A category prefix should be used to identify the type of table.
* **Naming Pattern:** `<category>_<entity>`

  * `<category>`: Indicates the table type, such as `dim` for dimension or `fact` for fact.
  * `<entity>`: A meaningful business-related name such as `customers`, `products`, or `sales`.
  * **Examples:**

    * `dim_customers` → Dimension table containing customer information.
    * `fact_sales` → Fact table containing sales transaction data.

#### **Glossary of Category Patterns**

| Pattern   | Meaning         | Example(s)                                 |
| --------- | --------------- | ------------------------------------------ |
| `dim_`    | Dimension table | `dim_customer`, `dim_product`              |
| `fact_`   | Fact table      | `fact_sales`                               |
| `report_` | Reporting table | `report_customers`, `report_sales_monthly` |

---

## **Column Naming Conventions**

### **Surrogate Keys**

Surrogate keys used in dimension tables follow a consistent naming pattern.

* Dimension table primary keys should end with the suffix `_key`.
* **Naming Pattern:** `<table_name>_key`

  * `<table_name>`: Represents the entity or table associated with the key.
  * `_key`: Indicates that the column is a surrogate key.
  * **Example:** `customer_key` → Surrogate key used in the `dim_customers` table.

### **Technical Columns**

Technical or system-generated columns use the `dwh_` prefix.

* Technical columns must begin with **`dwh_`** followed by a descriptive name.
* **Naming Pattern:** `dwh_<column_name>`

  * `dwh`: Prefix used to identify system-generated metadata columns.
  * `<column_name>`: Describes the purpose of the technical field.
  * **Example:** `dwh_load_date` → Stores the date on which a record was loaded into the data warehouse.

---

## **Stored Procedure Naming Conventions**

Stored procedures responsible for loading data into the warehouse should follow a consistent naming pattern.

* **Naming Pattern:** `load_<layer>`

  * `<layer>`: Specifies the warehouse layer being loaded, such as `bronze`, `silver`, or `gold`.

### **Examples**

* `load_bronze` → Loads data into the Bronze layer.
* `load_silver` → Loads data into the Silver layer.
* `load_gold` → Loads data into the Gold layer.

These conventions help keep the database structure consistent, readable, and easier to maintain throughout the project.
