## SQL TASK 8
## 1
CREATE TABLE employee (
      id INTEGER,
  	name VARCHAR(50),
  	birthday DATE,
  	email VARCHAR(100)
);
## 2
insert into employee (id, name, birthday, email) values (1, 'Xenia', '1997-03-04', 'xsanpher0@goodreads.com');
...
insert into employee (id, name, birthday, email) values (50, 'Cobby', '1951-06-24', 'cogus1d@umich.edu');
## 3
UPDATE employee
SET name='James'
WHERE name LIKE 'J%'
RETURNING *;
## 4
DELETE FROM employee
WHERE name='James'
RETURNING *;