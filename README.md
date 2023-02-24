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


