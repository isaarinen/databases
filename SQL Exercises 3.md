
# Exercises 3: Multiple Table Queries
### Exercise 1

![screenshot](3-1.png)
``select country.name as "country name", airport.name as "airport name" from country, airport where airport.iso_country = country.iso_country and country.name = "Iceland";``
### Exercise 2

![screenshot](3-2.png)
``select airport.name as "airport name" from country, airport where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";``
### Exercise 3

![screenshot](3-3.png)
``select country.name AS country_name, airport.name AS airport_name from airport, country where airport.iso_country = country.iso_country and  country.continent = "AN";``
### Exercise 4

![screenshot](3-4.png)
``select airport.elevation_ft from airport, game where game.location = airport.gps_code and game.screen_name = "Heini";``
### Exercise 5

![screenshot](3-5.png)
``select airport.elevation_ft * 0.3048 AS elevation_m from airport, game where game.location = airport.gps_code and game.screen_name = "Heini";``
### Exercise 6

![screenshot](3-6.png)
``select airport.name from airport, game where game.location = airport.gps_code and game.screen_name = "Ilkka";``
### Exercise 7

![screenshot](3-7.png)
``select country.name from airport, game, country where game.location = airport.gps_code and country.iso_country = airport.iso_country and game.screen_name = "Ilkka";``
### Exercise 8

![screenshot](3-8.png)
``select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";``
### Exercise 9
``select airport.name from game, goal, goal_reached, airport where airport.gps_code = game.location and game.screen_name = "Ilkka" and goal_reached.game_id = game.id and goal_reached.goal_id = goal.id and goal.name = "CLOUDS";``
![screenshot](3-9.png)

### Exercise 10

![screenshot](3-10.png)
``select country.name from game, goal, goal_reached, airport, country where country.iso_country = airport.iso_country  and airport.gps_code = game.location and game.screen_name = "Ilkka" and goal_reached.game_id = game.id and goal_reached.goal_id = goal.id and goal.name = "CLOUDS";``