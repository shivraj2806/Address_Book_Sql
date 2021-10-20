# " WELCOME TO ADDRESSBOOK SYSTEM MYSQL"

# "UC1 - CREATE ADDRESSBOOK SERVICE DATABASE"
create database addressbook_service;
show databases;

# "UC2 - CREATE ADDRESSBOOK TABLE"
use addressbook_service;
create table addressbook(FIRST_NAME varchar(50) NOT NULL,LAST_NAME varchar(50) NOT NULL,ADDRESS varchar(150) NOT NULL,CITY varchar(50) NOT NULL,STATE varchar(50) NOT NULL,ZIP_CODE int NOT NULL,PHONE_NUMBER bigint(20) NOT NULL,EMAIL varchar(30) NOT NULL);
describe addressbook;

# "UC3 - INSERT NEW CONTACTS TO ADDRESSBOOK"
insert into addressbook(FIRST_NAME,LAST_NAME,ADDRESS,CITY,STATE,ZIP_CODE,PHONE_NUMBER,EMAIL)values('PREM','PATIL','NASHIK','NASHIK','MAHARASHTRA',422101,7387557696,'prem@gmail.com'),('KALPESH','PATIL','MUMBAI','MUMBAI','MAHARASHTRA',422105,8208087289,'kalpesh@gmail.com');
select * from addressbook;