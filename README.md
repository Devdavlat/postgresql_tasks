## Task 1
## Question
### Categories jadval barcha ustun ma’lumotlarini bilan qaytaring.
#### Query  
```
select * from categories;
```
## Result
![Screenshot from 2023-02-22 21-33-50](https://user-images.githubusercontent.com/109902921/220850788-dff7f47e-7a9e-44e5-9ba7-b6d8fa5bcc11.png)
## -------------------------------------------------------------

## Task 2
## Question
### 2. Categories jadval category_name va description ustun ma’lumotlarini qaytaring
#### Query
```
select category_name , description from categories;
```
## Result
![Screenshot from 2023-02-22 21-36-56](https://user-images.githubusercontent.com/109902921/220850791-96a643a0-cac2-43c0-917f-9909dee4257d.png)
## Task 3
## Question
### Categories jadval barcha ustun ma’lumotlari olishda ustun nomlarini o’zbekcha tarjimada
### qaytaring. M-n: category_name=Nomi
#### Query
```
select 
    category_name as nomi, 
    description as tavsifi,
    picture as rasm 
   
from categories;
```
## Result
![Screenshot from 2023-02-22 21-39-17](https://user-images.githubusercontent.com/109902921/220850793-0669447d-48ec-4200-9284-175c213348c6.png)
## Task 4
## Question
### Categories jadvaldan kategoriya nomi ’Confections’ ga teng bo’lgan ma’lumotlarni
qaytaring.
#### Query
```
select * from categories
where category_name = 'Confections';
```
## Result
![Screenshot from 2023-02-22 21-41-30](https://user-images.githubusercontent.com/109902921/220850798-499eb79d-6841-4473-8d43-4181b1d7027b.png)
## Task 5
## Question
### Categories jadvaldan kategoriya nomi ‘Produce’ yoki ‘Seafood’ bo’lgan ma’lumotlarni
### qaytaring.
#### Query
```
select * from categories
where category_name = 'Produce' or category_name = 'Seafood';
```
## Result
![Screenshot from 2023-02-22 21-46-11](https://user-images.githubusercontent.com/109902921/220850802-a7ab7977-0152-4235-a61d-ebff72483923.png)
## Task 6
## Question
### Categories jadvaldan quyida belgilangan ma’lumotlarni qaytaring.
![Screenshot from 2023-02-23 15-19-19.png](..%2F..%2FPictures%2FScreenshots%2FScreenshot%20from%202023-02-23%2015-19-19.png)
### Query
```
select * from categories
where category_id between 6 and 8;
```
## Result
![Screenshot from 2023-02-22 21-50-11](https://user-images.githubusercontent.com/109902921/220850805-35b192bc-e65a-49ee-9d4e-918b3c073587.png)
## Task 7
## Question
### Categories jadvaldan ma’lumotlarni description alifbo bo’yicha Z-A tartibida chiqaring..
#### Query
```
select * from categories
order by description desc;
```
## Result
![Screenshot from 2023-02-22 21-51-12](https://user-images.githubusercontent.com/109902921/220850809-9c85e9b3-2d57-45d7-b053-47147b9e4e2c.png)
## Task 8
## Question
### Customers jadvalidan barcha ma’lumotlarni oling..
#### Query
```
select * from customers;
```
## Result
![Screenshot from 2023-02-22 21-53-26](https://user-images.githubusercontent.com/109902921/220850810-b68bd587-a7e2-4b30-b0df-57fed2fda108.png)
## Task 9
## Question
### Customers jadvalida ustun nomlarini o’zbekcha holatda oling.
#### Query
```
select customer_id as id , company_name as "kompaniya nomi" ,
contact_name as "kontak nomi" , contact_title as "kontak sarlavhasi",
address as adres , city as shahar , region as hudud,postal_code as "pochta kodi",
country as shahar, phone as telefon , fax as fax from customers; 
```
## Result
![Screenshot from 2023-02-22 22-01-16](https://user-images.githubusercontent.com/109902921/220850825-6b03d264-a8d8-47e3-a3af-1db3a5a9ef3b.png)
## Task 10
## Question
### Customers jadvalidan contact_title ‘Owner’ bo’lgan ma’lumotlarni qaytaring.
#### Query
```
select * from customers
where contact_title = 'Owner';
```
## Result
![Screenshot from 2023-02-22 22-03-42](https://user-images.githubusercontent.com/109902921/220850829-27bb34bb-871c-4f12-9584-7cf982881be9.png)
## Task 11
## Question
### Customers jadvalidan city ‘London’ bo’lgan ma’lumotlarni qaytaring.
#### Query
```
select * from customers
where city = 'London'; 
```
## Result
![Screenshot from 2023-02-22 22-04-08](https://user-images.githubusercontent.com/109902921/220850833-cc19f522-478e-4118-b420-6c9631c758fc.png)
## Task 12
## Question
### Customers jadvalidan region ustun NULL bo’lgan ma’lumotlarni qaytaring.
#### Query
```
select * from customers
where region is null;
```
## Result
![Screenshot from 2023-02-22 22-05-50](https://user-images.githubusercontent.com/109902921/220850836-3f37bd42-e51b-4546-b9fe-d38cb3a2f913.png)

## Task 13
## Question
### Customers jadvalidan region ustun NULL bo’lmagan ma’lumotlarni qaytaring..
#### Query
```
select * from customers
where region is not null;
```
## Result
![Screenshot from 2023-02-22 22-06-10](https://user-images.githubusercontent.com/109902921/220850846-5c44e912-625e-46cc-9919-141af3961fc4.png)
## Task 14
## Question
### Customers jadvalidan country ustun Germany bo’lgan ma’lumotlarni qaytaring..
#### Query
```
select * from customers
where country = 'Germany';
```
## Result
![Screenshot from 2023-02-22 22-08-57](https://user-images.githubusercontent.com/109902921/220850851-ddc18153-3c96-48f2-bb27-688aedcdb749.png)
## Task 15
## Question 
### Categories jadval barcha ustun ma’lumotlarini bilan qaytaring.
#### Query
```
select count(*) from customers
where country = 'Germany';
```
## Result
![Screenshot from 2023-02-22 22-09-22](https://user-images.githubusercontent.com/109902921/220850856-e25a7d78-d394-4e60-8b1e-42b6eae5435f.png)
## Task 16
## Question
### Customers jadvalidan fax ustun NULL bo’lmalgan ma’lumotlarni contact_name ustun
### alifbo tartiba tartiblab qaytaring..
#### Query
```
select * from customers
where fax is not null 
order by contact_name;
```
## Result
![Screenshot from 2023-02-22 22-13-37](https://user-images.githubusercontent.com/109902921/220850858-8788a844-72c5-4a1b-b276-519bc1236986.png)
## Task 17
## Question
### Employees jadvaldan barcha ma’lumotlarni qaytaring.
#### Query
```
select * from employees;
```
## Result
![Screenshot from 2023-02-22 22-14-52](https://user-images.githubusercontent.com/109902921/220850864-fdbadd32-58a0-4d77-af30-c5f58dee24cb.png)
## Task 18
## Question
### Employees jadval ustun nomlarini o’zbekcha qaytaring.
#### Query
```
select 
employee_id as id , 
first_name as ismi ,
last_name as familiyasi ,
title as sarlavhasi,
address as adres ,
title_of_courtesy as "murojaat qilish odobi",
birth_date as "tug'ilgan sanasi",
hire_date as "ishga qabul qilingan sanasi",
address as adres,
city as shahar,
region as hudud,
postal_code as "pochta kodi",
country as viloyat,
home_phone as "uy telefon", 
extension as kengaytma,
photo as rasm,
photo_path as "rasm limki",
notes as elsatmalar
from employees;
```
## Result
![Screenshot from 2023-02-22 22-16-58](https://user-images.githubusercontent.com/109902921/220850869-fdab63bd-ef7d-44fd-a526-d86f0ab748af.png)
## Task 19
## Question
### Employess jadvaldan title_of_courtest ‘Mr’ bo’lgan xodimlarni firts_name alifbo tartibida
### qaytaring.
#### Query
```
select * from employees
where title_of_courtesy = 'Mr';
```
## Result
![Screenshot from 2023-02-22 22-25-28](https://user-images.githubusercontent.com/109902921/220850874-3353907b-03d9-4fd8-a139-59f56767c7f7.png)
## Task 20
## Question
### Employes jadvalda title ‘Sales Representative’ bo’lgan xodimlar sonini qaytaring.
#### Query
```
select * from employees
where title = 'Sales Representative';
```
## Result
![Screenshot from 2023-02-22 22-27-20](https://user-images.githubusercontent.com/109902921/220850879-3bd46da6-0d77-4260-87e1-dd1c8ea2850d.png)
## Task 21
## Question
### Employes jadvalda hire_date 1994-yilda bo’lgan ma’lumotlarni qaytaring..
#### Query
```
select * from employees
where hire_date between '1994-01-01' and '1994-12-31';
```
## Result
![Screenshot from 2023-02-22 22-31-13](https://user-images.githubusercontent.com/109902921/220850884-73c661a4-b11c-4c23-ae1b-51de468d7b33.png)
## Task 22
## Question
### Employes jadvaldan region NULL bo’lmagan xodimlarni first_name, last_name, title, city,
### home_phone ma’lumotlarini first_name Z-A alifbo tartibida qaytaring.
#### Query
```
select firts_name , last_name , title,city, home_phone from employees
order by first_name desc;
```
## Result
![Screenshot from 2023-02-22 22-35-29](https://user-images.githubusercontent.com/109902921/220850888-e96d2594-9105-4226-ad19-e853b7164322.png)
## Task 23
## Question
### Orders jadvaldan customer_id ‘VINET’ bo’lgan buyurtmalarni qaytaring.
#### Query
```
select * from orsers
where customer_id = 'VINET';
```
## Result
![Screenshot from 2023-02-22 22-48-18](https://user-images.githubusercontent.com/109902921/220850893-213a4010-1e86-41ea-b512-f6ce8b4d9155.png)
## Task 24
## Question
### Orders jadvaldan order_date ustuni orqali 1996-yildagi ma’lumotlarni qaytaring.
#### Query
```
select * from orders 
where order_date between '1996-01-01' and '1996-12-31';
```
## Result
![Screenshot from 2023-02-23 11-33-08](https://user-images.githubusercontent.com/109902921/220850898-75ffd3fc-37b5-4851-92f4-e8aa57d8efe6.png)
## Task 25
## Question
### Orders jadvaldan ship_region ustun NULL bo’lmagan ma’lumotlarni qaytaring.
#### Query
```
select * from orders
where ship_region is not null;
```
## Result
![Screenshot from 2023-02-23 11-34-49](https://user-images.githubusercontent.com/109902921/220850901-51cea7a3-3706-483f-8911-4110407ee477.png)
## Task 26
## Question
### Orders jadvaldan order_id 10300 va 10400 orasida bo’lgan ma’lumotlarni qaytaring..
#### Query
```
select * from orders 
where order_id between 10300 and 10400;
```
## Result!
![Screenshot from 2023-02-23 11-48-45.png](..%2F..%2FPictures%2FScreenshots%2FScreenshot%20from%202023-02-23%2011-48-45.png)
## Task 27
## Question
### Order Details jadvaldan unit_price ustun umumiy qiymatini qaytaring..
#### Query
```
select sum(unit_price) from order_detail
```
## Result
![Screenshot from 2023-02-23 11-50-17](https://user-images.githubusercontent.com/109902921/220850915-8a476159-3633-470c-8a4c-9e9d29ee253b.png)
