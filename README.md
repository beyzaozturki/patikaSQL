# SQL Exercises 
**This repository is prepared for Patika.dev SQL tutorials. Free and open source PostgreSQL was used as the database management system. You can find examples to practice SQL in this repository.**
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
