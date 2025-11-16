# Data-Insertion-and-Handling-Nulls
Use INSERT INTO for Adding Rows
Syntax:

sql
INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);
Example:
Suppose you have a table called students with columns id, name, age.

sql
INSERT INTO students (id, name, age) VALUES (1, 'Alice', 20);
INSERT INTO students (id, name, age) VALUES (2, 'Bob', 22);
2. Handle Missing Values Using NULL or Default
If a column is missing, SQL will use NULL (if allowed) or the column’s DEFAULT value if defined.

Example:
If age is missing and allows NULL:

sql
INSERT INTO students (id, name) VALUES (3, 'Charlie');
This adds Charlie with NULL for age.

If there's a default value:
Suppose age has DEFAULT 18.

sql
INSERT INTO students (id, name) VALUES (4, 'David');
Now David's age will be 18.

3. Use UPDATE and DELETE with WHERE Conditions
UPDATE Syntax:

sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
Example: Update Bob’s age:

sql
UPDATE students SET age = 23 WHERE name = 'Bob';
DELETE Syntax:

sql
DELETE FROM table_name WHERE condition;
Example: Remove student named Alice:

sql
DELETE FROM students WHERE name = 'Alice';

