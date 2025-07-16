# 🧠 SQL Basics Quiz (30 Questions)

_All examples use the following `books` table:_

| id | title | author | price |
|----|------------------------|----------------------|--------|
| 1  | The Great Gatsby | F. Scott Fitzgerald | 10.99 |
| 2  | 1984 | George Orwell | 12.99 |
| 3  | To Kill a Mockingbird | Harper Lee | 8.99 |
| 4  | 1984 | George Orwell | 12.99 |
| 5  | Brave New World | Aldous Huxley | NULL |

---

## Part 1 – SELECT & Projection (Q1–Q5)

1. **Which query selects _all_ columns?**  
   A) `SELECT title, author FROM books;`  
   B) `SELECT books FROM *;`  
   C) `SELECT * FROM books;`  
   D) `SELECT ALL FROM books;`  
   **Answer:** C

2. **What does `*` mean in SQL?**  
   A) Primary key  
   B) All columns  
   C) All tables  
   D) All rows  
   **Answer:** B

3. **Select only the `title` column.**  
   A) `SELECT title FROM books;`  
   B) `SELECT * FROM books;`  
   C) `SELECT price FROM books;`  
   D) `SELECT author, price FROM books;`  
   **Answer:** A

4. **Retrieve both `title` and `author`.**  
   A) `SELECT title FROM author FROM books;`  
   B) `SELECT title, author FROM books;`  
   C) `GET title, author FROM books;`  
   D) `FETCH title, author FROM books;`  
   **Answer:** B

5. **Keyword used to fetch data:**  
   A) `GET`  
   B) `PULL`  
   C) `FETCH`  
   D) `SELECT`  
   **Answer:** D

---

## Part 2 – Aliases & Expressions (Q6–Q10)

6. **Rename `title` as `book_title`.**  
   A) `SELECT title = book_title FROM books;`  
   B) `SELECT title AS book_title FROM books;`  
   C) `SELECT title -> book_title FROM books;`  
   D) `SELECT book_title FROM books;`  
   **Answer:** B

7. **What does `SELECT 'Bookstore' AS source;` return?**  
   A) Table column  
   B) Fixed value `Bookstore`  
   C) Stored procedure  
   D) NULL column  
   **Answer:** B

8. **Calculate double the price.**  
   A) `SELECT price * 2 FROM books;`  
   B) `SELECT double(price) FROM books;`  
   C) `SELECT 2 * price IN books;`  
   D) `SELECT books.price * 2;`  
   **Answer:** A

9. **Effect of:** `SELECT title, price * 2 AS double_price FROM books;`  
   A) Title & original price  
   B) Title & double price  
   C) Title & NULL  
   D) Error  
   **Answer:** B

10. **Add a constant column.**  
    A) `SELECT title + 'Book' FROM books;`  
    B) `SELECT title, 'In stock' AS status FROM books;`  
    C) `SELECT title, book FROM books;`  
    D) `SELECT title, AS stock FROM books;`  
    **Answer:** B

---

## Part 3 – DISTINCT & Filtering (Q11–Q15)

11. **Return unique titles.**  
    A) `SELECT title FROM books;`  
    B) `SELECT UNIQUE title FROM books;`  
    C) `SELECT DISTINCT title FROM books;`  
    D) `SELECT title DISTINCT FROM books;`  
    **Answer:** C

12. **Purpose of `WHERE`:**  
    A) Join tables  
    B) Filter rows  
    C) Sort results  
    D) Group rows  
    **Answer:** B

13. **Find books by George Orwell.**  
    A) `SELECT * FROM books WHERE author = 'George Orwell';`  
    B) `SELECT * FROM books WHERE title = 'George Orwell';`  
    C) `SELECT * FROM books IF author = 'George Orwell';`  
    D) `FILTER books BY author = 'George Orwell';`  
    **Answer:** A

14. **Get books priced under ₹10.**  
    A) `SELECT * FROM books WHERE price > 10;`  
    B) `SELECT * FROM books WHERE price < 10;`  
    C) `SELECT price FROM books < 10;`  
    D) `SELECT price WHERE < 10;`  
    **Answer:** B

15. **`price IS NULL` checks:**  
    A) Price is 0  
    B) Price is missing  
    C) Price is negative  
    D) Price is numeric  
    **Answer:** B

---

## Part 4 – Sorting, LIMIT, OFFSET (Q16–Q22)

16. **Sort ascending by price.**  
    A) `ORDER books BY price;`  
    B) `SELECT * FROM books ORDER BY price;`  
    C) `SELECT * FROM books SORT price;`  
    D) `SORT * BY price;`  
    **Answer:** B

17. **Sort descending by price.**  
    A) `ORDER price FROM books DESC;`  
    B) `SELECT * FROM books ORDER BY price DESC;`  
    C) `SELECT * FROM books SORT DESC price;`  
    D) `ORDER BY price DOWN;`  
    **Answer:** B

18. **Effect of `LIMIT 3`:**  
    A) Top 3 expensive books  
    B) Any 3 random books  
    C) First 3 rows  
    D) Skips 3 rows  
    **Answer:** C

19. **Effect of `OFFSET 2`:**  
    A) Skips first 2 rows  
    B) Skips last 2 rows  
    C) Limits to 2 rows  
    D) Removes 2 rows  
    **Answer:** A

20. **Skip 2, show 2 rows.**  
    A) `LIMIT 2 SKIP 2`  
    B) `LIMIT 2 OFFSET 2`  
    C) `OFFSET 2 LIMIT 2`  
    D) Both **B** and **C**  
    **Answer:** D

21. **Rows with non‑NULL price.**  
    A) `WHERE price = NOT NULL`  
    B) `WHERE price != NULL`  
    C) `WHERE price IS NOT NULL`  
    D) `NOT NULL price`  
    **Answer:** C

22. **`WHERE price IS NULL` returns:**  
    A) All books  
    B) No books  
    C) Books with price  
    D) Books where price is missing  
    **Answer:** D

---

## Part 5 – Logical Operators (Q23–Q26)

23. **Orwell AND price > ₹10.**  
    A) `... OR ...`  
    B) `... AND ...`  
    C) `... OR author != ...`  
    D) Invalid  
    **Answer:** B

24. **`OR` operator means:**  
    A) Both true  
    B) Either true  
    C) First only  
    D) None true  
    **Answer:** B

25. **Price < ₹10 AND author ='Harper Lee'** returns:  
    A) One row  
    B) All rows  
    C) Zero rows  
    D) Error  
    **Answer:** A

26. **Correct use of `AND` / `OR`:**  
    A) `WHERE title AND price > 10`  
    B) `WHERE price > 10 OR title = '1984'`  
    C) `WHERE title = 1984 OR price = 10`  
    D) `WHERE OR title = '1984'`  
    **Answer:** B

---

## Part 6 – Comments & Syntax (Q27–Q30)

27. **Single‑line comment syntax:**  
    A) `#`  
    B) `//`  
    C) `--`  
    D) `/** */`  
    **Answer:** C

28. **Purpose of `;` in SQL:**  
    A) Start table  
    B) End query  
    C) Multiply data  
    D) Skip rows  
    **Answer:** B

29. **Keyword to rename columns:**  
    A) `RENAME`  
    B) `AS`  
    C) `SET`  
    D) `MODIFY`  
    **Answer:** B

30. **Valid SQL?** `SELECT title FROM books WHERE price < 15;`  
    A) Yes  
    B) No  
    **Answer:** A

---

Happy learning!

