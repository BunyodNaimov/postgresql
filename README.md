## 1. Categories jadval barcha ustun ma’lumotlarini bilan qaytaring.
```sql
SELECT * FROM categories 
```

![изображение](https://user-images.githubusercontent.com/122611882/221087577-14e1090a-526d-4c71-ab65-c6b104564f8d.png)

## 2. Categories jadval category_name va description ustun ma’lumotlarini qaytaring.
```sql 
select category_name, description from categories
```

![изображение](https://user-images.githubusercontent.com/122611882/221088067-fab4ddb7-d91a-4986-ba1f-79bbf42b3c78.png)

## 3. Categories jadval barcha ustun ma’lumotlari olishda ustun nomlarini o’zbekcha tarjimada qaytaring. M-n: category_name=Nomi
```sql
select
    category_id as id,
    category_name as nomi,
    description as tavsifi,
    picture as rasmi
from categories
```

![изображение](https://user-images.githubusercontent.com/122611882/221088831-ea9420ec-142b-40e3-8b31-9676a4624985.png)

## 4. Categories jadvaldan kategoriya nomi ’Confections’ ga teng bo’lgan ma’lumotlarni qaytaring.
```sql
select
*
from categories
where category_name='Confections'
```

![изображение](https://user-images.githubusercontent.com/122611882/221089299-ed58e3dd-55da-44de-8696-2a6d94b91eb8.png)

## 5. Categories jadvaldan kategoriya nomi ‘Produce’ yoki ‘Seafood’ bo’lgan ma’lumotlarni qaytaring.
```sql
select
*
from categories
where category_name='Produce'
```

![изображение](https://user-images.githubusercontent.com/122611882/221090732-4e02295b-93e7-4790-8cd1-570c7fa1aa08.png)

## 6 Categories jadvaldan quyida belgilangan ma’lumotlarni qaytaring.

```sql
select *
from categories
limit 3 offset 5
```


![изображение](https://user-images.githubusercontent.com/122611882/221090782-3cb55624-db55-4d18-a68e-25d7697f4f60.png)

## 7. Categories jadvaldan ma’lumotlarni description alifbo bo’yicha Z-A tartibida chiqaring.
```sql
select description
from categories
order by description desc
```

![изображение](https://user-images.githubusercontent.com/122611882/221091473-683b3426-c176-4a12-9c3b-a58a9d5a2f76.png)

## 8. Customers jadvalidan barcha ma’lumotlarni oling.
```sql
select *
from customers
```

![изображение](https://user-images.githubusercontent.com/122611882/221113201-291bf98d-2939-433e-a47c-72e6b3d6c7d1.png)

## 9. Customers jadvalida ustun nomlarini o’zbekcha holatda oling.
```sql
select customer_id   as mijoz_id_si,
       company_name  as kampaniya_nomi,
       contact_name  as kantakt_nomi,
       contact_title as kontakt_sarlavhasi,
       address       as manzil,
       city          as shahar,
       region        as mintaqa
from customers
```

![изображение](https://user-images.githubusercontent.com/122611882/221114401-fcdeacf2-c8fe-44f3-9b8b-bef6b0090c9f.png)

## 10. Customers jadvalidan contact_title ‘Owner’ bo’lgan ma’lumotlarni qaytaring
```sql
select *
from customers
where contact_title='Owner'
```

![изображение](https://user-images.githubusercontent.com/122611882/221116059-57fde6a2-f18b-4905-a858-9ac6325eb408.png)


## 11. Customers jadvalidan city ‘London’ bo’lgan ma’lumotlarni qaytaring.
```sql 
select *
from customers
where city='London'
```

![изображение](https://user-images.githubusercontent.com/122611882/221112694-b9854ed1-5a4a-45fc-b639-2edae498c1ec.png)

## 12. Customers jadvalidan region ustun NULL bo’lgan ma’lumotlarni qaytaring.
```sql
select *
from customers
where region is null
```

![изображение](https://user-images.githubusercontent.com/122611882/221117515-9f74a26b-e087-4e78-af4b-3213e1f719d6.png)

## 13. Customers jadvalidan region ustun NULL bo’lmagan ma’lumotlarni qaytaring.
```sql
select *
from customers
where region is not null
```

![изображение](https://user-images.githubusercontent.com/122611882/221118176-d26e8770-ec0d-4ce0-a321-aa088952eef3.png)

## 14. Customers jadvalidan country ustun Germany bo’lgan ma’lumotlarni qaytaring.
```sql
select customer_id,company_name,contact_name,region,country
from customers
where country='Germany'
```

![изображение](https://user-images.githubusercontent.com/122611882/221118526-e9b6e293-bc9c-437d-888d-2177ac285b8d.png)

## 15. Customers jadvalidan country ustun Germany bo’lgan qatorlar sonini qaytaring.
```sql
select count(*)
from customers
where country='Germany'
```

![изображение](https://user-images.githubusercontent.com/122611882/221118890-e6f1d3b0-072d-4c22-952c-45aa5b6cd286.png)

## 16. Customers jadvalidan fax ustun NULL bo’lmalgan ma’lumotlarni contact_name ustun alifbo tartiba tartiblab qaytaring.
```sql
select contact_name, fax
from customers
where fax is not null
order by contact_name asc
```

![изображение](https://user-images.githubusercontent.com/122611882/221119885-7e6e557b-2406-49b7-8598-418128b60a02.png)

## 17. Employees jadvaldan barcha ma’lumotlarni qaytaring.
```sql
select *
from employees
```

![изображение](https://user-images.githubusercontent.com/122611882/221120429-280885d2-ac0b-4360-bca7-3544c595e9ca.png)

## 18. Employees jadval ustun nomlarini o’zbekcha qaytaring.
```sql
select
    employee_id as ishchi_id_si,
    last_name as familia,
    first_name as ism,
    title as lavozim,
    title_of_courtesy as xushmuomalalik_unvoni,
    birth_date as tugilgan_sana,
    hire_date as ishga_qabul_qilingan_date,
    address as manzil,
    city as shahar,
    region as mintaqa
from employees
```

![изображение](https://user-images.githubusercontent.com/122611882/221130892-73ba4700-9017-430a-a41f-a1d9c166748f.png)

## 19. Employess jadvaldan title_of_courtest ‘Mr’ bo’lgan xodimlarni firts_name alifbo tartibida qaytaring.
```sql
select first_name, title_of_courtesy
from employees
where title_of_courtesy='Mr.'
order by first_name asc
```

![изображение](https://user-images.githubusercontent.com/122611882/221132285-a7be5094-69e9-45ce-9a27-e20b9387262a.png)

## 20. Employes jadvalda title ‘Sales Representative’ bo’lgan xodimlar sonini qaytaring.

```sql
select count(*)
from employees
where title='Sales Representative'
```

![изображение](https://user-images.githubusercontent.com/122611882/221132763-9eeb79fe-f47b-4e38-be0f-3d1219ac7e6e.png)

## 21. Employes jadvalda hire_date 1994-yilda bo’lgan ma’lumotlarni qaytaring.
```sql
select *
from employees
where hire_date between '1994-01-01' and '1994-12-31'
```

![изображение](https://user-images.githubusercontent.com/122611882/221133660-fd2eae0f-cd7e-4d00-8f8c-9d5da4e25605.png)

## 22. Employes jadvaldan region NULL bo’lmagan xodimlarni first_name, last_name, title, city,
## home_phone ma’lumotlarini first_name Z-A alifbo tartibida qaytaring.
```sql
select  region,first_name, last_name, title, city,home_phone
from employees
where region is not null
order by first_name asc 
```

![изображение](https://user-images.githubusercontent.com/122611882/221135279-f2f309d1-c822-41a4-ad51-1a908da91bb7.png)

## 23. Orders jadvaldan customer_id ‘VINET’ bo’lgan buyurtmalarni qaytaring.

```sql
select  *
from orders
where customer_id='VINET'
```
![изображение](https://user-images.githubusercontent.com/122611882/221136060-2bbb6420-bd29-42dd-a72a-9c5ea98c5354.png)

##  24. Orders jadvaldan order_date ustuni orqali 1996-yildagi ma’lumotlarni qaytaring.
```sql
select  *
from orders
where order_date between '1996-01-01' and '1996-12-31'
```

![изображение](https://user-images.githubusercontent.com/122611882/221137373-ffda2c62-6ca9-4d01-b566-56c968187e3e.png)

## 25. Orders jadvaldan ship_region ustun NULL bo’lmagan ma’lumotlarni qaytaring.
```sql
select  *
from orders
where ship_region is not null
```

![изображение](https://user-images.githubusercontent.com/122611882/221137759-f2c53189-1600-435c-aac7-02d46f906cef.png)

## 26. Orders jadvaldan order_id 10300 va 10400 orasida bo’lgan ma’lumotlarni qaytaring.
```sql
select  *
from orders
where order_id between 10300 and 10400
```

![изображение](https://user-images.githubusercontent.com/122611882/221138120-a5e501ce-a2a4-4512-ada2-cc0614878276.png)

## 27. Order Details jadvaldan unit_price ustun umumiy qiymatini qaytaring
```sql
select  sum(unit_price)
from order_details
```

![изображение](https://user-images.githubusercontent.com/122611882/221138791-228c6c9c-85f4-4eda-ba8a-3f015dca61a2.png)

