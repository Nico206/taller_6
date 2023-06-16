# Taller_6

Dependencias maven requeridas 

![image](https://github.com/NicoYwY/taller_6/assets/125584676/b26c7e95-1a04-4673-a1d3-dc1a0cae80a2)


Estructura de codigo MVC


![image](https://github.com/NicoYwY/taller_6/assets/125584676/66bce1a1-938b-43fd-aaad-be1c5c89d5f5)

ConnectionPool Funcional


![image](https://github.com/NicoYwY/taller_6/assets/125584676/e277598a-cd6f-4834-abf9-844f36087316)

Interfaz Repository java

![image](https://github.com/NicoYwY/taller_6/assets/125584676/9f3e9266-a5be-4b5b-b3c1-ae106b47a7c0)

Clase que implementa la interfaz Repository

![image](https://github.com/NicoYwY/taller_6/assets/125584676/5aecd244-fd82-4916-a6e8-33dab781abeb)

Script de creacion de base de datos

create database myapp;

use myapp;

create table users_tbl(
user_id int primary key auto_increment,
user_firstname varchar(40) not null,
user_lastname varchar (40) not null,
user_email varchar (60) not null,
user_password varbinary(256)
);

insert into myapp.users_tbl(user_firstname,user_lastname,user_email,user_password) values (upper('Nicolas'),upper('Zuñiga Rodriguez'),lower ('nicolas.music@gmail.com'), aes_encrypt('2N0I0C6OOO', '$2a$12$h3uBgKE.9Clbvn.Y1qU4ket8.rI5lkMctyyeXvVfYiwNsncfbdJcG'));

select*,
cast(aes_decrypt(user_password,'$2a$12$h3uBgKE.9Clbvn.Y1qU4ket8.rI5lkMctyyeXvVfYiwNsncfbdJcG') as char(50)) end_data from users_tbl where user_id=1;



