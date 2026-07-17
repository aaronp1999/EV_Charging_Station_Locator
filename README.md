# EV Charging Station Locator

A complete EV charging management system consisting of two Android applications and an ASP.NET administration website.

## Project Overview

The EV Charging Station Locator helps electric-vehicle users discover charging stations and allows charging-station operators to manage station information. A separate admin website is included for central administration and monitoring.

## Project Modules

### 1. EV User Android App — `EChargeU`

The user application is intended for EV owners.

Main capabilities:

- User registration and login
- Search and view charging stations
- View charging-station details
- Access station location information
- Interact with the EV charging service through a mobile interface

### 2. Charging Station Android App — `EChargeS`

The service-station application is intended for charging-station operators.

Main capabilities:

- Station/operator login
- Manage charging-station information
- Update station-related details
- Handle information required by EV users
- Communicate with the central system

### 3. ASP.NET Admin Website

The admin website provides centralized management for the system.

Main capabilities:

- Administrator login
- Manage registered users
- Manage charging stations and operators
- Review system information
- Maintain application data through a web interface

## Technology Stack

- **Mobile applications:** Java, XML, Android Studio, Gradle
- **Admin website:** ASP.NET, C#, HTML, CSS, JavaScript
- **Database:** Microsoft SQL Server
- **Development tools:** Android Studio, Microsoft Visual Studio, SQL Server Management Studio
- **Version control:** Git and GitHub

## Suggested Repository Structure

```text
EV-Charging-Station-Locator/
├── Apps/
│   ├── EChargeU/              # EV user Android application
│   └── EChargeS/              # Charging-station Android application
├── Web/
│   └── ECharge Station/       # ASP.NET admin website
├── Database/                  # SQL scripts or database backup
├── Screenshots/               # Application screenshots
├── README.md
└── .gitignore
```

## Running the Android Applications

### Requirements

- Android Studio
- Android SDK
- Java Development Kit
- Android emulator or physical Android device
- Access to the project database/API, where required

### EV User App

1. Clone or download this repository.
2. Open Android Studio.
3. Select **Open**.
4. Open the `Apps/EChargeU` folder.
5. Allow Gradle synchronization to finish.
6. Configure the server URL and required credentials, if applicable.
7. Start an Android emulator or connect a physical device.
8. Click **Run**.

### Charging Station App

1. Open Android Studio.
2. Select **Open**.
3. Open the `Apps/EChargeS` folder.
4. Allow Gradle synchronization to finish.
5. Configure the server URL and required credentials, if applicable.
6. Start an emulator or connect a physical device.
7. Click **Run**.

## Running the ASP.NET Admin Website Locally

### Requirements

- Windows
- Microsoft Visual Studio with the **ASP.NET and web development** workload
- .NET Framework
- Microsoft SQL Server or SQL Server Express
- SQL Server Management Studio

### Steps

1. Open:

   ```text
   Web/ECharge Station/ECharge Station.sln
   ```

2. Restore any missing NuGet packages.

3. Create or restore the SQL Server database.

4. Open `Web.config` and update the database connection string.

Example:

```xml
<connectionStrings>
  <add name="EChargeConnection"
       connectionString="Data Source=YOUR_SERVER_NAME;Initial Catalog=YOUR_DATABASE_NAME;Integrated Security=True;"
       providerName="System.Data.SqlClient" />
</connectionStrings>
```

5. Build the solution.

6. Run the website by pressing **F5** or selecting **IIS Express**.

## Database Setup

Add the database script or backup inside a `Database` folder before sharing the repository.

Recommended files:

```text
Database/
├── EChargeDatabase.sql
└── Database-Setup-Instructions.md
```

Do not upload real usernames, passwords, private connection strings, API secrets, or production data.

## Deployment

The ASP.NET admin website can be deployed to a Windows-based Azure App Service with an Azure SQL Database.

Before deployment:

1. Back up the project.
2. Retarget the ASP.NET project to a supported .NET Framework version.
3. Test the website locally.
4. Move the local SQL Server database to Azure SQL Database.
5. Store the production connection string in Azure App Service configuration.
6. Publish the web project from Visual Studio.

## Screenshots

Add screenshots to a `Screenshots` folder and display them here.

```markdown
![User App](Screenshots/user-app-home.png)
![Station App](Screenshots/station-app-dashboard.png)
![Admin Website](Screenshots/admin-dashboard.png)
```

## Demo

Add one or more of the following:

- Live admin website link
- Android APK release links
- Short demonstration video
- Screenshots of all major modules

## Security Notes

- Never commit database passwords.
- Never commit private API keys.
- Remove `local.properties`.
- Remove `.vs`, `.idea`, `bin`, `obj`, `.gradle`, and generated `build` folders.
- Use environment variables or hosting-platform settings for deployment secrets.

## Future Enhancements

- Real-time charger availability
- Route navigation and map integration
- Charging-slot reservation
- Online payment support
- User ratings and reviews
- Push notifications
- Charging-session history
- Analytics dashboard

## Author

**Aaron P**

- GitHub: `https://github.com/YOUR-GITHUB-USERNAME`
- Portfolio: `ADD-YOUR-PORTFOLIO-LINK`
- LinkedIn: `ADD-YOUR-LINKEDIN-LINK`

## License

This project is provided for educational and portfolio purposes. Add a suitable open-source license only after confirming that all included code, images, libraries, and assets may be redistributed.
