What we want to build

Client --> API Layer (GET | POST | PUT | DELETE) --> Service Layer --> Data Access Layer --> Database
																									|
																									|
Client <-- API Layer (GET | POST | PUT | DELETE) <-- Service Layer <-- Data Acess Layer <-- Database

So you hava a client @Frontend
Client calls APIs where the API will receive GET, POST, PUT, DELETE requests
We will have a Service Layer which is meant for business logic
We will have a data access layer which is responsable for connecting to a database
The API-Layer should talk to the Service-Layer to get some data; the Service-Layer should talk to the Data Access Layer to get a data so that it does a round trip (from client and all the way back)


Getting started
Goto Spring initializr
There you can boot strap any spring boot application
- pick your project type (maven / gradle)
- pick your language (java / kotlin / groovy)
- meta_group (youtube) | meta_artifact (yt_springboot | meta_name (ApiServiceData)
- Pick JAR for packaging (most common type for packaging type for java application)
- Dependencies (things our project needs): 
	Spring Web (for building web including RESTful, applications, Spring MVC, Tomcat as a container)
	Spring Data JPA (Persist data in SQL stores by using JDA and Hibernate)
	PostgreSQL Driver (connect to a postgreS database
- Download your project to your local folder
- open project with your favorite IDE: Intellij 
- Intellij
	Ultimate Edition has a lot of feautures when working with frameworks such as spring boot or working with databases
	Community Edition - you should also be fine with that
- Try "getbrains toolbox": lets you download and manage all your IDEs
- Take a look at the POM (Check your meta data, check your dependencies - you should see one default for testing and also a <parent> </parant>)

You have now successfuly created an empty spring boot application.

Start and run application testing
/src/test/java/com.meta_group.meta_artifact/meta_name
This is were all testing data is stored (learn more about testing uni testing / integration testing / mocking / TDD)
Here you have on empty test application.

Check project structure
/src/main/java/com.meta_group.meta_artifact/meta_name
Here you have a bere mode sperly application from scratch
You can see the anotation: @SpringBootApplication

/src/resources/ holdes:
- static (when doing web development such as html css javascript)
- template (when doing web development such as html css javascript)
- application.properties (Where we configure all properties for our application as well as environment specific properties, like when connecting to a database)


Start application
First, comment the dependency "data jpa" else the application will want to connect to a database
Run
Apache Tomcat will start as a web server on port 8080 
Browse to localhost:8080
For now will get nothing as we have not implemented any endpoints yet
404 means not found


Implement a simple RESTful ApiServiceData
Write code to your application class
Check comments there
So what we have done: created method returning jason array: ["Hello","World"]
That would be just the api layer


We want more :)
Create a class
Module it as a studet
Give it some attributes and behaviour
Students will endup in a database


Create a package to com.meta_group.meta_artifact
right click / new package / call it student
inside of student package, we will put every code that is student related
Write a Class Student (which will be our module)
Declare variables (id, name, email, dob-dateofbirth, age)
Write getters and setters and contructors 
Check code comments
Run
We are now done with a class that exposes an array of students


Now structure application into n-tier architecture with api-layer, service-layer, data access layer and DB

API-Layer
We already have class student
Now create class that will serve as the api layer
Create class in Student package called StudentController
Class StudentController will have all of the resources for our api

Service-Layer / Business layer
Now go ahead and create a class that would serve as the business logic for managing Student





