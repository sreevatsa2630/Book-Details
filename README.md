Spring Boot – CRUD Operations using MongoDB

CRUD stands for Create, Read/Retrieve, Update, and Delete and these are the four basic operations that we perform on persistence storage. CRUD is data-oriented and the standardized use of HTTP methods. HTTP has a few methods which work as CRUD operations and do note they are very vital from a developmental point perspective in programming that also does helps us relate better web development and also aids us while dealing with databases. 

So, standard CRUD Operations are as follows:

POST: Creates a new resource
GET: Reads/Retrieve a resource
PUT: Updates an existing resource
DELETE: Deletes a resource

Step 1: Refer to this article How to Create a Spring Boot Project with IntelliJ IDEA and create a Spring Boot project. 

Step 2: Add the following dependency

Spring Web
MongoDB
Lombok
DevTools

Below is the complete code for the pom.xml file. Please check if you have missed something.

<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.6.0</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.globallogic</groupId>
	<artifactId>spring-mongodb</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>spring-mongodb</name>
	<description>Demo project for Spring Boot</description>
	<properties>
		<java.version>11</java.version>
	</properties>
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-mongodb</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>
		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
			<optional>true</optional>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
				<configuration>
					<excludes>
						<exclude>
							<groupId>org.projectlombok</groupId>
							<artifactId>lombok</artifactId>
						</exclude>
					</excludes>
				</configuration>
			</plugin>
		</plugins>
	</build>

</project>

Step 3: Create 3 packages and create some classes and interfaces inside these packages as seen in the below image

model
repository
controller

step 4:Create the class in the package after that copy the code and it 

Step 5: Inside the MongoDB Compass

Go to your MongoDB Compass and create a Database named BookStore and inside the database create a collection named Book 

Now run your application and let’s test the endpoints in Postman and also refer to our MongoDB Compass.

Testing the Endpoint in Postman

Endpoint 1: POST – http://localhost:8989/addBook
Endpoint 2: GET – http://localhost:8989/findAllBooks
Endpoint 3: DELETE – http://localhost:8989/delete/1329

