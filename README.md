# 🚀 .NET Core and React App

This project follows the Udemy course:  
[Complete Guide to Building an App with .NET Core and React](https://www.udemy.com/course/complete-guide-to-building-an-app-with-net-core-and-react/)

---

## 📦 Tech Stack

- **Backend:** ASP.NET Core Web API
- **Frontend:** React
- **Database:** Entity Framework Core

---

## ▶️ Getting Started
> [!WARNING]: must have or create .\API\appsettings.json file containing database password

### 1. Restore Nuget Packages
> [NOTE]: only needed on fresh clone of project

```bash
dotnet restore
```

### 2. Run the API
> [NOTE]: this will also run migrations and seed database with test data if database doesn't exist

```bash
cd API
dotnet run
```

### 2. Run the client
```bash
cd client
npm run dev
```
---

## Migrations
Uses [dotnet-ef](https://www.nuget.org/packages/dotnet-ef) nuget package

> [NOTE]: from solution directory:

### Add Migration
```bash
dotnet ef migrations add InitialCreate -p Persistence -s API
```

### Run Migrations
```bash
dotnet ef database update -p Persistence -s API
```

### Delete Database
```bash
dotnet ef database drop -p Persistence -s API
```
