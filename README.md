# learn-sql (task answer)

SQL Lesson 1: SELECT queries 101
 
1.	SELECT title FROM movies;
2.	SELECT director FROM movies;
3.	SELECT title, director FROM movies;
4.	SELECT title, year FROM movies;
5.	SELECT * FROM movies;

SQL Lesson 2: Queries with constraints (Pt. 1)
 
1.	SELECT * FROM movies where id=6;
2.	SELECT * FROM movies where year between 2000 and 2010;
3.	SELECT * FROM movies where year not between 2000 and 2010;
4.	SELECT title, year FROM movies where id<=5;

SQL Lesson 3: Queries with constraints (Pt. 2)
 
1.	SELECT * FROM movies where title like "%toy story%";
2.	SELECT * FROM movies where director like "%John Lasseter%";
3.	SELECT title, director FROM movies where director!="John Lasseter";
4.	SELECT * FROM movies where title like "%WALL%";

SQL Lesson 4: Filtering and sorting Query results
 
1.	SELECT distinct director FROM movies order by director asc;
2.	SELECT distinct title FROM movies order by year desc limit 4;
3.	SELECT distinct title FROM movies order by title asc limit 5;
4.	SELECT title FROM movies order by title limit 5 offset 5;


SQL Review: Simple SELECT Queries
 
1.	SELECT city, population FROM north_american_cities where country like"canada";
2.	SELECT city FROM north_american_cities where country like "united states" order by latitude desc;
3.	SELECT city FROM north_american_cities where longitude < -87.629798 order by longitude asc;
4.	SELECT city FROM north_american_cities where country like "mexico" order by population desc limit 2;
5.	SELECT city, population FROM north_american_cities where country like "united states" order by population desc limit 2 offset 2;

SQL Lesson 6: Multi-table queries with JOINs
 
1.	SELECT title,Domestic_sales,International_sales FROM movies inner join boxoffice on id = Movie_id;
2.	SELECT title,Domestic_sales,International_sales FROM movies inner join boxoffice on id = Movie_id where International_sales>Domestic_sales;
3.	SELECT title FROM movies inner join boxoffice on id = Movie_id order by rating desc;

SQL Lesson 7: OUTER JOINs
 
1.	SELECT distinct building FROM employees;
2.	SELECT * FROM Buildings;
3.	SELECT distinct Building_name, Role FROM Buildings left join Employees on Building_name = Building;
