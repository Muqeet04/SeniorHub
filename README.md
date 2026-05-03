# SeniorHub - FYP Management System

A centralized digital platform for final year students to manage Final Year Projects (FYPs), find supervisors, and track graduation clearance. 

This implementation covers **all functional requirements** outlined in the SDA Assignment (FR-01 through FR-19), mapping the initial UML design to a full Java Swing desktop application.

## Features

- **Multi-Role Portals**: Dedicated dashboards for Students, Faculty, and System Admins.
- **Student Dashboard**: 
  - Manage profile and FYP groups.
  - Browse faculty directory and send supervision requests.
  - View project milestones and submit deliverables.
  - Apply to job postings and message alumni.
  - Track graduation clearance checklist and request transcripts.
- **Faculty Dashboard**: Review/grade submitted deliverables and manage incoming supervision requests.
- **Admin Dashboard**: Manage job postings and update student clearance statuses across departments.
- **Design Patterns**: Implements **MVC** (separating GUI from domain logic) and **Singleton** (`AppData` class) for consistent state management.

## Prerequisites
- Java Development Kit (JDK) 8 or higher.

## How to Compile and Run

### 1. Compile the Application

**On Windows (PowerShell):**
```powershell
& "C:\Program Files\Common Files\Oracle\Java\javapath\javac.exe" SeniorHubApp.java
```

**On Ubuntu / Linux (Terminal):**
```bash
javac SeniorHubApp.java
```

### 2. Run the Application

**On Windows (PowerShell):**
```powershell
& "C:\Program Files\Common Files\Oracle\Java\javapath\java.exe" SeniorHubApp
```

**On Ubuntu / Linux (Terminal):**
```bash
java SeniorHubApp
```

## Testing Credentials

The system comes pre-loaded with mock data for testing. You can use any of the following accounts:

### Student Accounts (Password: `pass123`)
- `hammad@uni.edu`
- `muqeet@uni.edu`
- `ali@uni.edu`

### Faculty Accounts (Password: `admin123`)
- `smith@uni.edu`
- `jane@uni.edu`
- `ahmed@uni.edu`

### Admin Account
- **Email**: `admin@uni.edu`
- **Password**: `admin123`
