# NotesCRUDApi (ASP.NET Core Web API)
This is a simple backend project built with ASP.NET Core Web API (.NET 8) and SQL Server. The project implements full CRUD (Create, Read, Update, Delete) operations for managing notes.

#Each note has:
A title
A description

The API is fully RESTful and was built as part of a backend development internship task.

#What the Project Does
This project exposes a REST API to perform the following operations on notes:
GET /notes – Retrieve all notes
GET /notes/{id} – Retrieve a single note by its ID
POST /notes – Create a new note
PUT /notes/{id} – Update an existing note
DELETE /notes/{id} – Delete a note

#How to Install and Run It
Prerequisites
.NET 8 SDK
SQL Server (LocalDB or full version)
Visual Studio 2022 or any code editor of your choice

#1. Clone the Repository
git clone https://github.com/HuzaifaBinAhmed/NotesCRUDApi.git
cd NotesCRUDApi
#2. Configure the Database
Update the appsettings.json file with your SQL Server connection string:

"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=NotesDb;Trusted_Connection=True;TrustServerCertificate=True;"
}
Replace YOUR_SERVER_NAME with your local SQL Server name (e.g., localhost, (localdb)\\MSSQLLocalDB, etc.).

#3. Run Migrations and Create the Database
Open the terminal or package manager console and run:

dotnet ef migrations add InitialCreate
dotnet ef database update
This will create the NotesDb database and generate the required tables.

#4. Run the Application
dotnet run

Swagger UI will also open automatically in the browser to help you test the API.


Update a note

Delete a note
