# Sql-Practice---03

create database project
use project

create table emp(emp_ID int primary key identity,emp_Name varchar(20),
emp_salary money, emp_Dept varchar(20),emp_Gender varchar(20),dept_no int)



insert into emp values
('sohan',20000,'IT','Male',2),
('mohan',25000,'HR','Male',1),
('rohan',30000,'CS','Male',4),
('gita',35000,'TL','Female',3),
('sita',40000,'IT','Female',6),
('rita',45000,'HR','Female',5),
('raju bhai',50000,'IT','Male',7)


alter table emp add emp_Job varchar(20)
update emp set emp_Job='clerk' where emp_ID=2
update emp set emp_Job='salesman' where emp_ID=3
update emp set emp_Job='driver' where emp_ID=4
update emp set emp_Job='ca' where emp_ID=5
update emp set emp_Job='tl' where emp_ID=6
update emp set emp_Job='fm' where emp_ID=7


select emp_name ,emp_salary/12  Monthly_salary from emp

select * from emp where dept_no=4 or dept_no=7

select * from emp where dept_no=5 and emp_salary>40000

select * from emp where emp_Job not in ('salesman','clerk')

select * from emp where emp_Name in ('gita','sita','raju bhai','mohan')

select * from emp where emp_name like 'r%' and emp_name like '_________'

select * from emp where emp_Name like '%i' 

select count(emp_salary/12) monthly_salry,COUNT(emp_salary) 
annual_salary from emp

select emp_salary as total_salary from emp

select * from  emp where  emp_salary = any
(select emp_salary from emp where emp_salary<45000)

select emp_Name,emp_salary from emp where emp_salary<45000

select * from emp

