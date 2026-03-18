# SQL-Base-Test
**Assumed schema (used across all tasks):**

* `Customers(id, name, city, country)`
* `Orders(id, customer_id, order_date, amount)`
* `Products(id, name, price, category)`
* `OrderItems(order_id, product_id, quantity)`

---

### **Task 1 - Basic SELECT (Intro, Syntax, Select)**

Return all customers from Germany.

**Requirements:**

* Use `SELECT`
* Use `WHERE`

**Expected output columns:**
`id, name, city, country`

---

### **Task 2 - Filtering + Sorting (WHERE, AND/OR/NOT, ORDER BY)**

Return all orders with amount greater than 100 **and** placed after `2023-01-01`, sorted by amount descending.

**Requirements:**

* `WHERE` with `AND`
* `ORDER BY DESC`

**Expected output columns:**
`id, customer_id, order_date, amount`

---

### **Task 3 - Aggregation (COUNT, SUM, AVG, GROUP BY)**

Find total number of orders and average order amount per customer.

**Requirements:**

* `GROUP BY`
* `COUNT()`
* `AVG()`

**Expected output columns:**
`customer_id, total_orders, avg_amount`

---

### **Task 4 - Joins + Filtering (JOIN, LIKE, BETWEEN)**

Return all orders with customer names where:

* customer name starts with “A”
* order amount is between 50 and 500

**Requirements:**

* `INNER JOIN`
* `LIKE 'A%'`
* `BETWEEN`

**Expected output columns:**
`order_id, customer_name, amount`

---

### **Task 5 - Advanced Query (LEFT JOIN, GROUP BY, HAVING, CASE)**

For each customer, show:

* total amount spent
* number of orders
* a label:

  * `"VIP"` if total > 1000
  * `"Regular"` otherwise

Include customers with **no orders**.

Only show customers whose total spending is greater than 200.

**Requirements:**

* `LEFT JOIN`
* `GROUP BY`
* `HAVING`
* `SUM()`, `COUNT()`
* `CASE`

**Expected output columns:**
`customer_name, total_spent, order_count, customer_status`
