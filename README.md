# SQL Exercises 
**This repository is prepared for Patika.dev SQL tutorials. Free and open source PostgreSQL was used as the database management system. You can find examples to practice SQL in this repository.**
&nbsp;

## Local Environment Setup
Follow the steps provided below to setup the local environment with PostgreSQL and database

` Step 1.`  Downloading PostgreSQL

First, we will need to install PostgreSQL on your local machine. The instructions below provide detailed description of the steps we need to take.

Installing PostgreSQL for Windows:

http://www.postgresqltutorial.com/install-postgresql/

Installing PostgreSQL for Mac OS:

https://www.postgresql.org/download/macosx/

Note: We need to write down the database superuser (postgres) password as we will need it to create the Sakila database once we have installed the PostgreSQL server.

`Step 2.`  Downloading Sakila database

Once PostgreSQL server is installed, we will need to download the Movie database from this page: PostgreSQL Sample Database

Scroll down and click on the orange "Download DVD Rental Sample Database" button.

This will download a zipped file, and you will need to extract the dvdrental.tar file.

` Step 3.`  Loading database

The next step is to load the DVD Rental database into our PostgreSQL server on our machine. We recommend using the PgAdmin tool. We can find the instructions to do so on the following link: Load PostgreSQL Sample Database.

The instructions are down ⅓ on this page under the header “Load the DVD Rental database using pgAdmin tool” .

Now, we need to follow the instructions all the way through the header titled "Verify the loaded sample database."

Once we have followed the instructions through the end of "Verify the loaded sample database.", we have now loaded the dvdrental sample database into our local PostgreSQL database server.

` Step 4.`  Connecting back to the PostgreSQL server:

Now, we will relaunch PgAdmin III and click on the PostgreSQL server within the Object browser and enter our superuser (postgres) password.

` Step 5.`  Connecting to the DVD rental database:

Next, we will click on the plus sign next to Databases to access the DVD rental database.

` Step 6.`  Choose the DVD Rental database

Choose the dvdrental database under Databases.

We are now linked to the DVD rental database.

` Step 7.`  Running Queries on your dvdrental database

Now, we are ready to run some queries. For that, we need to click on the SQL icon with a magnifying glass

&nbsp;

- ### SQL Basics
   🔸 ***<a href='#Exercises 1'>Exercises 1</a><br>***
   🔸 ***<a href='#Exercises 2'>Exercises 2</a><br>***
   🔸 ***<a href='#Exercises 3'>Exercises 3</a><br>***
   🔸 ***<a href='#Exercises 4'>Exercises 4</a><br>***
- ### SQL Basics II
   🔸 ***<a href='#Exercises 5'>Exercises 5</a><br>***
   🔸 ***<a href='#Exercises 6'>Exercises 6</a><br>***
   🔸 ***<a href='#Exercises 7'>Exercises 7</a><br>***
- ### Working With Tables
   🔸 ***<a href='#Exercises 8'>Exercises 8</a><br>***
- ### JOINs
   🔸 ***<a href='#Exercises 9'>Exercises 9</a><br>***
   🔸 ***<a href='#Exercises 10'>Exercises 10</a><br>***
   🔸 ***<a href='#Exercises 11'>Exercises 11</a><br>***
- ### Subqueries
   🔸 ***<a href='#Exercises 12'>Exercises 12</a><br>***

<br/><br/>

> ## ***<p id = 'Exercises 1' > Exercises 1 </p>***
 _Sort the data in the title and description columns in the film table._
~~~sql
SELECT title,description FROM film;
~~~
_Sort the data in all the columns in the film table with the conditions that the movie length is greater than 60 AND less than 75._
~~~sql
SELECT * FROM film 
WHERE length > 60 AND length < 75;
~~~
_Sort the data in all columns in the film table with rental_rate 0.99 AND replacement_cost 12.99 OR 28.99._
~~~sql
SELECT * FROM film 
WHERE rental_rate = 0.99 AND replacement_cost = 12.99 OR replacement_cost = 28.99;
~~~
_What is the value in the last_name column of the customer whose value is 'Mary' in the first_name column in the Customer table?_
~~~sql
SELECT last_name FROM customer 
WHERE first_name = 'Mary';
~~~
_Sort the data in the film table whose length is NOT greater than 50 and at the same time the rental_rate value is NOT 2.99 or 4.99._
~~~sql
SELECT * FROM film 
WHERE NOT(rental_rate = 4.99 OR rental_rate = 2.99) AND NOT length > 50;
~~~
