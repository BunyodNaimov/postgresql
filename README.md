```sql
SELECT * FROM categories 
```

![изображение](https://user-images.githubusercontent.com/122611882/221087577-14e1090a-526d-4c71-ab65-c6b104564f8d.png)


```sql 
select category_name, description from categories
```

![изображение](https://user-images.githubusercontent.com/122611882/221088067-fab4ddb7-d91a-4986-ba1f-79bbf42b3c78.png)


```sql
select
    category_id as id,
    category_name as nomi,
    description as tavsifi,
    picture as rasmi
from categories
```

![изображение](https://user-images.githubusercontent.com/122611882/221088831-ea9420ec-142b-40e3-8b31-9676a4624985.png)


```sql
select
*
from categories
where category_name='Confections'
```

![изображение](https://user-images.githubusercontent.com/122611882/221089299-ed58e3dd-55da-44de-8696-2a6d94b91eb8.png)


```sql
select
*
from categories
where category_name='Produce'
```

![изображение](https://user-images.githubusercontent.com/122611882/221090732-4e02295b-93e7-4790-8cd1-570c7fa1aa08.png)

```sql
select *
from categories
limit 3 offset 5
```


![изображение](https://user-images.githubusercontent.com/122611882/221090782-3cb55624-db55-4d18-a68e-25d7697f4f60.png)


```sql
select description
from categories
order by description desc
```

![изображение](https://user-images.githubusercontent.com/122611882/221091473-683b3426-c176-4a12-9c3b-a58a9d5a2f76.png)


```sql
select *
from customers
```

![изображение](https://user-images.githubusercontent.com/122611882/221113201-291bf98d-2939-433e-a47c-72e6b3d6c7d1.png)


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

```sql
select *
from customers
where contact_title='Owner'
```

![изображение](https://user-images.githubusercontent.com/122611882/221116059-57fde6a2-f18b-4905-a858-9ac6325eb408.png)



```sql 
select *
from customers
where city='London'
```

![изображение](https://user-images.githubusercontent.com/122611882/221112694-b9854ed1-5a4a-45fc-b639-2edae498c1ec.png)


```sql
select *
from customers
where region is null
```

![изображение](https://user-images.githubusercontent.com/122611882/221117515-9f74a26b-e087-4e78-af4b-3213e1f719d6.png)


```sql
select *
from customers
where region is not null
```

![изображение](https://user-images.githubusercontent.com/122611882/221118176-d26e8770-ec0d-4ce0-a321-aa088952eef3.png)


```sql
select customer_id,company_name,contact_name,region,country
from customers
where country='Germany'
```

![изображение](https://user-images.githubusercontent.com/122611882/221118526-e9b6e293-bc9c-437d-888d-2177ac285b8d.png)


```sql
select count(*)
from customers
where country='Germany'
```

![изображение](https://user-images.githubusercontent.com/122611882/221118890-e6f1d3b0-072d-4c22-952c-45aa5b6cd286.png)


```sql
select contact_name, fax
from customers
where fax is not null
order by contact_name asc
```

![изображение](https://user-images.githubusercontent.com/122611882/221119885-7e6e557b-2406-49b7-8598-418128b60a02.png)


```sql
select *
from employees
```

![изображение](https://user-images.githubusercontent.com/122611882/221120429-280885d2-ac0b-4360-bca7-3544c595e9ca.png)


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


```sql
select first_name, title_of_courtesy
from employees
where title_of_courtesy='Mr.'
order by first_name asc
```

![изображение](https://user-images.githubusercontent.com/122611882/221132285-a7be5094-69e9-45ce-9a27-e20b9387262a.png)

```sql
select count(*)
from employees
where title='Sales Representative'
```

![изображение](https://user-images.githubusercontent.com/122611882/221132763-9eeb79fe-f47b-4e38-be0f-3d1219ac7e6e.png)


```sql
select *
from employees
where hire_date between '1994-01-01' and '1994-12-31'
```

![изображение](https://user-images.githubusercontent.com/122611882/221133660-fd2eae0f-cd7e-4d00-8f8c-9d5da4e25605.png)


```sql
select  region,first_name, last_name, title, city,home_phone
from employees
where region is not null
order by first_name asc 
```

![изображение](https://user-images.githubusercontent.com/122611882/221135279-f2f309d1-c822-41a4-ad51-1a908da91bb7.png)


```sql
select  *
from orders
where customer_id='VINET'
```
![изображение](https://user-images.githubusercontent.com/122611882/221136060-2bbb6420-bd29-42dd-a72a-9c5ea98c5354.png)

```sql
select  *
from orders
where order_date between '1996-01-01' and '1996-12-31'
```

![изображение](https://user-images.githubusercontent.com/122611882/221137373-ffda2c62-6ca9-4d01-b566-56c968187e3e.png)


```sql
select  *
from orders
where ship_region is not null
```

![изображение](https://user-images.githubusercontent.com/122611882/221137759-f2c53189-1600-435c-aac7-02d46f906cef.png)


```sql
select  *
from orders
where order_id between 10300 and 10400
```

![изображение](https://user-images.githubusercontent.com/122611882/221138120-a5e501ce-a2a4-4512-ada2-cc0614878276.png)


```sql
select  sum(unit_price)
from order_details
```

![изображение](https://user-images.githubusercontent.com/122611882/221138791-228c6c9c-85f4-4eda-ba8a-3f015dca61a2.png)

