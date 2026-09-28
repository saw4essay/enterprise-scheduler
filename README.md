# Enterprise Scheduler

An enterprise-grade scheduling and workforce management system built with Python and FastAPI. The system is designed to simplify employee scheduling, prevent shift conflicts, optimize resource allocation, and generate useful reports for business operations.

---

## Overview

Enterprise Scheduler is a scheduling and workforce management application designed to help organizations efficiently manage employee shifts, availability, working hours, and operational resources.

The system focuses on automated scheduling, conflict detection, resource optimization, data analysis, and report generation.

---

## Features

- **Automated Scheduling:** Create and organize employee schedules efficiently based on employee availability and working-hour constraints.
- **Conflict Detection & Resolution:** Detect overlapping shifts and identify scheduling conflicts.
- **Shift & Workforce Management:** Manage employee shifts, availability, working hours, and team schedules.
- **Resource Optimization:** Improve resource allocation by balancing workloads across available personnel.
- **Data Analysis:** Analyze scheduling and workforce data using Pandas and NumPy.
- **Report Generation:** Generate professional PDF reports using ReportLab.
- **Excel Export:** Export schedules and reports to Excel using OpenPyXL.
- **Database Management:** Store and manage application data using SQLite and SQLAlchemy.
- **REST API:** Provide application functionality through a FastAPI-based API.
- **Scalable Architecture:** Organized to support future improvements and additional scheduling features.

---

## Tech Stack

- **Language:** Python 3.10+
- **Framework / API:** FastAPI
- **Data Analysis & Processing:** Pandas, NumPy
- **Database:** SQLite
- **ORM:** SQLAlchemy
- **PDF Generation:** ReportLab
- **Excel Generation:** OpenPyXL
- **API Server:** Uvicorn
- **Version Control:** Git & GitHub

---

## Project Structure

    enterprise-scheduler/
    │
    ├── app/
    │   ├── main.py
    │   ├── database.py
    │   ├── models.py
    │   ├── schemas.py
    │   ├── crud.py
    │   │
    │   ├── routers/
    │   │   ├── employees.py
    │   │   ├── schedules.py
    │   │   └── reports.py
    │   │
    │   ├── services/
    │   │   ├── scheduler.py
    │   │   ├── conflict_checker.py
    │   │   └── optimizer.py
    │   │
    │   └── utils/
    │       ├── pdf_export.py
    │       └── excel_export.py
    │
    ├── tests/
    │   ├── test_employees.py
    │   ├── test_schedules.py
    │   └── test_reports.py
    │
    ├── screenshots/
    │   ├── fastapi-docs.png
    │   └── dashboard.png
    │
    ├── requirements.txt
    ├── .gitignore
    ├── LICENSE
    ├── README.md
    └── scheduler.db

---

## Installation

Follow these steps to set up and run the project locally.

### Prerequisites

- Python 3.10 or higher
- Git installed on your system
- pip installed

### 1. Clone the Repository

    git clone https://github.com/saw4essay/enterprise-scheduler.git
    cd enterprise-scheduler

### 2. Create a Virtual Environment

#### Windows

    python -m venv venv
    venv\Scripts\activate

#### Linux / macOS

    python3 -m venv venv
    source venv/bin/activate

### 3. Install Dependencies

    pip install -r requirements.txt

### 4. Run the Application

    uvicorn app.main:app --reload

The API will be available at:

    http://127.0.0.1:8000

FastAPI interactive documentation:

    http://127.0.0.1:8000/docs

Alternative API documentation:

    http://127.0.0.1:8000/redoc

---

## Usage

After starting the application, open the FastAPI interactive documentation at:

    http://127.0.0.1:8000/docs

Typical workflow:

1. Add employees and their availability.
2. Create scheduling requirements.
3. Generate employee shifts.
4. Check for scheduling conflicts.
5. Optimize resource allocation.
6. Export schedules to Excel.
7. Generate PDF reports.

---

## API Endpoints

### Employees

    GET    /employees
    GET    /employees/{employee_id}
    POST   /employees
    PUT    /employees/{employee_id}
    DELETE /employees/{employee_id}

### Schedules

    GET    /schedules
    GET    /schedules/{schedule_id}
    POST   /schedules
    PUT    /schedules/{schedule_id}
    DELETE /schedules/{schedule_id}

### Scheduling

    POST   /schedules/generate
    POST   /schedules/check-conflicts
    POST   /schedules/optimize

### Reports

    GET    /reports/schedules/pdf
    GET    /reports/schedules/excel

> Note: API endpoints may evolve as the project implementation is developed.

---

## Screenshots

### FastAPI Documentation

![FastAPI Documentation](screenshots/fastapi-docs.png)

### Application Dashboard

![Application Dashboard](screenshots/dashboard.png)

---

## Future Improvements

- Add authentication and role-based access control.
- Add a web-based dashboard for schedule management.
- Add advanced scheduling algorithms.
- Add support for PostgreSQL and other production databases.
- Add employee notifications and reminders.
- Add calendar integration.
- Improve resource optimization algorithms.
- Add automated testing and CI/CD pipelines.
- Add Docker support for easier deployment.
- Add cloud deployment support.

---

## License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for more information.
