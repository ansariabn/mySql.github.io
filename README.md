# MySQL Project

## Project Question-1
![Question of Project](https://github.com/ansariabn/mySql.github.io/assets/110123115/6cd04bd0-73e3-44c5-923b-db5d492b6271)

## Project Question-2
![Project-2](https://github.com/ansariabn/mySql.github.io/assets/110123115/e3441125-7dfe-4577-9660-223456450c4e)

# Project Question-3
![proj-3-Q](https://github.com/ansariabn/mySql.github.io/assets/110123115/e30ecdb3-ef47-4943-8e5c-e7c36d6a038d)

## Project Answer-1
![Pr-ans](https://github.com/ansariabn/mySql.github.io/assets/110123115/b9951848-5c9f-47f8-85c7-c835ad292c77)


## Project Answer-2
![Project-2](https://github.com/ansariabn/mySql.github.io/assets/110123115/13a9afe1-b05b-45e4-9cec-bedfa1700963)


## Project Answer-3
create table Seller (
seller_id varchar (10) not null,
s_pass varchar (10),
Name varchar (20),
address varchar (20),
primary key (seller_id)
);

create table seller_phone_num(
phone_no int not null,
seller_id varchar (10) not null,
foreign key (seller_id) references Seller (seller_id)
);


create table Cart (
cart_id varchar (10) not null,
primary key (cart_id)
);

create table Customer (
customer_id varchar (10) not null,
c_pass varchar (20) not null,
Name Varchar (20) not null,
Address varchar (30) not null,
Phone_no Int not null,
Pincode int not null,
cart_id varchar (10) not null,
primary key (customer_id),
foreign key (cart_id) references Cart (cart_id)
);

create table payment (
payment_id varchar (10) not null,
payment_date date,
Total_amount int not null,
customer_id varchar (10) not null,
cart_id varchar (10) not null,
primary key (payment_id),
foreign key (customer_id) references Customer (customer_id),
foreign key (cart_id) references Cart (cart_id)
);



create table product(
product_id varchar (10)not null,
Type int not null,
color varchar (20),
age_group int not null,
size varchar (5),
gender varchar (1),
commission int not null,
cost int not null,
quantity int not null,
seller_id varchar (10) not null,
primary key (product_id),
foreign key (seller_id) references Seller (seller_id)
);


create table cart_item (
cart_id varchar (10) not null,
product_id varchar (10) not null,
quantity_wished int not null,
Date_added date,
purchased varchar (20),
foreign key (cart_id) references Cart (cart_id),
foreign key (product_id) references product (product_id),
primary key (cart_id, product_id)

);
3. 1 select city from customer 

order by Asc;

3.2 alter table Product
change Product_id pro_id varchar(10);

 

3.3 select * from customer 

 where product > 1

 

3.4 select * from customer 

where Name like 'a%a';

 

3.5 select * from order 

where cost > 10000

 

3.6 select * from Payment

insert into payment ()

values ()

ALTER TABLE customer
change Paymentr_id newPaymentr_id varchar(20);

select * from seller

insert into seller (column name)

values (colume value)

ALTER TABLE seller
change seller_id newseller_id varchar(20);

 

select * from cart

insert into cart ()

values ()

ALTER TABLE cart
change cart_id newcart_id varchar(20);
