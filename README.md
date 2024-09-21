# Databases-He Chun
# Week [3]
？？？？
### Assignment 2
SELECT * FROM example 
![screenshot](schreenshot-file-name.png)

### Assignment 3
#1
SELECT 
    country.name AS "country name", 
    airport.name AS "airport name"
FROM 
    airport, country
WHERE 
    airport.iso_country = country.iso_country 
    AND country.name = 'Iceland';
![3 1](https://github.com/user-attachments/assets/b0e92fdd-cdc4-47d1-a58f-743bce1d3ff3)

#2
select 
airport.name as "airport name"
from 
airport, country
where 
airport.iso_country = country.iso_country 
and country.name = "France" 
and airport.type = "large_airport";
![3 2](https://github.com/user-attachments/assets/433e5731-25b1-4733-badc-9ea1388882f0)

#3
select country.name as country_name, airport.name as airport_name
from airport, country
where airport.iso_country = country.iso_country and country.continent = "AN";
![3 3](https://github.com/user-attachments/assets/23bb71a6-6e48-4d04-af18-98bec8a05b7c)

#4
select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
![3 4](https://github.com/user-attachments/assets/6a1c5c92-1a71-4b0b-8f60-f67cf11ee3ce)


#5
select elevation_ft * 0.3048 as elevation_m
from airport, game
where location = ident and screen_name = "Heini";
![3 5](https://github.com/user-attachments/assets/a8c4c030-f103-4215-b70e-9d33b6fa5ac4)

#6
select name
from airport, game
where location = ident and screen_name = "Ilkka";
![3 6](https://github.com/user-attachments/assets/3288b880-cb4b-4897-8867-2f465346d0bd)

#7
select country.name
from airport, game, country
where location = ident 
and airport.iso_country = country.iso_country  
and screen_name = "Ilkka";
![3 7](https://github.com/user-attachments/assets/f2e772fb-f6cb-4f40-b555-d8c1cf45e378)

#8
select name
from goal, goal_reached, game
where game.id = game_id
and goal.id = goal_id
and screen_name = "Heini";
![3 8](https://github.com/user-attachments/assets/2a931243-912e-42a5-bcb8-5d1c40a8ac19)

#9
select airport.name
from airport, game, goal, goal_reached
where ident = location
and game.id = game_id
and goal.id = goal_id
and screen_name = "Ilkka"
and goal.name = "CLOUDS";
![3 9](https://github.com/user-attachments/assets/79265111-1b7d-4bcb-b985-b18c8c1c27d3)

#10
select country.name
from country, airport, game, goal, goal_reached
where airport.iso_country = country.iso_country 
and ident = location 
and game.id = game_id 
and goal.id = goal_id 
and screen_name = "Ilkka" 
and goal.name = "CLOUDS";
![3 10](https://github.com/user-attachments/assets/1b4f8a9f-3f38-46c5-9344-be8405c5ea63)








# Week [4]

### Assignment 4
SELECT * FROM example 
![screenshot](schreenshot-file-name.png)



### Assignment 5
SELECT * FROM example WHERE column = 'value' 
![screenshot](schreenshot-file-name.png)


# Week [5]

### Assignment 6
SELECT * FROM example 
![screenshot](schreenshot-file-name.png)

### Assignment 7
SELECT * FROM example WHERE column = 'value' 
![screenshot](schreenshot-file-name.png)

# Week [6]

### Assignment 8
SELECT * FROM example 
![screenshot](schreenshot-file-name.png)



