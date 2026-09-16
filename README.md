# Online Doctor Appointment System

A full-stack **Online Doctor Appointment System** built with the **MERN Stack**. The platform allows patients to find doctors, view their profiles, book appointments, make online payments, and manage their medical appointments.

The system provides separate modules for **Users, Doctors, and Admins**, with role-based authentication and authorization.

---

## 🚀 Features

### 👤 User / Patient Module

* User registration and login
* JWT-based authentication
* Role-based authorization
* User profile management
* Update personal information
* Upload profile picture
* Search doctors
* Filter doctors by specialization
* View doctor profiles
* View doctor availability
* Select appointment date and time
* Book doctor appointments
* Online appointment payment
* View payment status
* View upcoming appointments
* View previous appointments
* Cancel appointments
* Reschedule appointments
* View appointment details
* Receive appointment notifications
* View prescriptions and medical information
* Logout securely

---

### 👨‍⚕️ Doctor Module

* Doctor registration/login
* JWT authentication
* Doctor profile management
* Add/update specialization
* Add professional experience
* Add qualifications
* Add consultation fee
* Add clinic/hospital information
* Manage availability
* Set available appointment slots
* View booked appointments
* Accept/reject appointments
* Update appointment status
* View patient information
* Manage consultation records
* Add prescriptions
* Add medical notes
* View appointment history
* Manage profile picture
* Secure logout

---

### 🛠️ Admin Module

The Admin panel provides complete management of the platform.

#### User Management

* View all users
* View user details
* Update user information
* Block/unblock users
* Delete users

#### Doctor Management

* View all doctors
* Approve doctor accounts
* Reject doctor applications
* Update doctor information
* Block/unblock doctors
* Delete doctors
* Manage doctor specializations

#### Appointment Management

* View all appointments
* Monitor appointment status
* Manage cancelled appointments
* Manage completed appointments
* View appointment details

#### Payment Management

* View all payments
* Track successful payments
* Track failed payments
* View payment transaction details
* Monitor platform revenue

#### Dashboard

Admin dashboard provides:

* Total users
* Total doctors
* Total appointments
* Completed appointments
* Cancelled appointments
* Total payments
* Revenue statistics
* Doctor statistics
* Appointment statistics

---

# 🔐 Authentication & Authorization

The application uses **JWT (JSON Web Token)** based authentication.

### Authentication

Users can:

* Register
* Login
* Logout
* Access protected routes
* Manage their profiles

Passwords are securely hashed before being stored in the database.

### Authorization

The application uses **role-based access control**.

Available roles:

```text
User
Doctor
Admin
```

Each role has access only to the features allowed for that role.

Example:

```text
User → Book appointments
Doctor → Manage appointments and patients
Admin → Manage users, doctors, appointments and payments
```

---

# 🏥 Doctor Appointment System

Users can:

1. Search for a doctor
2. Select a specialization
3. View doctor profile
4. Check availability
5. Select date and time
6. Book an appointment
7. Make online payment
8. Receive booking confirmation
9. Attend consultation
10. View appointment history

---
# 📅 Appointment Management

Each appointment contains information such as:

```text
Patient
Doctor
Date
Time
Reason
Appointment Status
Payment Status
Created Date
```

Appointment statuses:

```text
Pending
Confirmed
Completed
Cancelled
Rejected
```

---

# 💊 Prescription Management

Doctors can create prescriptions for patients after consultation.

Prescription information may include:

* Patient
* Doctor
* Medicine name
* Dosage
* Frequency
* Duration
* Instructions
* Medical notes

Users can view their prescriptions from their account.

---

# 👤 Profile Management

### User Profile

Users can manage:

* Name
* Email
* Phone
* Gender
* Date of birth
* Address
* Profile picture

### Doctor Profile

Doctors can manage:

* Name
* Email
* Phone
* Specialization
* Qualifications
* Experience
* Consultation fee
* Clinic information
* Working hours
* Profile picture
* About/description

---

# 🔔 Notifications

The application can provide notifications for:

* Appointment booking
* Appointment confirmation
* Appointment cancellation
* Appointment rejection
* Payment confirmation
* Appointment reminders
* Prescription availability

