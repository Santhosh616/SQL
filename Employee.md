````
-- create a db
 create database EmployeeDB;
 
 -- use that db
 use EmployeeDB;
 
 -- create table detail of an employee
 
 CREATE TABLE Details (
    Employee_Id VARCHAR(100),
    Employee_name VARCHAR(100),
    dateofBirth DATE,
    DateOfjoining DATE,
    Salary INT,
    Bonus INT,
    City VARCHAR(100),
    Address VARCHAR(100),
    Department VARCHAR(100),
    Employee_mail_id VARCHAR(100),
    Employee_status VARCHAR(100),
    Timestamp date default current_timestamp,
    Phone_number VARCHAR(10)
);

-- display the result
select * from details;

-- insert values to table
insert into Details (Employee_Id, Employee_name, dateofBirth, DateOfjoining, Salary, Bonus, City, Address, Department, Employee_mail_id, Employee_status, Phone_number)
values
('ds001', 'Sharanya', '1985-05-15', '2010-08-23', 70000, 5000, 'Delhi', '1234 Rajpath Rd', 'HR', 'sha2005ranya@gmail.com', 'Active', '9876543210'),
('ds002', 'Sree', '1990-03-12', '2015-07-30', 75000, 6000, 'Mumbai', '5678 Bandra East', 'Finance', 'sree12@gmail.com', 'Active', '9123456789'),
('ds003', 'Prabhu', '1982-11-22', '2008-05-10', 80000, 7000, 'Bangalore', '9101 MG Road', 'IT', 'prabhu@gmail.com', 'Inactive', '9345678901'),
('ds004', 'Madhan', '1995-02-05', '2018-01-25', 68000, 4000, 'Chennai', '1234 Anna Nagar', 'Marketing', 'madhan@23gmail.com', 'Active', '9786541230'),
('ds005', 'Kumaran', '1980-07-09', '2005-03-13', 95000, 8000, 'Hyderabad', '6789 Banjara Hills', 'Operations', 'kumaran@gmail.com', 'Active', '9345678123'),
('ds006', 'Nandha', '1993-10-16', '2017-11-05', 72000, 5500, 'Pune', '2345 Koregaon Park', 'Legal', 'Nandha12@gmail.com', 'Active', '9876123456'),
('ds007', 'Navanithi', '1988-04-23', '2014-02-11', 85000, 6500, 'Kolkata', '3456 Salt Lake City', 'Engineering', 'navanithi@gmail.com', 'Inactive', '9912345678'),
('ds008', 'Aashif Shadin', '1997-08-30', '2020-06-19', 60000, 3000, 'Jaipur', '4567 C-Scheme', 'Sales', 'aashi@gmail.com', 'Active', '9034567890'),
('ds009', 'Santhosh', '1984-01-10', '2009-09-07', 77000, 5200, 'Lucknow', '5678 Hazratganj', 'Support', 'sandy@gmail.com', 'Active', '9123987456'),
('ds010', 'Praveen', '1992-12-20', '2016-10-17', 73000, 4800, 'Ahmedabad', '6789 Navrangpura', 'Finance', 'bheem@gmail.com', 'Active', '9384765120');

-- change column name
 alter table Details
change column  Employee_name First_name varchar(20);

-- add column to existing table
alter table Details 
add column Age int ;

-- update details
update Details
set Age=19
where Employee_id='ds001';
update Details
set Age=20
where Employee_id='ds002';
update Details
set Age=19
where Employee_id='ds003';
update Details
set Age=20
where Employee_id='ds004';
update Details
set Age=20
where Employee_id='ds005';
update Details
set Age=20
where Employee_id='ds006';
update Details
set Age=20
where Employee_id='ds007';
update Details
set Age=20
where Employee_id='ds008';
update Details
set Age=19
where Employee_id='ds009';
update Details
set Age=19
where Employee_id='ds010';

-- drop column 
alter table Details
drop column Employee_status ;

-- delete  a record
delete from Details where Employee_id='ds006';

-- display name ends with a
select * from details where first_name like '%a';

-- salary more than 70000
select * from details
where salary>70000;

-- city chennai
select * from details
where city = "chennai";

-- age 19 and dep s finance
select * from details
where age= 19 and department ='Finance';

-- count of salary more than 90000
select count(*) from details
where  salary>90000;

-- average age in dept finance
select avg(age) from details
where department ='finance';

-- aggregate function
select max(salary) from details ;
select min(salary) from details;

-- name start with A
select * from details 
where  first_name like "A%";

-- name middle in A  and salary between 85000 and 90000
select *  from details 
where first_name like '%a%'
and salary between 85000 and 90000;

-- truncate table
truncate details;
````
