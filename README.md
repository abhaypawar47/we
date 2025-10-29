cmd -----------------------------------
	pwd = current dir
	ls = list file
	cd = change dir	
	mkdir = make new dir
	rmdir = remove directory
	touch = create new empty file
	cp = copy
	mv = move
	chmod = change file permisssion
	ping = check network
---------------------------------------------------------------------------------------------------
sql------------------------------------
	sql = used for store manage & retrive data from rdbms
	db->tables->rows & colums
	-
	ddl = create / alter / drop
	dml = select /insert / update /delete
	dcl = grant / revoke
	tcl =commit / rollback 
-DDL-------------------------
	create db = create database company
	use database = use company
	create table = create table emp ( emp_id primary key,name varchar,salary decimal);
	alter table = alter table emp add email varchar;
		      alter table emp modify salary float;
		      alter table emp drop column age;
	drop table = drop table emp;
	truncate table = truncate table emp;
-DML-------------------------
	insert data = insert into emp (emp_id,name,salary) values (1,"abhay",25000);
	select data = select * from emp;
		      select name,salary from emp where name = "abhay";
	update data = update emp set salary = 60000 where name ="abhay";
	delete data = delete from emp where name = "abhay";
-FILTER----------------------
	select * from emp where salary > 50000;
	select * from emp where department in ("it", "hr");
	select * from emp where name like "a%";
	select * from emp where salary between 40000 and 80000;	
-AGGR------------------------
	SELECT COUNT(*) FROM employees;
	SELECT AVG(salary) FROM employees;
	SELECT department, SUM(salary) FROM employees GROUP BY department;
---------------------------------------------------------------------------------------------------------------
MONGODB-----------------------------------------------------------------------------------------------------------------------
	show db = show dbs
	create/use db = use company
	create collection = db.createCollection("emp")
	insert document = db.emp.insertOne(name:"abhay",age:22,salary:23000 )
			  db.emp.insertMany([{name:"prit",age:25,salary:25000},{a re}]);
	read document = db.emp.find()
			db.employees.find({ department: "IT" })
			db.employees.find({ salary: { $gt: 50000 } })
-update and delete ------------------------------
	db.employees.updateOne({ name: "Abhay" }, { $set: { salary: 60000 } })
	db.employees.updateMany({}, { $inc: { age: 1 } })
	db.employees.deleteOne({ name: "John" })
	db.employees.deleteMany({ department: "HR" })

	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
