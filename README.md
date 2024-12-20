# **Welcome to my SQL problem-solving repository!**

This repository is dedicated to solving SQL challenges from [HackerRank](https://www.hackerrank.com/). Here, you’ll find:

- **A variety of SQL problems**: From beginner to advanced levels, covering key concepts like SELECT queries, JOINs, subqueries, window functions, and more.
- **Well-documented solutions**: Each solution includes a clear explanation of the approach and the query used to solve the problem.
- **Learning-focused insights**: Perfect for anyone looking to strengthen their SQL skills or understand different problem-solving techniques.

## Revising the Select Query I
SELECT *  
FROM city  
WHERE countrycode LIKE 'USA' AND population>100000;  

## Revising the Select Query II  
SELECT name  
FROM city  
WHERE countrycode LIKE 'USA' AND population>120000;  

## Select All
SELECT *  
FROM city;  

## Select By ID
SELECT *  
FROM city  
WHERE id = 1661;  

## Japanese Cities' Attributes  
SELECT *  
FROM city  
WHERE countrycode LIKE 'JPN';

## Japanese Cities' Names
SELECT name  
FROM city  
WHERE countrycode LIKE 'JPN';  

## Weather Observation Station 1
SELECT city, state  
FROM station;  

## Weather Observation Station 3
SELECT DISTINCT city  
FROM station  
WHERE id%2=0;  

## Weather Observation Station 4
SELECT COUNT(city) - COUNT(DISTINCT city)  
FROM station;  

## Weather Observation Station 5
SELECT city, LENGTH(city)  
FROM station  
WHERE LENGTH(city) = (  
    SELECT MIN(LENGTH(city)) FROM station  
)  
ORDER BY city  
LIMIT 1;  
SELECT city, LENGTH(city)  
FROM station  
WHERE LENGTH(city) = (  
    SELECT MIN(LENGTH(city)) FROM station  
)  
ORDER BY city  
LIMIT 1;  

OR  

(SELECT city, LENGTH(city) AS city_len  
FROM station  
ORDER BY LENGTH(city), city  
LIMIT 1) UNION  
(SELECT city, LENGTH(city) AS city_len  
FROM station  
ORDER BY LENGTH(city) DESC, city  
LIMIT 1 )  

## Weather Observation Station 6
SELECT DISTINCT city    
FROM station    
WHERE city LIKE 'a%' OR city LIKE 'e%' OR city LIKE 'i%' OR city LIKE 'o%' OR city LIKE 'u%';    

## Weather Observation Station 7
SELECT DISTINCT city  
FROM station  
WHERE RIGHT(city, 1) IN ('a', 'e', 'i', 'o', 'u');  

## Weather Observation Station 8
SELECT DISTINCT city    
FROM station    
WHERE LEFT(city, 1) IN ('a', 'e', 'i', 'o', 'u') AND RIGHT(city, 1) IN ('a', 'e', 'i', 'o', 'u');    

## Weather Observation Station 9
SELECT DISTINCT city    
FROM station    
WHERE LEFT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u');    

## Weather Observation Station 10
SELECT DISTINCT city    
FROM station    
WHERE RIGHT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u');    

## Weather Observation Station 11
SELECT DISTINCT city    
FROM station    
WHERE LEFT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u') OR RIGHT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u');    

## Weather Observation Station 12
SELECT DISTINCT city    
FROM station    
WHERE LEFT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u') AND RIGHT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u');    

## Higher Than 75 Marks
SELECT name    
FROM students    
WHERE marks>75    
ORDER BY RIGHT(name, 3), id;    

## Employee Names
SELECT name    
FROM employee    
ORDER BY name;    

## Employee Salaries
SELECT name    
FROM employee    
WHERE salary>2000 AND months<10    
ORDER BY employee_id;    

## Type of Triangle    
SELECT     
    CASE    
        WHEN A+B>C AND B+C>A AND A+C>B THEN    
            CASE    
                WHEN A=B AND B=C AND C=A THEN "Equilateral"    
                WHEN A=B OR B=C OR C=A THEN "Isosceles"    
                ELSE "Scalene"    
            END    
        ELSE "Not A Triangle"    
    END    
FROM triangles;    

