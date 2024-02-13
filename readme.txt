A project to perform crud operations on spring data jpa entitites using spring boot,
thymeleaf in MVC structure. The project is a web application aimed at displaying tutorials allowing
users to create delete update and read tutorials.

//db schema
`tutorials` (
   `id` int NOT NULL,
   `description` varchar(256) DEFAULT NULL,
   `level` int NOT NULL,
   `published` bit(1) DEFAULT NULL,
   `title` varchar(128) NOT NULL,
   PRIMARY KEY (`id`)
 )

//api endpoints
1. Get ("/tutorials")
    displays all the tutorials from the server

2. Get ("/tutorials/new")
    renders a form to create a new tutorial

3. Post ("/tutorials/save")
    saves the tutorial created in /tutorials/new to the database

4. Get ("/tutorials/{id}")
    renders the prefilled form with tutorial of id {id} to be edited

5. Get ("/tutorials/delete/{id}")
    deletes the specific tutorial with id {id}

5. Get ("/tutorials/{id}/published/{status}")
    changes the published status of the tutorial.