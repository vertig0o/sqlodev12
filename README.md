# sqlodev12

1. Select count(*) from film 
where length>any 
(Select avg(length) from film);
2. Select count(*) from film
where rental_rate=
(Select max(rental_rate) from film);
3. Select * from film
where rental_rate=(Select min(rental_rate) from film) and 
replacement_cost=(Select min(replacement_cost) from film);
4. Select c.customer_id, c.first_name, COUNT(*) from payment p
Inner Join customer c ON p.customer_id = c.customer_id
Group By c.customer_id
Order By COUNT(*) DESC;
