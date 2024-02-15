# задание 3
```sql
update products set price = price * 0.875
where products.category = 'clothing';
update products set price = price * 0.95
where products.category != 'clothing';
```

# задание 4
```sql
Самая низкая цена

select category, avg(price)
from products
group by category
order by avg 
limit 1

Самая высокая цена

select category, avg(price)
from products
group by category
order by avg desc
limit 1
```
# задание 5
```sql
select * from orders
delete from orders where quantity
< (select avg (quantity) from orders);
```
