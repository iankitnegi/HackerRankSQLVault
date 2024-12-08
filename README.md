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




















