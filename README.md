# Spring CRUD with Vue.js

## Description

This is a simple Spring CRUD application, with vue.js for the view rendering. 
It can connect to a database and view,save,edit and delete Person and Supplier entities.

This project was created for training purposes.

## Requirements

- JDK 1.8 or above
- Maven 3.x
- Git 2.x
- MySQL5.x
- Node.js 6.x

## Installation

First, git clone the application in a local folder and then follow the instructions below.

### Server Application:
1. Create an empty database schema in your MySQL installation with the name: "springbootcrud".
2. Open the folder "springbootcrud" as a project on your preferred IDE.
3. Open the file: springbootcrud-webapp/src/main/resources/application.properties.
4. Modify the following properties, depending on your MySQL installation:
   - spring.datasource.username=root
   - spring.datasource.password=(your root user password)
5. Build the project in your IDE to download the necessary dependencies.
6. Run the Application.class file.

### Client Application:
1. Cd to the springbootcrud-client folder.
2. Execute the following command in the terminal:
    - command: npm install
3. When the installation will be finished you can run the Client with the following terminal command:
   - command: npm run dev
4. Then you can visit http://localhost:9000

## Usage 

1. On the left of the Dashboard stands the navigation menu where you can navigate between the Home Page and the Persons and Suppliers dashboard panels.
2. On the Home page, you can view the welcome message.
3. On the Person Management page, you can:
    - initiate a search on the existing Persons based on their name or email
    - create a new Person
    - edit an existing Person
    - delete a Person
4. On the Supplier Management page, you can:
    - initiate a search on the existing Suppliers based on their Company Name or VAT number
    - create a new Supplier
    - edit an existing Supplier
    - delete a Supplier