# Online Book Library System (ASP.NET Core MVC)

## Project Overview

This project is a web-based library management system that allows users to manage a list of books. It supports basic CRUD (Create, Read, Update, Delete) operations and is built using ASP.NET Core MVC and Entity Framework Core. The application is deployed using Azure App Service and the book data is stored in an Azure SQL Database.

---

## Features

- Add a new book to the library
- View a list of all books
- Edit book details
- View individual book details
- Delete books from the library

---

## Technologies Used

- ASP.NET Core MVC
- Entity Framework Core (Code First)
- SQL Server (Azure-hosted)
- Razor Views with Bootstrap 4/5 for UI
- Visual Studio Code for development
- Git for version control
- Azure App Service for deployment

---

## Folder Structure

OnlineBookLibrary/
├── Controllers/
│ └── BooksController.cs
├── Models/
│ └── Book.cs
├── Views/
│ └── Books/
│ ├── Index.cshtml
│ ├── Create.cshtml
│ ├── Edit.cshtml
│ ├── Details.cshtml
│ └── Delete.cshtml
├── Data/
│ └── ApplicationDbContext.cs
├── Migrations/
├── appsettings.json
├── Program.cs / Startup.cs (depending on ASP.NET version)
└── README.md


