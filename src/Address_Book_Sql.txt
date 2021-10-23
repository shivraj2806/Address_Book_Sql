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

# "UC4 - EDIT EXISTING CONTACT PERSON USING NAME"
update addressbook set ZIP_CODE = 422102 where FIRST_NAME = 'KALPESH';
select * from addressbook;

# "UC5 - DELETE PERSON USING PERSON NAME"
delete from addressbook where FIRST_NAME = 'KALPESH';
select * from addressbook;

# "UC6 - RETRIEVE PERSON BELONGING TO CITY OR STATE"
insert into addressbook(FIRST_NAME,LAST_NAME,ADDRESS,CITY,STATE,ZIP_CODE,PHONE_NUMBER,EMAIL)values('KALPESH','PATIL','MUMBAI','MUMBAI','MAHARASHTRA',422105,8208087289,'kalpesh@gmail.com');
select * from addressbook;
select FIRST_NAME from addressbook where CITY = 'MUMBAI';
select FIRST_NAME from addressbook where CITY = 'NASHIK';
select FIRST_NAME from addressbook where STATE = 'MAHARASHTRA';

# "UC7 - UNDERSTAND THE SIZE OF ADDRESSBOOK BY CITY OR STATE"
select count(FIRST_NAME) from addressbook where CITY = 'NASHIK';
select count(FIRST_NAME) from addressbook where CITY = 'MUMBAI';
select count(FIRST_NAME) from addressbook where STATE = 'MAHARASHTRA';

# "UC8 - SORT ENTRIES ALPHABETICALLY USING PERSON NAME FOR GIVEN CITY"
select FIRST_NAME from addressbook order by CITY ;