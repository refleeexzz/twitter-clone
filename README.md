twitter-clone
=======================
A simple twitter clone using PHP and a MySQL database.


Setup 
-----------
1) Start MySQL and apache in XAMPP. <br>

2) Create a new database MySQL in using XAMPP(write in browser http://localhost/phpmyadmin/).
<img src="https://i.imgur.com/oSnIH5Z.png"/>
<img src="https://i.imgur.com/4iW0kA5.png"/>
execute here <img src="https://i.imgur.com/nq1Fcwj.png"/>

```
create database twitter-clone;

use twitter-clone;

create table usuarios(
	id int not null primary key AUTO_INCREMENT,
	nome varchar(100) not null,
	email varchar(150) not null,
	senha varchar(32) not null
);

create table tweets(
	id int not null PRIMARY KEY AUTO_INCREMENT,
	id_usuario int not null,
	tweet varchar(140) not null,
	data datetime default current_timestamp
);

create table usuarios_seguidores(
	id int not null primary key auto_increment,
	id_usuario int not null,
	id_usuario_seguindo int not null
);
```

3) Make a backup of your original XAMPP htdocs.
<img src="https://i.imgur.com/MNMoGIy.png"/>
<img src="https://i.imgur.com/o1bYfEI.png"/> <br>
4) Cut the files from the public folder you downloaded into the htdocs folder inside the XAMPP directory:
<img src="https://i.imgur.com/0Aj19LB.png"/> <br>
5) Create a folder inside the XAMPP directory with the name "twitter-clone" and cut the remains of the files you downloaded inside it.
<img src="https://i.imgur.com/QhO7x8w.png"/>


