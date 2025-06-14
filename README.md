# 📅 Event Manager App for High School

Welcome to the **Event Manager App**, a cross-platform mobile application designed to streamline the management and registration of school events for students, teachers, and administrators. Developed using React Native for the front end and PHP with MySQL for the back end, this app enhances accessibility and control over school activities in a secure and user-friendly environment.

---

## 🚀 Features

### 👤 User Authentication

* Secure login and sign-up with OTP email verification.
* Different login experiences for **students**, **teachers**, and **admins**.
* "Forgot Password" functionality with OTP and email recovery.

### 🎓 Student Functionality

* View upcoming events in card format.
* Register for events using a structured form.
* Receive approval or disapproval notifications from teachers.

### 👩‍🏫 Teacher Functionality

* Add new events with custom details.
* View list of registered students for each event.
* Approve or disapprove students based on registration form responses.
* Receive email notifications upon student registrations.

### 🛠 Admin Functionality

* Add and manage teacher accounts (teachers can only register if added by the admin).
* View and remove teachers.
* View and change admin profiles.
* Add new admins (which removes the previous one).

---

## 🧑‍💻 Technologies Used

### Front-End:

* **React Native**
* **JavaScript**
* **CSS (Flexbox for layout and styling)**

### Back-End:

* **PHP**
* **MySQL**
* **Apache (via DigitalOcean server)**

### Email Services:

* **SMTP with PHPMailer**

  * Sends OTPs for sign-up and password recovery.
  * Notifies students of approval/disapproval status.

---

## 🗃 Database Schema

### `USER` Table:

| Field     | Description                               |
| --------- | ----------------------------------------- |
| Name      | Full name                                 |
| Email     | Unique user email                         |
| Class     | Student class                             |
| Section   | Class section                             |
| Phone No. | Contact number                            |
| Password  | User password                             |
| Type      | `1` = Student, `2` = Teacher, `3` = Admin |

### `EVENTS` Table:

| Field       | Description        |
| ----------- | ------------------ |
| Title       | Event title        |
| Description | Event details      |
| Fee         | Registration cost  |
| Age-Group   | Eligible age group |
| Venue       | Event location     |
| Start Date  | Beginning of event |
| End Date    | End of event       |

---

## 🔍 Navigation Overview

1. **Login Screen** – Initial screen with login and navigation to sign-up and password recovery.
2. **Sign-Up Screen** – Choose teacher or student sign-up, OTP-based verification.
3. **Events Screen** – Acts as the home screen for each user type, showing relevant options and events.
4. **Teacher Admin Functions** – Screens to add/view/remove teachers and admins.
5. **Student Registration** – View events and fill forms.
6. **Teacher Event Review** – View registrants and approve/disapprove with email notifications.

---

## ✅ Testing Overview

* **OTP Verification**: Ensures secure sign-up and password recovery.
* **Event Registration**: Validates form entries before accepting.
* **Approve/Disapprove Students**: Removes or retains students based on teacher decision.
* **Event Management**: Full flow from adding events to student participation.
* **User Management**: CRUD operations on admins and teachers.

---

## 🔄 Extensibility

This app is built with extensibility in mind. Thanks to:

* Modular design in React Native
* Centralized database schema
* Scalable PHP back-end

You can easily:

* Add new user roles
* Expand registration forms
* Add notification systems
* Integrate with calendars or third-party tools
