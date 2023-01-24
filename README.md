# deepracer2023

Database: deepracer
table : teams

create table teams (
prefix varchar(5)  default 'T',
teamid int primary key auto_increment,
team_name varchar(50)  not null,
password varchar(50)  not null,
category varchar(50) not null,
captain_name varchar(50) unique not null,
captain_mailid varchar(100) unique not null,
cmbno bigint(10) unique not null,
org_name varchar(50) not null,
no_of_members int,
unique team_name,
unique captain_name,
unique captain_mailid,
unique cmbno,
unique (prefix,teamid));

