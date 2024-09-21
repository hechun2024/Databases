# Databases-He Chun
# Week [3]

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
select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "Iceland";
![3 3](https://github.com/user-attachments/assets/3de89ca7-83b6-42e2-91e6-8d68322f6a0a)

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



