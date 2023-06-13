# mysql-database

Steps:
1. # configured aws provider with proper credentials
2. # use data source to get all avalablility zones in region
3. # create a default subnet in the first az if one does not exit
4. # create a default subnet in the second az if one does not exit
# create security group for the web server
# create security group for the database
# create the subnet group for the rds instance
# create the rds instance



STEPS IN CREATING MYSQL database
## Step 1: Update the system
sudo apt update
## Step 2: Install MySql
sudo apt install mysql-server
## Step 3: Check the Status of MySql (Active or Inactive)
sudo systemctl status mysql
## Step 4: Login to MySql as a root
sudo mysql
## Step 5: Update the password for the MySql Server
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'place-your-password-here';
FLUSH PRIVILEGES;
## Step 6: Test the MySql server if it is working by running sample sql queries
CREATE DATABASE mysql_test;
USE mysql_test;
CREATE TABLE table1 (id INT, name VARCHAR(45));
INSERT INTO table1 VALUES(1, 'Virat'), (2, 'Sachin'), (3, 'Dhoni'), (4, 'ABD');
SELECT * FROM table1;