# Text Editor

**Text Editor** is an ASP.NET MVC project that provides a simple text editing experience with the integration of the TinyMCE WYSIWYG editor. This project is designed to allow developers to quickly set up and start editing text content with a modern UI.

## Features

- Simple text editing interface
- Rich text formatting provided by TinyMCE
- Easy configuration and customization
- Ready-to-use connection string configuration for your database

## Requirements

- [.NET Core 7 or later](https://dotnet.microsoft.com/download) (or the appropriate version specified in your project)
- An SQL-based database (like SQL Server)
- A valid [TinyMCE API key](https://www.tiny.cloud/get-tiny/) for the rich text editor, or you can use the free version with limited features

## Getting Started

Follow these steps to set up the project on your local machine:

### 1. Clone the Repository

Clone the repository using Git:

```bash
git clone https://github.com/yourusername/TextEditor.git
```

Then, navigate to the project directory:

```bash
cd TextEditor
```

### 2. Configure the Application Settings

Before running the application, you need to update the connection string and the TinyMCE API key in your configuration file.

#### Update `appsettings.json`

Open the `appsettings.json` file, and you will see a section similar to the one below:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "your DB Connection String"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "TinyMCE": {
    "ApiKey": "Your TinyMCE API key"
  },
  "AllowedHosts": "*"
}
```

- **Connection String:** Replace `"your DB Connection String"` with your actual database connection string. This is essential for the application to connect to your chosen database.
  
- **TinyMCE API Key:** Replace `"Your TinyMCE API key"` with the API key provided by TinyMCE. If you do not have an API key, you can [sign up for one](https://www.tiny.cloud/get-tiny/), or alternatively, you can use the free default version (though with limited features).

### 3. Restore Dependencies and Run the Project

Restore the project dependencies using the following command:

```bash
dotnet restore
```

Next, build and run the project:

```bash
dotnet run
```

The application should now be running locally, and you can access it via your web browser at `https://localhost:5001` or the appropriate URL provided in your console output.

## Additional Information

- **Database Migrations:** If using Entity Framework Core, remember to apply any necessary migrations.
  ```bash
  dotnet ef database update
  ```
- **Customizing TinyMCE:** For more information on how to customize TinyMCE, refer to the [TinyMCE documentation](https://www.tiny.cloud/docs/).



---

By following these steps, you should be able to download, configure, and run the **Text Editor** project successfully. Happy coding!