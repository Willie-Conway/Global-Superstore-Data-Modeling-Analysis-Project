

📘 sql_cheatsheet

# 💡 SQL & Data Engineering Concepts Cheat Sheet for Interview

## 🔄 SQL Language Categories

| Category | Description | Example Commands |
|----------|-------------|------------------|
| **DML** (Data Manipulation Language) | Used to manipulate existing data | `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `JOIN`, `AGGREGATE FUNCTIONS` |
| **DDL** (Data Definition Language) | Defines structure of DB objects | `CREATE`, `ALTER`, `DROP`, `TRUNCATE`, `VIEW`, `INDEX` |
| **DCL** (Data Control Language) | Controls access to data | `GRANT`, `REVOKE` |
| **TCL** (Transaction Control Language) | Manages transactions | `COMMIT`, `ROLLBACK`, `SAVEPOINT` |

---

## 🔧 DML Tools & Concepts

### ✅ Indexes
- **Purpose**: Improve performance for search and filtering.
- **Analogy**: Like a book index to find info quickly.
- **Example**: `CREATE INDEX idx_customer_name ON customers(name);`
- **Note**: Created using DDL, used within DML queries.

---

### 🔗 Joins
- **Purpose**: Merge data from multiple tables based on relationships.
- **Example**:
  ```sql
  SELECT o.order_id, c.customer_name
  FROM orders o
  JOIN customers c ON o.customer_id = c.id;

	•	Types: INNER, LEFT, RIGHT, FULL OUTER, CROSS

⸻

➕ Aggregations (Functions)
	•	Purpose: Summarize data.
	•	Common Functions: SUM(), AVG(), COUNT(), MIN(), MAX()
	•	Example:

SELECT region, SUM(sales) AS total_sales
FROM orders
GROUP BY region;



⸻

👀 Views (Saved Filters)
	•	Purpose: Virtual tables (predefined queries).
	•	Use Case: Simplify complex queries and improve readability.
	•	Example:

CREATE VIEW top_customers AS
SELECT customer_id, SUM(sales) AS total
FROM orders
GROUP BY customer_id
ORDER BY total DESC
LIMIT 10;



⸻

⚙️ Stored Procedures (Methods)
	•	Purpose: Encapsulate logic for repetitive tasks.
	•	Use Case: Apply business logic like applying tax or sending batch updates.
	•	Example:

CREATE PROCEDURE apply_tax()
BEGIN
  UPDATE orders SET total = total * 1.05;
END;



⸻

🧠 How to Remember

Tool	Category	Analogy
Indexes	Optimizer	Fast retrieval system
Stored Procedures	Methods	Reusable logic blocks
Aggregations	Functions	Math operations (SUM, AVG)
Views	Filters	Saved filtered reports
Joins	Merging Tool	Combine tables by relation


⸻

 