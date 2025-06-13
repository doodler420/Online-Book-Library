




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

![image](https://github.com/user-attachments/assets/8eaa61f9-a34d-4586-a5d8-0fb40dabebc1)
![image](https://github.com/user-attachments/assets/59789e34-b9d5-4b09-b768-98d2e9769fad)

---

## Database Schema

![image](https://github.com/user-attachments/assets/9f2139ac-4d7e-47fe-983a-09ffe8c73c09)

---

## ASP .NET app setup

- Create an ASP .NET MVC app using C# with the templates provided in Visual Studio Code 2022
- Retain default options and create the application
- Add a class to the Models folder and name it Book.cs
- Write the C# code for the schema logic here
- Now add a Controller with Razor views , refer to the base class Book.cs and name it BooksController.cs
- Now go to the views added in Views/Books after scaffolding is done
- Edit all views for the BooksController with bootstrap CSS tags , for example changing the color and layout of buttons and the page with accent colors
- Save the files
- Now add a Data folder and add ApplicationDbContext.cs file to the app
- Open NuGet Package Manager -> Package Manager Console
- Type the following commands to create a migration and update the database:

  Add-Migration -Name BookMigration -Context ApplicationDbContext 

  Update-Database -Migration BookMigration -Context ApplicationDbContext
- Local DB is created , launch the app and test it.


# Here are the screenshots for the application:

![image](https://github.com/user-attachments/assets/67a239c6-e5db-4389-95ff-b81859256724)
# Books
![image](https://github.com/user-attachments/assets/5caf0b51-b34b-4898-8543-1954ea7aeeed)
# Create
![image](https://github.com/user-attachments/assets/77e4290b-7e8d-4a2c-a043-eb2279506417)
# Edit
![image](https://github.com/user-attachments/assets/14ee4b52-d253-4a6b-b18b-63671c932012)
# Details
![image](https://github.com/user-attachments/assets/53620180-7278-4223-aef5-7aeb64cc2a74)
# Delete
![image](https://github.com/user-attachments/assets/c3d6490d-8798-47e0-9b24-b8c51af1f96e)




---


## Github Repository

- Add a repository on github with the name Online-Book-Library
- Clone it on your local machine
- Add the asp.net app folder into the cloned repository
- Run the following commands to push it to the github repository:

-git add .

-git commit -m "message"

-git push origin main

- Open github to verify committed files

---

## Azure Deployment

### Step 1 : Create App Service

- Go to Azure Portal
  
- Search for App Services → Click Create

- Fill in the following:

-Name: online-book-library-app

-Publish: Code

-Runtime stack: .NET 8 

Region: Choose nearest region

- Under Deployment, select:

-GitHub as source

-Choose your repository and branch (main)

-Review and Create

---

### Step 2 : Create Azure SQL Database

- Go to Azure Portal → Search SQL databases → Click Create

- Fill in:

-Database name: OnlineBookLibraryDb

-Server: Create new (note the admin username and password)

-Select Basic pricing tier (for free tier)

- After deployment, go to the new database → Click Set Server Firewall → Allow Azure Services and your IP.|

- In the Azure SQL database resource, click Connection strings

- Copy the ADO.NET connection string.

- Replace the placeholder in your appsettings.json file under "DefaultConnection"

---

###  Step 3 : Update Azure App Settings

- Go to Azure App Service → Configuration

- Under Application Settings, click + New application setting:

-Name: ConnectionStrings:DefaultConnection

-Value: Paste your full connection string 

- Save and restart the App Service

- Run Migrations on azure and update the database

---

### Step 4 : Test the deployed site

- Open your deployed site
- Check if everything works properly




