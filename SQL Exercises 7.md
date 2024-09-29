# Exercises 7: Update Queries
### Exercise 1

![screenshot](7-1.png)
``update game set location = (select ident from airport where name = 'Nottingham Airport'), co2_consumed = (select co2_consumed from game where screen_name = 'Vesa') + 500 where id in(select id from game where screen_name = 'Vesa');``

### Exercise 2

![screenshot](7-2.png)

### Exercise 3

![screenshot](7-3.png)
``delete from goal_reached; select * from goal_reached;``
### Exercise 4

![screenshot](7-4.png)
``delete from game; select * from game;``