Notifications can be implemented using email, in-app notifications, or other notification services.

---

# 🔎 Doctor Search & Filters

Users can search and filter doctors by:

* Doctor name
* Specialization
* Experience
* Consultation fee
* Availability
* Location

Example specializations:

```text
Cardiologist
Dermatologist
Neurologist
Dentist
Pediatrician
General Physician
Psychiatrist
Orthopedic
```

---

# 📊 Dashboard

### User Dashboard

```text
Upcoming Appointments
Previous Appointments
Payment History
Prescriptions
Profile
```

### Doctor Dashboard

```text
Today's Appointments
Upcoming Appointments
Completed Appointments
Patients
Earnings
Profile
Availability
```

### Admin Dashboard

```text
Total Users
Total Doctors
Total Appointments
Total Revenue
Pending Doctors
Recent Appointments
Payment Statistics
```

---

# 🧱 Tech Stack

## Frontend

* React.js
* JavaScript
* React Router
* Axios
* Context API / Redux
* Tailwind CSS / CSS
* React Toastify or similar notification library

## Backend

* Node.js
* Express.js
* REST API
* JWT Authentication
* bcrypt
* Middleware
* Role-based authorization

## Database

* MongoDB
* Mongoose

## Payment

* Stripe / Payment Gateway

## Other Technologies

* Git
* GitHub
* Cloudinary
* Postman
* Environment Variables

---

# 🗄️ Main Database Models

### User

```text
_id
name
email
password
phone
gender
dateOfBirth
address
profileImage
role
createdAt
```

### Doctor

```text
_id
name
email
password
phone
specialization
qualification
experience
consultationFee
clinic
availability
profileImage
isApproved
role
createdAt
```

### Appointment

```text
_id
user
doctor
date
time
reason
status
paymentStatus
paymentId
createdAt
```

### Payment

```text
_id
user
doctor
appointment
amount
transactionId
paymentStatus
paymentMethod
createdAt
```

### Prescription

```text
_id
patient
doctor
appointment
medicines
notes
createdAt
```

---

# 🔗 REST API Structure

## Authentication

```http
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
GET  /api/auth/me
```

## Users

```http
GET    /api/users/profile
PUT    /api/users/profile
DELETE /api/users/profile
```

## Doctors

```http
GET    /api/doctors
GET    /api/doctors/:id
PUT    /api/doctors/profile
PUT    /api/doctors/availability
```

## Appointments

```http
POST   /api/appointments
GET    /api/appointments
GET    /api/appointments/:id
PUT    /api/appointments/:id
DELETE /api/appointments/:id
```

## Payments

```http
POST /api/payments/create
POST /api/payments/verify
GET  /api/payments/history
```

## Prescriptions

```http
POST /api/prescriptions
GET  /api/prescriptions
GET  /api/prescriptions/:id
```

## Admin

```http
GET    /api/admin/users
GET    /api/admin/doctors
PUT    /api/admin/doctors/:id/approve
PUT    /api/admin/users/:id/status
DELETE /api/admin/users/:id
GET    /api/admin/appointments
GET    /api/admin/payments
GET    /api/admin/dashboard
```

---

# 🔒 Security

The application follows common web security practices:

* JWT authentication
* Password hashing
* Protected API routes
* Role-based authorization
* Authentication middleware
* Input validation
* Secure environment variables
* CORS configuration
* Payment verification
* Restricted admin routes


---

# 🔄 Application Flow

```text
                    Online Doctor Appointment System
                                |
             ┌──────────────────┼──────────────────┐
             ↓                  ↓                  ↓
           User              Doctor              Admin
             |                  |                  |
         Register           Register            Login
             |                  |                  |
           Login              Login             Dashboard
             |                  |                  |
       Search Doctor       Manage Profile      Manage Users
             |                  |                  |
       View Profile        Set Availability    Manage Doctors
             |                  |                  |
       Book Appointment    Manage Requests     Manage Appointments
             |                  |                  |
          Payment          Consult Patient     Manage Payments
             |                  |                  |
       Appointment         Prescription         Reports
             |
        Appointment
          History
```

---
  
  
# 👨‍💻 Author

**Muhammad Junaid**

Full Stack / MERN Stack Developer

