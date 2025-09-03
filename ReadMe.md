journalApp

A simple Spring Boot REST API for managing journal entries, demonstrating CRUD operations: POST to create, GET to retrieve, PUT to update, and DELETE to remove journal entries. Built with Spring Boot for quick setup and easy management.

Repository

GitHub Repository

License

This project is licensed under the Apache License, Version 2.0. See the LICENSE file for details.

Prerequisites





Java 17 or later



Maven



IntelliJ IDEA (or another IDE like Eclipse)



Postman (for testing API endpoints)

Setup Instructions





Clone the Repository:

git clone http://github.com/ARK1998/journalApp.git
cd journalApp



Open in IntelliJ IDEA:





Open IntelliJ IDEA.



Select File > Open and choose the journalApp directory.



Ensure the project is recognized as a Maven project (you may need to click Import as Maven Project).



Build the Project:





Run mvn clean install in the terminal or use IntelliJ's Maven panel to build the project.



Run the Application:





Locate the main application class (e.g., JournalAppApplication.java) in src/main/java.



Right-click and select Run 'JournalAppApplication'.



The application will start on http://localhost:8080.

API Endpoints

The API is accessible at http://localhost:8080/journal. Below are the CRUD operations you can test using Postman.

1. POST - Create a Journal Entry





URL: http://localhost:8080/journal



Method: POST



Content-Type: application/json



Body (example):

{
"id": "1",
"title": "Happy",
"content": "I am Happy :)"
}



Response: 201 Created with the created entry.

2. GET - Retrieve All Journal Entries





URL: http://localhost:8080/journal



Method: GET



Response: 200 OK with a list of entries, e.g.:

[
{
"id": "1",
"title": "Happy",
"content": "I am Happy :)"
},
{
"id": "2",
"title": "Ok",
"content": "I am Ok"
},
{
"id": "3",
"title": "Travel",
"content": "I am Traveling :)"
}
]

3. PUT - Update a Journal Entry





URL: http://localhost:8080/journal/1



Method: PUT



Content-Type: application/json



Body (example):

{
"id": "1",
"title": "Super Happy",
"content": "I am Super Happy :)"
}



Response: 200 OK with the updated entry.

4. DELETE - Delete a Journal Entry





URL: http://localhost:8080/journal/1



Method: DELETE



Response: 204 No Content

Testing with Postman





Install Postman: Download and install Postman from postman.com.



Create a New Collection:





Open Postman and create a new collection named journalApp.



Add Requests:





Create requests for each endpoint (POST, GET, PUT, DELETE) using the URLs and JSON bodies provided above.



Set the appropriate HTTP method and Content-Type: application/json for POST and PUT requests.



Test the API:





Start the Spring Boot application in IntelliJ IDEA.



Send requests via Postman to http://localhost:8080/journal.



Verify responses match the expected status codes and data.

Example JSON Data

Use the following JSON examples in Postman to test the API:





Entry 1:

{
"id": "1",
"title": "Happy",
"content": "I am Happy :)"
}



Entry 2:

{
"id": "2",
"title": "Ok",
"content": "I am Ok"
}



Entry 3:

{
"id": "3",
"title": "Travel",
"content": "I am Traveling :)"
}

Troubleshooting





Port Conflict: If 8080 is in use, update the server.port in application.properties to another port (e.g., 8081).



Dependencies: Ensure all Maven dependencies are resolved. Run mvn dependency:resolve if issues occur.



Postman Errors: Verify the correct URL, method, and JSON format. Check that the application is running.

Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.