I build this password Manager where people can store there store , edit , delete and view
their userId and password related to various website.

![image](https://user-images.githubusercontent.com/89289293/143278064-bb016793-a717-4bc4-bdb4-f618ccc3145f.png)

This is index page where user will have two option , one for login if he is already a regitered user or to register if you are visiting here for first time.

![image](https://user-images.githubusercontent.com/89289293/143281261-25ee15f4-a93f-4921-b5f7-3c4a547d10f2.png)
This is registration page where user can register in order to login to use this password manager.
while registration 
1. if user uses already existing email in database (means someone has already registered using that mail) and he will get message saying email already exist.
2. if user miss any one of entry then he will get message saying Email and password are required.
3. if user forgot to use to @ in email then he will get message saying Email must have an at-sign (@).
if everything is ok then user email id and password will be stored in 'users' table (Used SHA256 hashing algo for password encryption) and user will be redirected to login page.

if user click on cancel button he will be redirected to index page.

(cookie is key value pair which we store in browser for fixed time so that it can be used by that website when you visit it next time)
(Session :used to manage information across different pages)

I have used session to show message

![image](https://user-images.githubusercontent.com/89289293/143311743-a3506001-5983-4722-a98c-d01fb724fa98.png)

while login 
1. if user entered emailid and password ,it will matched from database if does not match , user will get message saying wrong email and password.
2. if user miss any one of entry then he will get message saying Email and password are required.
3. if user forgot to use to @ in email then he will get message saying Email must have an at-sign (@).
if everything is ok then user will be redirected to view page.

if user click on cancel button he will be redirected to index page.


![image](https://user-images.githubusercontent.com/89289293/143314075-944a08a7-16a3-4081-a547-88adffe8acb6.png)
this is view page where user can view, edit and delete his entries.


![image](https://user-images.githubusercontent.com/89289293/143314508-b807d399-32d7-40ec-b61f-55d88e292e6d.png)

this is add page where user can add his entry.

![image](https://user-images.githubusercontent.com/89289293/143315098-7a8938c6-62de-4182-aa05-09e14fd689b3.png)

this is edit page where user can udpate his entry and i have used GET variable for user_id to update that entry.

![image](https://user-images.githubusercontent.com/89289293/143316120-2124cdf4-1791-41bc-aaba-f182d10cf7f7.png)

this is delete page , user needs to confirm before deleting entry and i have used GET variable for user_id to delete that entry.

About PDO : Represents a connection between PHP and a database server
PDO::prepare — Prepares a statement for execution and returns a statement object. Prepares an SQL statement to be executed by the PDOStatement::execute() method.
PDO::exec() executes an SQL statement in a single function call, returning the number of rows affected by the statement.

PDOStatement::fetch — Fetches the next row from a result set. Fetches a row from a result set associated with a PDOStatement object. The mode parameter determines how PDO returns the row.

mode : Controls how the next row will be returned to the caller. This value must be one of the PDO::FETCH_* constants, defaulting to value of PDO::ATTR_DEFAULT_FETCH_MODE (which defaults to PDO::FETCH_BOTH).
PDO::FETCH_ASSOC: returns an array indexed by column name as returned in your result set

