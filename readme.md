# Text Editor

Text Editor is an ASP.NET MVC project that provides a feature-rich text editing experience powered by the TinyMCE editor. Follow the instructions below to get the project up and running on your local machine.

## Prerequisites

- [.NET 7 SDK or higher](https://dotnet.microsoft.com/download)
- A supported database server (e.g., SQL Server)
- A [TinyMCE API key](https://www.tiny.cloud/) (free or paid, depending on your needs)

## Getting Started

### 1. Clone or Download the Repository

Clone the repository using Git:

```bash
git clone https://github.com/yourusername/text-editor.git
cd text-editor
```

Or simply download the ZIP and extract it.

### 2. Configure the Application Settings

Open the `appsettings.json` file in your favorite code editor and update the following sections:

- **Connection String:** Replace `"your DB Connection String"` with your actual database connection string.
- **TinyMCE API Key:** Replace `"Your TinyMCE API key"` with your actual TinyMCE API key.

Example `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=your_server;Database=your_db;User Id=your_user;Password=your_password;"
  },
  "TinyMCE": {
    "ApiKey": "your_actual_api_key"
  }
}
```

### 3. Apply Entity Framework Migrations

After updating your connection string, you need to apply the EF migrations to set up the database schema.

Open a terminal or the Package Manager Console (in Visual Studio) and run the following commands:

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

This command applies all pending migrations and creates (or updates) the necessary database structure.

### 4. Run the Application

Start the application by running:

```bash
dotnet run
```

Or, if you're using Visual Studio, press `F5` or click on the "Run" button.

Your application should now launch in your default web browser.

## TinyMCE Integration

The Text Editor project uses the TinyMCE editor for rich text editing. Ensure you have a valid API key set in `appsettings.json` for the editor to work correctly.

---

Feel free to customize this file further to fit your project's needs. Happy coding!