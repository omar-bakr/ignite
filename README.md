# DataBase session task

## Query for the second user with highest total purchases
```
SELECT user_id,COUNT(product_id),SUM(product.price)
FROM cart
INNER JOIN product
WHERE product.id=product_id
GROUP BY user_id  
```
### Query result

| user_id | COUNT(product_id)| SUM(product.price)
| --- | ----------- |--------
| 1 | 2 |25000
| 2 | 1 |15000

<br>

-------------------------------------- 


## Query for the best selling product
```
SELECT product.name,COUNT(product_id)
FROM order_prodcut
INNER JOIN product
WHERE product.id=product_id
GROUP BY product_id;

```
### Query result

| name | COUNT(product_id)
| --- | ----------- 
| iphone 12 | 2 
| samsun | 1 

<br>

-------------------------------------- 

## Query for the best selling category
```
SELECT categories.name,COUNT(category_id)
FROM product_category
INNER JOIN categories
WHERE categories.id=category_id
GROUP BY category_id;


```
### Query result

| name | COUNT(category_id)
| --- | ----------- 
| electronics | 2 

**Note:I have attached the ERD design alongside with some screenshots.**