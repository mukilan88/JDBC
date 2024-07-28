
# JDBC

A simple project for a java program to store data to database using JDBC

## Creating DB and Table in mysql
Step 1:

    create database jdbcdemo;

Step 2:

    use jdbcdemo;

Step 3:

    create table employee(

    emp_id  int PRIMARY KEY,

    ename varchar(30),

    salary int

    );

Step 4:

    insert into employee values(1,”Mukilan”,1000000);

Step 5:

    select * from employee;

Step 6: → call stored procedure

    delimiter $$

    create procedure GetEmp()

    begin

	    select  * from employee;

    end$$

    delimiter ;

Step 7: → stored procedure with input parameter

    delimiter $$

    create procedure GetEmpById(In id int)

    begin

	    select  * from employee where emp_id=id;

    end$$

    delimiter ;

Step 8: → stored procedure with input/output parameter

    delimiter $$

    create procedure GetNameById(In id int,out empname varchar(40))

    begin

	    select  ename from employee where emp_id=id into empname;

    end$$

    delimiter ;

## Creating project in eclipse

Step 1:

File Menu select → new → click java project → give the project name and click finish

Step 2:

In the project folder go to src and right click src → from new select class → create the main class file.

## Insert JAR

Download the jar file as platform independent as zip file and extract the file and insert the file to the project 

Right click the src → go to build path → click Configure Build Path → in that pop box select the libraries → click the classpath → left side select the add external JARs → add the extracted JAR file to the project


