# SpotASpot - Property Searching Website

SpotASpot is a full-stack web application designed to help users find and explore properties for sale or rent. It features a clean and responsive design, allowing users to search properties based on various criteria and view detailed property information. The website also includes an admin dashboard for managing property listings.

## Project Overview

SpotASpot is a property-searching platform inspired by websites like Zillow. Users can browse properties, view property details, and admins can add, edit, or delete property listings. This project utilizes modern web technologies and follows the MVVM architecture to separate concerns and improve maintainability.

### Key Features:
- User authentication using JWT-based login system
- Property search functionality with multiple filter options
- Property details page
- Admin dashboard for adding, editing, and deleting properties
- Responsive design that works across various devices
- API documentation using Swagger

## Tech Stack

- **Frontend**: Blazor (C#), HTML, CSS (Bootstrap)
- **Backend**: .NET Core (Web API), C#
- **Database**: Microsoft SQL Server (MSSQL)
- **Authentication**: JWT (JSON Web Tokens)
- **APIs**: RESTful APIs
- **Others**: Swagger, Entity Framework Core, LINQ

## Project Setup

### Prerequisites
To run this project locally, you need to have the following installed:
- [.NET SDK 7.0 or higher](https://dotnet.microsoft.com/download)
- [Visual Studio Code](https://code.visualstudio.com/) or any other IDE of your choice
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) or any local database instance

### Backend Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/SpotASpot.git
    cd SpotASpot
    ```

2. Open the solution in Visual Studio or your preferred IDE.

3. Configure the database connection string in `appsettings.json`:
    ```json
    {
        "ConnectionStrings": {
            "DefaultConnection": "Server=.;Database=SpotASpotDB;Trusted_Connection=True;"
        }
    }
    ```

4. Run database migrations to set up the database schema:
    ```bash
    dotnet ef database update
    ```

5. Run the backend API:
    ```bash
    dotnet run
    ```

6. The backend API will be running at `http://localhost:5000` or the URL specified in your `appsettings.json`.

### Frontend Setup (Blazor)

1. In the frontend folder (`SpotASpot.Client`), open the solution.

2. Set up the API URL in the `PropertyService.cs` or any service that interacts with the API:
    ```csharp
    client.BaseAddress = new Uri("https://localhost:44357/");  // Update with your backend API URL
    ```

3. Build and run the frontend:
    ```bash
    dotnet build
    dotnet run
    ```

4. Open the application in your browser at `http://localhost:5000`.

### Swagger Documentation

Swagger documentation for the backend API is available at:
