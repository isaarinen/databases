# Exercises 6: Aggregate Queries
### Exercise 1

![screenshot](6-1.png)
``select max(elevation_ft) from airport;``
### Exercise 2

![screenshot](6-2.png)
``select continent, count(*) from country group by continent;``
### Exercise 3

![screenshot](6-3.png)
``select game.screen_name, count(*) from game join goal_reached on game.id = goal_reached.game_id group by game.screen_name;``
### Exercise 4

![screenshot](6-4.png)
``select screen_name from game where co2_consumed in(select min(co2_consumed) from game);``
### Exercise 5

![screenshot](6-5.png)
``select country.name, count(*) from airport, country where airport.iso_country = country.iso_country group by name order by count(*) desc limit 50;``
### Exercise 6

![screenshot](6-6.png)
``select country.name from airport, country where airport.iso_country = country.iso_country group by name having count(*) > 1000;``
### Exercise 7

![screenshot](6-7.png)
``select name from airport where elevation_ft in(select max(elevation_ft) from airport);``
### Exercise 8

![screenshot](6-8.png)
``select name from country where iso_country in(select iso_country from airport where elevation_ft in(select max(elevation_ft) from airport));``
### Exercise 9

![screenshot](6-9.png)
``select count(*) from goal_reached where game_id in(select id from game where screen_name = 'Vesa');``
### Exercise 10

![screenshot](6-10.png)
``select name from airport where latitude_deg in(select min(latitude_deg) from airport);``