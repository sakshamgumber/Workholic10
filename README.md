# Workholic

A Flask-based web application for job management, user authentication, and more.

## Features

- User registration and login (for workers and contractors)
- Job creation and listing
- Form filling and dashboard views
- Static assets (images, JS, CSS)
- Multiple database instances for different modules

## Project Structure

```
├── app.py                # Main Flask application
├── requirements.txt      # Python dependencies
├── requirments.txt       # (Alternate) Python dependencies
├── static/               # Static files (images, JS, CSS)
├── templates/            # HTML templates
├── instance/             # SQLite databases
├── env/                  # Python virtual environment
├── .vercel/              # Vercel deployment config
└── __pycache__/          # Python cache files
```

## Getting Started

1. **Install dependencies**  
   Use either `requirements.txt` or `requirments.txt`:
   ```sh
   pip install -r requirements.txt
   # or
   pip install -r requirments.txt
   ```

2. **Run the application**
   ```sh
   python app.py
   ```

3. **Access the app**  
   Open [http://localhost:5000](http://localhost:5000) in your browser.

## Databases

- Located in the `instance/` folder:
  - `contlogindb.db`
  - `fill_formdb.db`
  - `jobsdb.db`
  - `worklogindb.db`


# Project Flow Diagram

```mermaid
flowchart TD
    A[Home Page] --> B[Work Register]
    A --> C[Work Login]
    A --> D[Cont Register]
    A --> E[Cont Login]
    B --> C
    D --> E
    C --> F[Work Dashboard]
    E --> G[Cont Dashboard]
    G --> H[Create Job]
    G --> I[Job List]
    F --> I
    I --> J[Fill Form]
    F --> K[Past Forms]
    J --> F
    F --> L[Logout]
    G --> L
    A --> M[About]
```
- **Home Page**: Entry point for all users.
- **Work/Cont Register/Login**: Separate flows for worker and contractor registration/login.
- **Dashboards**: After login, users access their respective dashboards.
- **Job Management**: Contractors can create jobs; workers can view and apply.
- **Forms**: Workers fill forms for jobs; past forms can be viewed.
- **Logout/About**: Accessible from dashboards and home.


Images of Project

Home Page
<img width="2880" height="1618" alt="image" src="https://github.com/user-attachments/assets/b924d1cd-c812-49a3-a2c6-ef9688325f74" />

Worker Portal 
<img width="2860" height="1602" alt="image" src="https://github.com/user-attachments/assets/3ec29e4c-6d69-4a47-82cd-b046959b2360" />

About Us
<img width="2878" height="1628" alt="image" src="https://github.com/user-attachments/assets/6581150e-2dd5-4307-9cec-ea8b74f12c59" />

Contracter Portal
<img width="2880" height="1640" alt="image" src="https://github.com/user-attachments/assets/03b41333-9661-4694-a047-06058417e593" />


