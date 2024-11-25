# CS_120
Flask Appointment Booking System
This is a Flask-based appointment booking system that enables users to register, log in, book appointments with doctors, and manage their profiles. The system leverages CSV files for storing user data and appointment details.

Features
User Authentication: Sign-up, login, and session management.
Appointment Management: Book, view, and manage appointments.
Profile Management: Update user profiles with personal details.
API Support: Retrieve appointment data in JSON format.
CSV-based Storage: Users and appointments are stored in users.csv and appointments.csv.
Logging: Comprehensive logging for debugging and monitoring.
Technologies Used
Python (Flask Framework)
HTML, CSS for UI
CSV for data storage
Prerequisites
Python 3.7+
Flask (pip install flask)
Setup Instructions
Clone the repository:

bash
Copy code
git clone <repository-url>
cd <project-directory>
Install dependencies:

bash
Copy code
pip install flask
File Initialization: Ensure that users.csv and appointments.csv exist in the root directory or are created automatically when the app runs for the first time.

Run the application:

bash
Copy code
python app.py
Access the application: Open your browser and navigate to http://127.0.0.1:5000/.

Folder Structure
graphql
Copy code
├── app.py                # Main application file
├── templates/            # HTML files for rendering
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── main_dashboard.html
│   ├── account.html
│   ├── billing.html
│   ├── prescriptions.html
│   └── appointments.html
├── users.csv             # Stores user details
├── appointments.csv      # Stores appointment details
└── README.md             # Project documentation
Endpoints
Public Routes
/ - Redirects to login or dashboard.
/signup - User registration page.
/login - User login page.
Protected Routes (Login Required)
/logout - Log out of the application.
/dashboard - Main dashboard for users.
/book_appointment - Book a new appointment.
/update_profile - Update user profile.
/account - User account page.
/billing - Billing information.
/prescriptions - Prescription details.
/appointments - View all user appointments.
API
/get_available_slots/<doctor> - Fetch available slots for a specific doctor.
/api/appointments - Retrieve all appointments in JSON format.
Key Functions
login_required: Decorator to protect routes from unauthorized access.
initialize_csv_files: Creates users.csv and appointments.csv if they don’t exist.
get_user_details: Fetch user details from users.csv.
update_user_details: Update user details in users.csv.
get_user_appointments: Retrieve all appointments for a user.
book_appointment_helper: Handles booking logic, ensuring time slot availability.
Notes
Environment Variables: Replace your_secret_key_here in the code with a secure value for production.
File Paths: Ensure users.csv and appointments.csv have the correct permissions for reading and writing.
Deployment: For deployment, configure a production-ready server like Gunicorn or uWSGI, and set up a reverse proxy with Nginx.
Logging
All significant actions and errors are logged to the console for monitoring and debugging.

Future Enhancements
Database Integration: Replace CSV files with a relational database (e.g., MySQL or PostgreSQL).
Improved Authentication: Use Flask-Login for session management and bcrypt for password hashing.
Dynamic UI: Enhance the front-end with modern JavaScript frameworks (React or Vue.js).
Appointment Reminders: Add email or SMS notifications for upcoming appointments.
Feel free to adapt or expand the functionality of the application as needed! 🎉
