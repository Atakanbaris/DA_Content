## SQL TASK 12
## 1
SELECT COUNT(length) FROM film WHERE length>
(
SELECT AVG(length) FROM film
);
## 2
SELECT COUNT(rental_rate) FROM film WHERE rental_rate=(
SELECT MAX(rental_rate) from film);
## 3
SELECT title,rental_rate,replacement_cost FROM film 
WHERE rental_rate=(
SELECT MIN(rental_rate)FROM film)
AND replacement_cost=
(SELECT MIN(replacement_cost)FROM film);
## 4
SELECT customer_id, COUNT(*) FROM payment GROUP BY customer_id ORDER BY count DESC;