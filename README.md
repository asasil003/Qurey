# E-Commerce Database Schema & Queries

This project defines a basic MySQL schema for an e-commerce system and provides essential SQL queries for common operations.

## Database Tables

- **Users**: Stores user information (customers and admins).
- **Products**: Stores product details, including stock and price.
- **Orders**: Stores order records, linked to users.
- **Order_Items**: Stores individual items within each order.

## Schema

See `Queries.txt` for the full `CREATE TABLE` statements.

## Example Queries

### 1. Fetch all products with more than 10 stock

```sql
SELECT * FROM Products WHERE stock > 10;
```

### 2. Fetch all orders placed by a specific user

```sql
SELECT * FROM Orders WHERE user_id = ?;
-- Replace ? with the user's id
```

### 3. Update product stock after an order is placed

```sql
UPDATE Products
SET stock = stock - ?
WHERE id = ?;
-- Replace ? with the quantity ordered and product id
```

## Usage

1. Run the SQL statements in `Queries.txt` to create the tables.
2. Use the provided queries to interact with your e-commerce database.

---

**Note:**  
- Adjust data types and constraints as needed for your application.
- Always validate user input and handle transactions when updating stock after orders.
