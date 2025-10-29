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
-------------------------------------------------------------------------------------------
postman--------------------------------
	Postman is an API development and testing tool that allows you to:
		· Send requests (GET, POST, PUT, DELETE, etc.)
		· Test APIs manually or with scripts
		· Automate API testing with collections
		· View responses (JSON, XML, HTML)
		· Manage environments, tokens, and variables
-METHODS
	get = retrive data = get all users
	post = create new data = add user
	put = update full record = update user info
	patch = update partial record = change email only 
	delete = remove record = delete a user

-COMMON STATUS CODE 
	200 = SUCCESS
	400 = BAD REQUEST 
	404 = NOT FOUND
	500 = SERVER ERROR
-----------------------------------------------------------------------------------------
browser dev tool
	set of tool help inspect/debug/analyze/optimize web pages
	
	element panel=Inspect and edit the HTML and CSS of a webpage in real-time.
	Console Panel= used to log message test js code and view error / warning
	source panel = used for debug js code
	network panel = track all https req/res inc api-calls/css/scripts
	application panel =View and manage client-side data stored in the browser.
	Performance Panel=Analyze page load time, rendering performance, and FPS.
	Memory Panel=Used to detect memory leaks and manage performance.
	Device Toolbar=Simulate websites on different devices and screen sizes.
	
---------------------------------------------------------------------------------------------------
json
	data format used for storing and exchanging data between a server and a client.
	
	Text-based
	Language-independent
	Easy to read and write
	Structured like JavaScript objects
---------------------------------------------------------------------------------------------------
stlc
	sequence of specific activities conducted during the testing process to
	ensure software quality and that it meets the business requirements.
	
	1. Requirement Analysis
	2. Test Planning
	3. Test Case Design / Development
	4. Test Environment Setup
	5. Test Execution
	6. Test Closure

--Key Testing Types Used During STLC
	Unit Testing – Developer tests individual units.
	Integration Testing – Modules are combined and tested.
	System Testing – End-to-end system validation.
	Acceptance Testing – User/client validation.
	Regression Testing – Rechecking after bug fixes.
	Performance Testing – Checks system speed, scalability.
	Security Testing – Identifies vulnerabilities.
	
---------------------------------------------------------------------------------------------------
testing type
	ways or methods used to test a software application
	to ensure that:
			It works as expected,
			It meets user and business requirements,
			It’s reliable, secure, and performs well under various conditions.

	1.Functional Testing :ensure the software’s features and behaviors work correctly.
		Unit Testing:Test individual units or components of code.
		Integration Testing:Test interactions between integrated modules.
		System Testing:Validate the entire system as a whole.
		Sanity Testing:Quick check after small code changes or bug fixes to 	
			       confirm functionality is working fine
		Smoke Testing:Initial check before detailed testing
		Regression Testing:ensure new changes haven’t broken existing flty
	2.Non-Functional Testing :These ensure quality attributes like performance, 
				  reliability, and scalability.
		Performance Testing
		Load Testing
		Stress Testing	
	 	Scalability Testing
	 	
testing documentation
	Testing documentation is the proof and guide of all testing activities — before, 
	during, and after testing.
	
-----------------------------------------------------------------------------------------
BUG LIFECYCLE

	The Bug Life Cycle / Defect Life Cycle is the journey of a bug from the moment 
	it is identified until it is closed or deferred.
	
	stages:
		1. New / Opened
		2. Assigned
		3. Open
		4. Fixed / Resolved
		5. Retest
		6. Verified
		7. Closed
		8. Reopened (Optional)
		9. Rejected / Not a Bug / Deferred /
	
	Important Bug Attributes
		Bug ID
		Title / Summary
		Description
		Steps to Reproduce
		Expected Result
		Actual Result
		Severity
		Priority
		Status
		Assigned To
		Reported By
		Environment
		
-BUGZILLA
	open-source bug/defect tracking tool

-AUTOMATION TESTING
	process of using software tools to automatically execute pare actual
	results with expected results, and generate reports without human intervention.
	
-Selenium
	open-source automation tool
	Selenium cannot test desktop apps or mobile apps — only web-based applications
	
---------------------------------------------------------------------------------------------------------------------------------------------------------------
	
	

	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
