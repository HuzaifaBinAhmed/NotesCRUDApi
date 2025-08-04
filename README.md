# NotesCRUD API (ASP.NET Core Web API)

This is a simple backend project built with **ASP.NET Core Web API (.NET 8)** and **SQL Server**. The project implements full CRUD (Create, Read, Update, Delete) operations for managing notes.

Each note has:
- A title  
- A description

The API is fully RESTful and was built as part of a backend development internship task.

---

## What the Project Does

This project exposes a REST API to perform the following operations on notes:

- GET /notes – Retrieve all notes  
- GET /notes/{id} – Retrieve a single note by its ID  
- POST /notes – Create a new note  
- PUT /notes/{id} – Update an existing note  
- DELETE /notes/{id} – Delete a note

---

## How to Install and Run It

Prerequisites:
- .NET 8 SDK
- SQL Server (LocalDB or full version)
- Visual Studio 2022 or any code editor of your choice

Clone the Repository:
git clone https://github.com/HuzaifaBinAhmed/NotesCRUDApi.git
cd NotesCRUDApi

Configure the Database:
Open appsettings.json and update the connection string like this:

"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=NotesDb;Trusted_Connection=True;TrustServerCertificate=True;"
}

Replace YOUR_SERVER_NAME with your local SQL Server instance (e.g., localhost, (localdb)\MSSQLLocalDB, etc.).

Apply Migrations and Create the Database:
Open the terminal or Package Manager Console and run the following commands:

dotnet ef migrations add InitialCreate
dotnet ef database update

This will create the NotesDb database and generate the required tables.

Run the Application:
dotnet run

Once it starts, open your browser and go to:
https://localhost:{port}/swagger

Swagger UI will open, where you can test all endpoints (GET, POST, PUT, DELETE).
