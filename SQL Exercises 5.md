# Exercises 5: Subqueries
### Exercise 1

![screenshot](5-1.png)
``select name from country where iso_country in( select iso_country from airport where name like 'Satsuma%');``
### Exercise 2
![screenshot](5-2.png)
``select name from airport where iso_country in( select iso_country from country where name = "Monaco");``
### Exercise 3
![screenshot](5-3.png)
``select screen_name from game where id in(select game_id from goal_reached where goal_id in(select id from goal where name = 'CLOUDS'));``
### Exercise 4
![screenshot](5-4.png)
``select name from country where iso_country not in(select
iso_country from airport);``
### Exercise 4
![screenshot](5-5.png)
``select name from goal where id not in(select goal_id from goal_reached where game_id in(select id from game where screen_name = 'Heini'));``