# Databases-He Chun
# Week [3]
### Assignment 2
#2.1
select * from goal;
![2 1](https://github.com/user-attachments/assets/70483923-d1c0-4e5b-901e-f6fc7d512490)

#2.2
select name,type from airport
where iso_country = "FI";
![2 2](https://github.com/user-attachments/assets/81f31f87-e514-4b8b-aa65-802cb45b7233)

#2.3
select name from airport
where iso_country = "FI" order by name asc;
![2 3](https://github.com/user-attachments/assets/b75d04c8-0a16-4943-829c-ea6fca567507)

#2.4
select name,type from airport
where iso_country = "FI" order by type asc , name asc;
![2 4](https://github.com/user-attachments/assets/398b35ba-fb45-4a4d-98f7-2fd4976fee18)

#2.5
select name from country where name like  "F%";
![2 5](https://github.com/user-attachments/assets/bebd1df5-1750-4ae9-be97-a5b34e613ca2)

#2.6
select name from country where name like  "%F%";
![2 6](https://github.com/user-attachments/assets/de4cd47b-c618-4a44-82a7-213ea53f0d78)

#2.7
select location from game where screen_name = "Vesa" ;
![2 7](https://github.com/user-attachments/assets/e6b2fa71-b595-4fb3-b5ac-e7b7de06885f)

#2.8
select co2_consumed from game where screen_name = "Ilkka";
![2 8](https://github.com/user-attachments/assets/50ab0763-e9ba-4f62-8ec7-13bbdd9a3949)

#2.9
select DISTINCT co2_budget from game where co2_budget = "10000";
![2 9](https://github.com/user-attachments/assets/02d0f614-d9de-4afe-aba6-efdda99aba6e)

#2.10
select screen_name , co2_budget, co2_consumed ,
       (co2_budget - co2_consumed) as co2_left
from game
where screen_name = "Ilkka";
![2 10](https://github.com/user-attachments/assets/c7e335cc-5c7e-4098-ad51-b0d9bc7e17ac)

### Assignment 3
#3.1
SELECT 
    country.name AS "country name", 
    airport.name AS "airport name"
FROM 
    airport, country
WHERE 
    airport.iso_country = country.iso_country 
    AND country.name = 'Iceland';
![3 1](https://github.com/user-attachments/assets/b0e92fdd-cdc4-47d1-a58f-743bce1d3ff3)

#3.2
select 
airport.name as "airport name"
from 
airport, country
where 
airport.iso_country = country.iso_country 
and country.name = "France" 
and airport.type = "large_airport";
![3 2](https://github.com/user-attachments/assets/433e5731-25b1-4733-badc-9ea1388882f0)

#3.3
select country.name as country_name, airport.name as airport_name
from airport, country
where airport.iso_country = country.iso_country and country.continent = "AN";
![3 3](https://github.com/user-attachments/assets/23bb71a6-6e48-4d04-af18-98bec8a05b7c)

#3.4
select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
![3 4](https://github.com/user-attachments/assets/6a1c5c92-1a71-4b0b-8f60-f67cf11ee3ce)


#3.5
select elevation_ft * 0.3048 as elevation_m
from airport, game
where location = ident and screen_name = "Heini";
![3 5](https://github.com/user-attachments/assets/a8c4c030-f103-4215-b70e-9d33b6fa5ac4)

#3.6
select name
from airport, game
where location = ident and screen_name = "Ilkka";
![3 6](https://github.com/user-attachments/assets/3288b880-cb4b-4897-8867-2f465346d0bd)

#3.7
select country.name
from airport, game, country
where location = ident 
and airport.iso_country = country.iso_country  
and screen_name = "Ilkka";
![3 7](https://github.com/user-attachments/assets/f2e772fb-f6cb-4f40-b555-d8c1cf45e378)

#3.8
select name
from goal, goal_reached, game
where game.id = game_id
and goal.id = goal_id
and screen_name = "Heini";
![3 8](https://github.com/user-attachments/assets/2a931243-912e-42a5-bcb8-5d1c40a8ac19)

#3.9
select airport.name
from airport, game, goal, goal_reached
where ident = location
and game.id = game_id
and goal.id = goal_id
and screen_name = "Ilkka"
and goal.name = "CLOUDS";
![3 9](https://github.com/user-attachments/assets/79265111-1b7d-4bcb-b985-b18c8c1c27d3)

#3.10
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
#4.1
select country.name as "country name", airport.name as "airport name"
from country
inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";
![4 1](https://github.com/user-attachments/assets/c4638469-659c-4d0a-b152-d06e9e9976bc)

#4.2
select screen_name, airport.name
from game inner join airport on location = ident;
![4 2](https://github.com/user-attachments/assets/e9afc47a-d625-4f79-a69b-3edce5f6832f)

#4.3
select screen_name, country.name from game 
inner join airport on location = ident 
inner join country on airport.iso_country = country.iso_country;
![4 3](https://github.com/user-attachments/assets/c6d6d52a-3038-430d-8a1c-2c4a5daef574)

#4.4
select airport.name, game.screen_name from airport
left join game on ident = location
where name like "%Hels%";
![4 4](https://github.com/user-attachments/assets/1cfb4552-d7cf-44b2-841d-444bee2f80f3)

#4.5
select name, screen_name from goal 
left join goal_reached on goal.id = goal_id  
left join game on game.id = game_id;
![4 5](https://github.com/user-attachments/assets/b67da3f0-1132-492d-83aa-327aab6e0aaa)


### Assignment 5
#5.1
select country.name from country
inner join airport on country.iso_country = airport.iso_country
where airport.name like "Satsuma%";
![5 1](https://github.com/user-attachments/assets/5291bb06-b5e0-4d3d-94e6-58c4398d235f)

#5.2
select name from airport 
where iso_country in( select iso_country from country where name = "Monaco");
![5 2](https://github.com/user-attachments/assets/e6d0d453-bbda-497c-9e12-9f49e07a5a57)

#5.3
SELECT screen_name 
FROM game 
WHERE id IN (
    SELECT game_id 
    FROM goal_reached 
    WHERE goal_id IN (
        SELECT id 
        FROM goal 
        WHERE name = "CLOUDS"
    )
);
![5 3](https://github.com/user-attachments/assets/dc0007e3-0819-4a25-aa77-d2a54b4b6c47)

#5.4
select country.name
from country
where iso_country not in
(select airport.iso_country
from airport);
![5 4](https://github.com/user-attachments/assets/a6467833-4704-4a93-9eba-d0932b559550)

#5.5
select name from goal
where id not in(
select goal.id
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini"
);
![5 5](https://github.com/user-attachments/assets/aee44f86-8674-41a4-bd60-331a023de5fd)


# Week [5]

### Assignment 6
#6.1
select max(elevation_ft)
from airport;
![6 1](https://github.com/user-attachments/assets/ef51b8d1-2bfb-4480-857f-4aeba182030b)

#6.2
select continent, count(*)
from country
group by continent;
![6 2](https://github.com/user-attachments/assets/70b48180-53f1-48c3-afd6-a359a42c16b6)

#6.3
from game, goal_reached
where id = game_id
group by screen_name;
![6 3](https://github.com/user-attachments/assets/0ec7ceca-45eb-4d2e-852e-aefdc2979abe)

#6.4
select screen_name from game
where co2_consumed in(select min(co2_consumed) from game);
![6 4](https://github.com/user-attachments/assets/064e286c-77fe-4445-9e4f-3c42ede26b41)


#6.5
select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;
![6 5](https://github.com/user-attachments/assets/7498d845-d00d-438d-93b4-2ce7cb346cc8)

#6.6
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;
![6 6](https://github.com/user-attachments/assets/c35a538e-73f2-4766-bd3b-6b777e5df537)

#6.7
select airport.name from airport
where elevation_ft in(
    select max(elevation_ft) from airport
    );
![6 7](https://github.com/user-attachments/assets/d48892cb-89a7-4bcb-9b82-94bcf5870abf)

#6.8
select name from country
where iso_country in (
    select iso_country from airport
    where elevation_ft in(
    select max(elevation_ft)
    from airport)
); 
![6 8](https://github.com/user-attachments/assets/7978cfae-8cb3-494b-84e4-2869cff7fa9b)

#6.9
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;
![6 9](https://github.com/user-attachments/assets/3d35eb20-5108-4d24-a16c-4ee95f5c21ba)

#6.10
select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);
![6 10](https://github.com/user-attachments/assets/7897368a-ad2a-405d-838a-bb5852ed67a7)

### Assignment 7
#7.1
update game
set  location = (select ident from airport where name = "Nottingham Airport"), 
co2_consumed = co2_consumed+500
where screen_name = "Vesa";

select * from game;
![7 1](https://github.com/user-attachments/assets/83956073-2085-4680-abba-89b28f6ef434)

#7.2
![7 2](https://github.com/user-attachments/assets/67d5fb0a-40ce-4c09-8f34-7c117d8ff4b0)

#7.3
delete from goal_reached;
select * from goal_reached;

#7.4
delete from game;
select * from game;
![7 4](https://github.com/user-attachments/assets/d08d9dea-537d-4256-84a9-448703b8d3c1)




