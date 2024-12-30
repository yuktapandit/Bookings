# Hall Booking System

## Overview
The Hall Booking System is a web application designed to manage bookings for various halls. It includes features to create, read, update, and delete bookings. The backend is built using Spring Boot with a PostgreSQL database, and the frontend is implemented in React.

---

## Features
1. **CRUD Operations**:
   - Add, view, update, and delete bookings.
2. **JAVA Microservices**:
   - Entity, Controller, Repository, and Services.
3. **CORS Support**:
   - Configured to allow requests from `http://localhost:3000`.
4. **Customizable Halls**:
   - Predefined list of halls with an option to select during booking.
5. **Real-time Calculations**:
   - Auto-calculates total charges based on rent and additional charges.

---

## Technologies Used

### Backend
- **Spring Boot**
  - REST API development
  - Dependency injection using `@Autowired`
  - Data access with JPA Repository
- **PostgreSQL**
  - Relational database for storing booking details
- **PL/pgSQL**
  - Stored procedures for database operations
- **Spring Web MVC**
  - CORS configuration

### Frontend
- **React.js**
  - UI development with components like BookingForm and BookingList
  - State management with React Hooks (`useState`, `useEffect`)
- **CSS**
  - Styling for form and list views

---

## Backend Implementation

### Key Files
- **Main Application**: `HallBookingApplication.java`
  - Entry point for the Spring Boot application.
- **Entity**: `HallBooking.java`
  - Defines the data model for bookings.
- **Repository**: `HallBookingRepository.java`
  - Provides JPA repository for database interactions.
- **Service**: `HallBookingService.java`
  - Contains business logic for booking operations.
- **Controller**: `HallBookingController.java`
  - REST API endpoints for bookings.
- **CORS Configuration**: `CorsConfig.java`
  - Enables cross-origin requests.

### Database
- **Stored Procedures**:
  - `insert_booking`: Inserts a new booking.
  - `update_booking`: Updates an existing booking.
  - `delete_booking`: Deletes a booking by ID.
  - `get_all_bookings`: Fetches all bookings.

---

## Frontend Implementation

### Key Components
1. **BookingForm**:
   - Collects user input for creating or updating bookings.
   - Auto-calculates the total amount based on rent and additional charges.
2. **BookingList**:
   - Displays a list of bookings with options to edit or delete.

### Key Features
- **Real-time Total Calculation**:
  - Updates the total field dynamically based on input.
- **Error Handling**:
  - Alerts on submission errors or failed operations.
- **Navigation**:
  - Built with React Router for seamless transitions.

---

## Setup Instructions

### Prerequisites
- **Backend**: Java 17+, Maven, PostgreSQL
- **Frontend**: Node.js, npm

### Steps
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd hall-booking-system
   ```

2. **Backend Setup**:
   - Import the backend project into your favorite IDE (e.g., IntelliJ, Eclipse).
   - Configure the database in `application.properties`.
   - Run the Spring Boot application.

3. **Database Setup**:
   - Execute the provided SQL scripts to set up the `hall_booking` database and stored procedures.

4. **Frontend Setup**:
   ```bash
   cd frontend
   npm install
   npm start
   ```

5. **Access the Application**:
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:8080/api/bookings`

---

## API Endpoints

### Base URL
`http://localhost:8080/api/bookings`

### Endpoints
- **GET** `/` - Fetch all bookings.
- **POST** `/` - Create a new booking.
- **PUT** `/` - Update an existing booking.
- **DELETE** `/{id}` - Delete a booking by ID.

---

## Screenshots
1. **Booking Form**: Captures details for new bookings.
   ![image](https://github.com/user-attachments/assets/77348e74-3c2b-4a45-8021-f926153d03e1)
   ![image](https://github.com/user-attachments/assets/36d17e6f-6048-43a2-b306-26262e1ca7be)

3. **Booking List**: Displays all bookings with edit and delete options.
   ![image](https://github.com/user-attachments/assets/8837db80-79b6-4de4-8a4b-90bb956684fc)


---

## License
This project is licensed under the MIT License.

---

## Video OverView
https://www.loom.com/share/a7cb73dc56274ed3be8efac7ede5c93d?sid=cd2133cc-a147-4e33-b9e0-bbdc65e15370

