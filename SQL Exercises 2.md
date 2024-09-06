# Exercises 2: Single Table Queries

### Exercise 1

![screenshot](2-1.png)
``select * from goal;``
### Exercise 2

![screenshot](2-2.png)
``select name, type from airport where iso_country = "FI";``
### Exercise 3

![screenshot](2-3.png)
``select name from airport where iso_country = "FI" order by name;``
### Exercise 4

![screenshot](2-4.png)
``select name, type from airport where iso_country = "FI" order by type, name;``
### Exercise 5

![screenshot](2-5.png)
``select name from country where name like "F%;"``
### Exercise 6

![screenshot](2-6.png)
``select name from country where name like "%F%";``
### Exercise 7

![screenshot](2-7.png)
``select location from game where screen_name = "Vesa";``
### Exercise 8

![screenshot](2-8.png)
``select co2_consumed from game where screen_name = "Ilkka";``
### Exercise 9
``select distinct co2_budget from game;``
![screenshot](2-9.png)

### Exercise 10

![screenshot](2-10.png)
``SELECT screen_name, co2_budget, co2_consumed, @co2_left := co2_budget - co2_consumed AS co2_left from game where screen_name = "Ilkka";``