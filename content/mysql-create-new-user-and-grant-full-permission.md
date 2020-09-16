[Back to Home](../index.md)


## Create new user and grant full permission in MySQL 

### Step 1: Login to your MySQL Server with **root**
Take note that **root** user won't be able to access MySQL server remotely. Therefore, we have to create new user for remote access.
After logging in create new user as follow.


`CREATE USER 'admin'@'%' IDENTIFIED BY 'youradminpassword';`

### Step 2: Grant all privileges to newly create user in our case **admin**


`GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%' WITH GRANT OPTION;`


### Step 3: Flush to take affect immediately

`FLUSH PRIVILEGES;`

That's all it takes.

### In case you are not satisfied with your password

`SET PASSWORD FOR 'admin'@'%' = PASSWORD('yournewpassword');`
