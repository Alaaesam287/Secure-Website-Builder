
Most SQL injection vulnerabilities occur within the `WHERE` clause of a `SELECT` query. 

However, SQL injection vulnerabilities can occur at any location within the query, and within different query types. Some other common locations where SQL injection arises are:

- In `UPDATE` statements, within the updated values or the `WHERE` clause.
- In `INSERT` statements, within the inserted values.
- In `SELECT` statements, within the table or column name.
- In `SELECT` statements, within the `ORDER BY` clause.


1. Retrieving Hidden Data:

	SELECT * FROM products WHERE category = 'Gifts'--' AND released = 1 -->> -- means comment so the rest of the query will be commented
	
	`OR 1=1`  if it appears to be harmless in the context you're injecting into,. If your condition reaches an `UPDATE` or `DELETE` statement, for example, it can result in an accidental loss of data like DELETE * FROM users WHERE username = '' OR 1=1 --'; --> This will delete all.


2. Subverting application logic:
	SELECT * FROM users WHERE username = 'administrator'--' AND password = '' -->> This will login based on the username only

3. SQL injection UNION attacks:
	When an application is vulnerable to SQL injection, and the results of the query are returned within the application's responses, you can use the `UNION` keyword to retrieve data from other tables within the database.--> SELECT a, b FROM table1 UNION SELECT c, d FROM table2
	
	






















Whatever I input to input field goes to Database
So
SELECT * FROM table WHERE name="" OR 1=1; --> this is true as it runs queries on the table and each row is true due to 1=1 so it will return everything
- WHERE =="==" OR 1=1; =="==   the Highlighted is the original quotes
- also if we have a URL that has a file.php and has a parameter this parameter can be attacked using sqli 
- To find the parameter use the tool in linux arjun -u http://blabla/file.php in linux


