# Electric Bus Location Tracker System

## Overview

The **Electric Bus Location Tracker System** is a database-driven transportation management application developed for the electric bus network operating in Mianwali, Punjab, Pakistan. The system provides real-time bus tracking, route and stop management, driver duty scheduling, GPS-based location monitoring, and administrative reporting.

The project was developed as a Database Systems project and demonstrates the design and implementation of a normalized relational database (3NF) integrated with a Flutter-based mobile application and a Node.js REST API.

The system supports three user roles:

* **Passengers** – Search routes, view bus locations, and check estimated arrival times.
* **Drivers** – View assigned duties, start/complete duties, and share live GPS locations.
* **Administrators** – Manage buses, routes, schedules, drivers, duty assignments, and reports.

---

## Features

### Passenger Features

* Search available routes and stops
* View live bus locations on map
* Check estimated arrival times (ETAs)
* Save favorite routes and stops

### Driver Features

* View assigned duties
* Start and complete duties
* Share real-time GPS location
* View monthly duty history
* Manage profile information

### Administrator Features

* Manage buses and routes
* Manage drivers and user accounts
* Create and monitor duty assignments
* Generate operational reports
* View dashboard statistics

### Database Features

* Fully normalized relational schema (3NF)
* Stored Procedures for CRUD operations
* Database Triggers for business rule enforcement
* Audit logging
* Role-based access control
* Soft deletion support
* Real-time bus location storage

---

## System Requirements

### Software Requirements

* MySQL 8.0 or above
* Node.js (v18+ recommended)
* Express.js
* Flutter SDK
* Git
* Visual Studio Code / Android Studio

### Required Libraries & Packages

#### Backend

* express
* mysql2
* bcryptjs
* jsonwebtoken
* dotenv
* pdfkit

#### Flutter

* flutter_map
* geolocator
* http
* provider

### Hardware Requirements

* Minimum 4 GB RAM
* Dual-Core Processor or higher
* 1 GB Free Storage
* Android Device or Emulator

---

## Installation Instructions

### Step 1: Clone the Repository

```bash
git clone https://github.com/LaibaTaj31/Electric_Buses_Tracker_DB-project.git
cd Electric_Buses_Tracker_DB-project
```

### Step 2: Create the Database

Open MySQL and execute the DDL script:

```sql
SOURCE dbDDL.sql;
```

This will create:

* Tables
* Constraints
* Stored Procedures
* Triggers
* Views

### Step 3: Populate Sample Data

Run:

```sql
SOURCE dbDML.sql;
```

This will insert sample records into all tables.

### Step 4: Configure Backend

Navigate to the backend directory:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file and configure:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=electric_bus_tracker

JWT_SECRET=your_secret_key
```

Start the server:

```bash
npm start
```

### Step 5: Run Flutter Application

Navigate to the Flutter project directory:

```bash
cd Project_App
```

Install packages:

```bash
flutter pub get
```

Run the application:

```bash
flutter run
```

---

## Usage Instructions

### Administrator

1. Login using administrator credentials.
2. Manage buses, routes, and drivers.
3. Create duty assignments.
4. Monitor system statistics.
5. Generate operational reports.

### Driver

1. Login using driver credentials.
2. View assigned duties.
3. Start duty when scheduled.
4. Share live GPS location.
5. Complete duty after route completion.

### Passenger

1. Open the application.
2. Search routes and stops.
3. View live bus locations.
4. Check estimated arrival times.
5. Save favorite routes.

---

## Database Design Highlights

The database consists of the following major entities:

* Users
* Drivers
* Admins
* Buses
* Routes
* Stops
* Route Stop Details
* Schedules
* Duty Assignments
* Bus Locations
* Reports
* Audit Logs

### Database Components

* 12 Base Tables
* 20 Stored Procedures
* 4 Triggers
* 1 Reporting View
* 3NF Normalized Schema

---

## Project Structure

```text
Electric_Buses_Tracker_DB-project/
│
├── dbDDL.sql
├── dbDML.sql
├── Database Design Document.pdf
│
├── Project App/
│   ├── lib/
│   ├── assets/
│   ├── screens/
│   ├── widgets/
│   └── main.dart
│
├── backend/
│   ├── controllers/
│   ├── routes/
│   ├── middleware/
│   ├── models/
│   ├── services/
│   └── server.js
│
└── README.md
```

### Important Files

| File        | Description                                            |
| ----------- | ------------------------------------------------------ |
| `dbDDL.sql` | Creates database schema, procedures, triggers and view |
| `dbDML.sql` | Inserts sample data                                    |
| `main.dart` | Entry point of Flutter application                     |
| `server.js` | Backend server configuration                           |
| `README.md` | Project documentation                                  |

---

## Technology Stack

| Layer           | Technology                         |
| --------------- | ---------------------------------- |
| Frontend        | Flutter                            |
| Backend         | Node.js + Express.js               |
| Database        | MySQL 8                            |
| Authentication  | JWT + bcryptjs                     |
| Maps            | OpenStreetMap + flutter_map        |
| Reports         | PDFKit                             |
| Hosting         | AWS Elastic Beanstalk + Amazon RDS |
| Version Control | Git & GitHub                       |

---

## Contributors

* Mehroz Ali Khan
* Ali Abbas
* Laiba Taj

**Department of Computer Science**
**Namal University, Mianwali**

---

## License

This project was developed for academic and educational purposes as part of the Database Systems course at Namal University.
