# SQL Exercises for Patika.dev
**This repository is prepared for Patika.dev SQL tutorials. Free and open source PostgreSQL was used as the database management system. You can find examples to practice SQL in this repository.**
&nbsp;

⚡ ***<a href='#Exercises 1'>Exercises 1</a><br>***
⚡ ***<a href='#Exercises 2'>Exercises 2</a><br>***
⚡ ***<a href='#Exercises 3'>Exercises 3</a><br>***
⚡ ***<a href='#Exercises 4'>Exercises 4</a><br>***
⚡ ***<a href='#Exercises 5'>Exercises 5</a><br>***
⚡ ***<a href='#Exercises 6'>Exercises 6</a><br>***
⚡ ***<a href='#Exercises 7'>Exercises 7</a><br>***
⚡ ***<a href='#Exercises 8'>Exercises 8</a><br>***
⚡ ***<a href='#Exercises 9'>Exercises 9</a><br>***
⚡ ***<a href='#Exercises 10'>Exercises 10</a><br>***
⚡ ***<a href='#Exercises 11'>Exercises 11</a><br>***
⚡ ***<a href='#Exercises 12'>Exercises 12</a><br>***

<br/><br/>

> ## ***<p id = 'Exercises 1' > Exercises 1 </p>***
 _Sort the data in the title and description columns in the film table._
~~~sql
SELECT title,description FROM film;
~~~
#### Sort the data in all the columns in the film table with the conditions that the movie length is greater than 60 AND less than 75.
~~~sql
SELECT * FROM film 
WHERE length > 60 AND length < 75;
~~~
#### Film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
~~~sql
SELECT * FROM film WHERE rental_rate = 0.99 AND replacement_cost = 12.99 OR replacement_cost = 28.99
~~~
#### Customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
~~~sql
SELECT last_name FROM customer where first_name = 'Mary';
Cevap : Smith
~~~
#### Film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
~~~sql
SELECT * FROM film WHERE NOT(rental_rate = 4.99 OR rental_rate = 2.99) AND NOT length > 50;
~~~
