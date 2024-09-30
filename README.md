Recipe Management System

Overview

The Recipe Management System is a Java-based application that allows users to manage their recipes through a simple command-line interface. Users can create, read, update, and delete recipes stored in a MySQL database. The application also implements caching to improve performance for frequently accessed recipes.

Features

Create a Recipe: Users can add new recipes with their name, ingredients, instructions, and preparation time.

Read a Recipe: Users can fetch recipes by ID, with support for caching to optimize retrieval times.

Update a Recipe: Users can update the preparation time of existing recipes.

Delete a Recipe: Users can delete recipes from both the cache and the database.


Technologies Used

Java: The application is built using Java.

JDBC: For connecting to a MySQL database.

MySQL: The database used to store recipes.

Concurrency: Utilizes Java's concurrency framework to manage cache and database operations.


Prerequisites

Java Development Kit (JDK) installed on your machine.

MySQL database server running locally.

MySQL Connector/J library for JDBC connectivity.


A MySQL database named receipemanagement with a table named recipes having the following schema:

CREATE TABLE recipes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    ingredients TEXT NOT NULL,
    instructions TEXT NOT NULL,
    prep_time INT NOT NULL
);

Installation

1.Clone the Repository:

git clone https://github.com/20481A0536/RecipeManagement.git

cd RecipeManagement

2.Configure Database Connection:

Open the RecipeManagement.java file and set the database URL, username, and password according to your MySQL setup.

3.Compile the Application:

javac RecipeManagement.java

4.Run the Application:

java RecipeManagement


Usage

Upon starting the application, the user will see a menu with the following options:

1. Create Recipe
2. Read Recipe
3. Update Recipe
4. Delete Recipe
5. Exit
Users can enter their choice, and follow the prompts to manage recipes.

Caching

The application includes a caching mechanism that stores frequently accessed recipes in memory, reducing database calls and improving performance. The cache has a configurable size and removes the least recently used (LRU) item when it exceeds its limit.


Error Handling

The application includes basic error handling for SQL exceptions, ensuring that any issues with database connectivity or operations are reported to the user.


Contributing

Contributions are welcome! If you'd like to contribute to the project, please fork the repository and submit a pull request.


