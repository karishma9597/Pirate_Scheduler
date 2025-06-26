# Pirate_Scheduler
This is a scheduler I made for fun! You can store and search caller's names. It then scans the database for important information and determines if they are a customer, if they have called before. Pirate Scheduler logs the dates of all communications as well as allows for setting callback times
Pirate Scheduler logs the dates of all communications as well as allows for setting callback times and can tell if the caller is a customer or not.

I would reccomend downloading MySQL workbench (GUI for database). Here is the link for MySQL Workbench ---> https://dev.mysql.com/downloads/workbench/

Inside of your database, create two tables.

Table Name: customer_calls, Columns: Customer_Name varchar(50), Time_Of_Call datetime, Notes varchar(250), Callback_time datetime, Callback_time_2 datetime, id int AI PK

Table 2 Name: order_info, Columns: Order_ID int AI PK, Customer_Name varchar(45), Notes varchar(250), Customer_Paid float, Date_Of_Purchase datetime, Item_Purchased varchar(45), Item_ID int

Here are sql queries to save you time:

CREATE TABLE schedules.customer_calls ( Customer_Name varchar(50), Time_Of_Call datetime, Notes varchar(250), Callback_time datetime, Callback_time_2 datetime, id int AUTO_INCREMENT PRIMARY KEY );

CREATE TABLE schedules.order_info ( Order_ID int AUTO_INCREMENT PRIMARY KEY, Customer_Name varchar(45), Notes varchar(250), Customer_Paid float, Date_Of_Purchase datetime, Item_Purchased varchar(45), Item_ID int );

Once you have your two tables created.

Open boringstuff.py this file is where your database username,password, ip address, and schema (database's name) live. if you use the sql queries noted above. Your schema's name will be "schedules".

You fill in your User_Name, Password, Schema.

After this you should be ready to run Scheduler.py (the GUI) and start making queries. If you have issues with connecting to your database. Make sure you are hosting your database on your local server, and check connection config settings @ the home screen of MySQL workbench.
