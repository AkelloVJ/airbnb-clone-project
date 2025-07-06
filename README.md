# Airbnb Clone Project

## Overview

The Airbnb Clone Project is a full-stack software development project that replicates core functionalities of Airbnb’s booking platform. It focuses on backend systems using Django, MySQL, and GraphQL to create secure, scalable APIs and features such as user registration, property listings, bookings, reviews, and payments. This blueprint is a hands-on opportunity to simulate professional-level backend development.

---

## Team Roles

- **Backend Developer:** Builds and maintains server-side application logic, APIs, and integrations with the database.
- **Database Administrator (DBA):** Designs, optimizes, and manages the relational database to ensure data integrity and performance.
- **DevOps Engineer:** Implements CI/CD pipelines and manages infrastructure using tools like Docker and GitHub Actions.
- **Security Engineer:** Ensures secure coding practices, implements authentication and authorization mechanisms, and enforces API security measures.
- **Technical Project Manager:** Oversees task delegation, manages timelines, and ensures team alignment on project goals.

---

## Technology Stack

- **Django:** A Python-based web framework used to build and manage RESTful APIs for backend logic and data interaction.
- **MySQL:** A relational database system used to store user, property, booking, and payment data.
- **GraphQL:** Enables flexible and efficient querying of backend data, providing the frontend with exactly what it needs.
- **Docker:** Containerization tool used to package the application and ensure consistency across environments.
- **GitHub Actions:** CI/CD automation tool used to test, build, and deploy code changes automatically.
- **Postman:** Used to test API endpoints during development.
- **Nginx (optional):** Reverse proxy server to serve the application in production.

---

## Database Design

**Key Entities and Relationships:**

1. **Users**
   - Fields: `id`, `name`, `email`, `password`, `role`
   - Relationships: One-to-many with Properties, Bookings, Reviews

2. **Properties**
   - Fields: `id`, `title`, `description`, `location`, `price_per_night`
   - Relationships: Many-to-one with Users, One-to-many with Bookings and Reviews

3. **Bookings**
   - Fields: `id`, `user_id`, `property_id`, `start_date`, `end_date`, `total_price`
   - Relationships: Many-to-one with Users and Properties

4. **Reviews**
   - Fields: `id`, `user_id`, `property_id`, `rating`, `comment`
   - Relationships: Many-to-one with Users and Properties

5. **Payments**
   - Fields: `id`, `booking_id`, `payment_method`, `status`, `transaction_id`
   - Relationships: One-to-one with Bookings

---

## Feature Breakdown

- **User Management:** Users can sign up, log in, and manage profiles securely. Includes both host and guest roles.
- **Property Management:** Hosts can list, edit, and delete properties, including uploading images and setting availability.
- **Booking System:** Guests can search for properties, book available listings, and view booking history.
- **Review System:** Users can leave ratings and comments on properties they've stayed at.
- **Payment Processing:** Handles booking payments through a secure and integrated gateway.

---

## API Security

- **Authentication:** JSON Web Tokens (JWT) will be used for secure user login and session handling.
- **Authorization:** Role-based access control (RBAC) will prevent unauthorized access to certain routes and data.
- **Rate Limiting:** Prevents abuse by limiting the number of API requests per user within a time window.
- **Input Validation:** All input data will be sanitized and validated to prevent SQL injection and XSS attacks.
- **HTTPS Enforcement:** All API traffic will be encrypted to protect user credentials and sensitive data.

**Why Security Matters:**
- Protects user data and privacy
- Prevents fraudulent bookings and payments
- Maintains platform integrity and trustworthiness

---

## CI/CD Pipeline

- **What is CI/CD?**
  - Continuous Integration (CI): Automatically tests code whenever changes are pushed.
  - Continuous Deployment (CD): Automatically builds and deploys the application to staging or production environments.

- **Tools Used:**
  - **GitHub Actions:** Automates testing and deployment workflows.
  - **Docker:** Ensures consistent environment configuration.
  - **Coverage.py & Pytest:** For running tests and tracking code coverage during CI runs.
  - **Heroku or DigitalOcean (optional):** For hosting the deployed backend.

---

## Manual Review

This project is designed to simulate real-world team dynamics, software architecture planning, and execution. While the current stage is documentation, future implementation will follow this blueprint.

---

