journalApp

A simple Spring Boot REST API for managing journal entries with CRUD operations: POST to create, GET to retrieve, PUT to update, and DELETE to remove entries. Built for quick setup and easy management.

(134 characters)

Repository

GitHub Repository

License

Licensed under the Apache License, Version 2.0.

Prerequisites





Java 17+



Maven



IntelliJ IDEA (or Eclipse/VS Code)



Postman (for API testing)

Setup Instructions





Clone the Repository:

git clone https://github.com/ARK1998/journalApp.git
cd journalApp



Open in IntelliJ IDEA:





Open IntelliJ IDEA.



Go to File > Open and select the journalApp directory.



Import as a Maven project if prompted.



Build the Project:





Run mvn clean install in the terminal or use IntelliJ’s Maven panel.



Run the Application:





Open src/main/java/com/scanify/journalApp/JournalApplication.java.



Right-click and select Run JournalApplication.



The API will start on http://localhost:8080.

API Endpoints

The API is hosted at http://localhost:8080/journal. Test endpoints using Postman.

POST - Create a Journal Entry





URL: http://localhost:8080/journal



Method: POST



Content-Type: application/json



Body:

{
    "id": "1",
    "title": "Happy",
    "content": "I am Happy :)"
}



Response: 201 Created with the created entry.

GET - Retrieve All Journal Entries





URL: http://localhost:8080/journal



Method: GET



Response: 200 OK with a list of entries:

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

PUT - Update a Journal Entry





URL: http://localhost:8080/journal/1



Method: PUT



Content-Type: application/json



Body:

{
    "id": "1",
    "title": "Super Happy",
    "content": "I am Super Happy :)"
}



Response: 200 OK with the updated entry.

DELETE - Delete a Journal Entry





URL: http://localhost:8080/journal/1



Method: DELETE



Response: 204 No Content

Testing with Postman





Install Postman: Download from postman.com.



Create a Collection:





Open Postman and create a collection named journalApp.



Add Requests:





Create requests for POST, GET, PUT, and DELETE using the URLs and JSON bodies above.



Set Content-Type: application/json for POST and PUT.



Test the API:





Start the application in IntelliJ.



Send requests to http://localhost:8080/journal.



Verify responses match expected status codes and data.

Example JSON Data

Test the API with these JSON examples in Postman:





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

Configuration





Database: Uses an in-memory H2 database by default. Configure application.properties for other databases (e.g., MySQL) if needed.



Port: Runs on 8080. Change server.port in application.properties if there’s a conflict.

Troubleshooting





Port Conflict: Update server.port in application.properties (e.g., server.port=8081).



Dependencies: Run mvn dependency:resolve if Maven issues occur.



Postman Errors: Ensure correct URL, method, JSON format, and that the application is running.

Contributing

Contributions are welcome! Fork the repository, make changes, and submit a pull request.
