
#  PostgreSQL Basics

###  Table: `books`

| id | title                 | author              | price |
| -- | --------------------- | ------------------- | ----- |
| 1  | The Great Gatsby      | F. Scott Fitzgerald | 10.99 |
| 2  | 1984                  | George Orwell       | 12.99 |
| 3  | To Kill a Mockingbird | Harper Lee          | 8.99  |
| 4  | 1984                  | George Orwell       | 12.99 |
| 5  | Brave New World       | Aldous Huxley       | NULL  |

---

### 1️  SELECT Fundamentals

Retrieve all or specific columns from the `books` table.

```sql
SELECT * FROM books;
```

  **Output:**

| id | title                 | author              | price |
| -- | --------------------- | ------------------- | ----- |
| 1  | The Great Gatsby      | F. Scott Fitzgerald | 10.99 |
| 2  | 1984                  | George Orwell       | 12.99 |
| 3  | To Kill a Mockingbird | Harper Lee          | 8.99  |
| 4  | 1984                  | George Orwell       | 12.99 |
| 5  | Brave New World       | Aldous Huxley       | NULL  |

```sql
SELECT title, author FROM books;
```

  **Output:**

| title                 | author              |
| --------------------- | ------------------- |
| The Great Gatsby      | F. Scott Fitzgerald |
| 1984                  | George Orwell       |
| To Kill a Mockingbird | Harper Lee          |
| 1984                  | George Orwell       |
| Brave New World       | Aldous Huxley       |

---

### 2️ Aliases and Constants

Rename columns or insert fixed values.

```sql
SELECT title AS book_title, 'Available' AS status FROM books;
```

  **Output:**

| book\_title           | status    |
| --------------------- | --------- |
| The Great Gatsby      | Available |
| 1984                  | Available |
| To Kill a Mockingbird | Available |
| 1984                  | Available |
| Brave New World       | Available |

---

### 3️ Expressions in SELECT

Calculate new values in the result.

```sql
SELECT title, price, price * 2 AS double_price FROM books;
```

  **Output:**

| title                 | price | double\_price |
| --------------------- | ----- | ------------- |
| The Great Gatsby      | 10.99 | 21.98         |
| 1984                  | 12.99 | 25.98         |
| To Kill a Mockingbird | 8.99  | 17.98         |
| 1984                  | 12.99 | 25.98         |
| Brave New World       | NULL  | NULL          |

---

### 4️ Selecting DISTINCT Values

Return only unique values.

```sql
SELECT DISTINCT title FROM books;
```

  **Output:**

| title                 |
| --------------------- |
| The Great Gatsby      |
| 1984                  |
| To Kill a Mockingbird |
| Brave New World       |

---

### 5️ Filtering with WHERE

Filter rows using conditions.

```sql
SELECT * FROM books WHERE price > 10;
```

  **Output:**

| id | title            | author              | price |
| -- | ---------------- | ------------------- | ----- |
| 1  | The Great Gatsby | F. Scott Fitzgerald | 10.99 |
| 2  | 1984             | George Orwell       | 12.99 |
| 4  | 1984             | George Orwell       | 12.99 |

---

### 6️ Sorting with ORDER BY

Sort rows by column values.

```sql
SELECT * FROM books ORDER BY price;
```

  **Output:**

| id | title                 | author              | price |
| -- | --------------------- | ------------------- | ----- |
| 3  | To Kill a Mockingbird | Harper Lee          | 8.99  |
| 1  | The Great Gatsby      | F. Scott Fitzgerald | 10.99 |
| 2  | 1984                  | George Orwell       | 12.99 |
| 4  | 1984                  | George Orwell       | 12.99 |
| 5  | Brave New World       | Aldous Huxley       | NULL  |

---

### 7️ Limiting Results with LIMIT

Limit number of rows in result.

```sql
SELECT * FROM books LIMIT 2;
```

  **Output:**

| id | title            | author              | price |
| -- | ---------------- | ------------------- | ----- |
| 1  | The Great Gatsby | F. Scott Fitzgerald | 10.99 |
| 2  | 1984             | George Orwell       | 12.99 |

```sql
SELECT * FROM books LIMIT 2 OFFSET 2;
```

  **Output:**

| id | title                 | author        | price |
| -- | --------------------- | ------------- | ----- |
| 3  | To Kill a Mockingbird | Harper Lee    | 8.99  |
| 4  | 1984                  | George Orwell | 12.99 |

---

### 8️ Handling NULL Values

Find rows with or without missing values.

```sql
SELECT * FROM books WHERE price IS NULL;
```

  **Output:**

| id | title           | author        | price |
| -- | --------------- | ------------- | ----- |
| 5  | Brave New World | Aldous Huxley | NULL  |

```sql
SELECT * FROM books WHERE price IS NOT NULL;
```

  **Output:** Returns all rows except the one with NULL price.

---

### 9️ Single Line Comments

Use `--` to add explanations.

```sql
-- Get all books with price above ₹10
SELECT * FROM books WHERE price > 10;
```

  Comments are ignored by PostgreSQL during execution.

---

