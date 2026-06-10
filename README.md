# URL Shortener API

A RESTful API built with ASP.NET Core for generating shortened URLs and redirecting users to their original destinations.

This project was developed to practice backend development concepts such as API design, database persistence, dependency injection, and Entity Framework Core.

## Features

* Generate shortened URLs from long links
* Redirect users to the original URL using a short code
* Store URLs in a relational database
* RESTful API architecture
* Database migrations with Entity Framework Core
* Swagger/OpenAPI integration

## Tech Stack

### Backend

* C#
* ASP.NET Core Web API
* Entity Framework Core

### Database

* SQL Server

### Tools

* Swagger / OpenAPI
* Git
* GitHub
* Docker

## Architecture

The project follows a simple and maintainable backend architecture:

```text
API Endpoints
      ↓
Services
      ↓
Entity Framework Core
      ↓
SQL Server Database
```

Project structure:

```text
UrlShortener
│
├── Entities
│   └── ShortenedUrl
│
├── Models
│   └── ShortenUrlRequest
│
├── Services
│   └── UrlShorteningService
│
├── Migrations
│
├── Extensions
│
├── ApplicationDbContext
└── Program
```

## How It Works

1. A user submits a long URL.
2. The API generates a unique short code.
3. The original URL and short code are stored in the database.
4. When the shortened URL is accessed, the API redirects the user to the original address.

## Getting Started

### Prerequisites

* .NET SDK
* SQL Server
* Docker (optional)

### Clone the Repository

```bash
git clone https://github.com/ocainadev/url-shortener-api.git
cd url-shortener-api
```

### Configure the Database

Update the connection string in:

```text
appsettings.json
```

### Apply Migrations

```bash
dotnet ef database update
```

### Run the Application

```bash
dotnet run
```

The API will be available locally and Swagger documentation can be accessed through the configured endpoint.

## Concepts Demonstrated

* RESTful API Development
* Dependency Injection
* Entity Framework Core
* Database Migrations
* SQL Server Integration
* URL Encoding and Generation
* Clean Project Organization

## Future Improvements

* User authentication and authorization
* URL expiration dates
* Click analytics
* Custom short codes
* Rate limiting
* Unit and integration tests
* Docker Compose support
* Caching with Redis

## Author

Cainã Santos

GitHub: https://github.com/ocainadev

## License

This project is available for educational and portfolio purposes.
