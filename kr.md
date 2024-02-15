# 3
```sql
update products set price = price * 0.875
where products.category = 'clothing';
update products set price = price * 0.95
where products.category != 'clothing';
```

# 4
## Самая низкая цена
```sql
select category, avg(price)
from products
group by category
order by avg 
limit 1
```
## Самая высокая цена
```sql
select category, avg(price)
from products
group by category
order by avg desc
limit 1
```
# 5
```sql
select * from orders
delete from orders where quantity
< (select avg (quantity) from orders);
```
