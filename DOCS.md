# Student Management System - Documentation

## System Overview
The Student Management System is a comprehensive Android application designed to manage student records locally and view user data from a remote API. It features a secure login, a dashboard for navigation, student registration with CRUD operations, and reporting capabilities.

## Features Implemented
1. **Login Module**: Secure access with field validation.
2. **Dashboard**: Centralized navigation using Material Design CardViews.
3. **Student Registration**: Form-based entry for student details (ID, Name, Email, Course, Phone) with Save, Update, Delete, and Clear functionalities.
4. **Local Database**: Persistent storage using SQLite for student records.
5. **Student List**: Scrollable list of students using RecyclerView with edit functionality.
6. **API Integration**: Integration with JSONPlaceholder API using Retrofit to fetch and display user data.
7. **Reports**: Statistical overview of registered students and course-wise distribution.
8. **Error Handling**: Comprehensive validation for forms, database operations, and network calls.

## Database Design
**Table: students**
- `id`: INTEGER PRIMARY KEY AUTOINCREMENT
- `studentId`: TEXT (Unique Identifier)
- `fullName`: TEXT
- `email`: TEXT
- `course`: TEXT
- `phone`: TEXT

## API Design
- **Endpoint**: `https://jsonplaceholder.typicode.com/users`
- **Method**: GET
- **Library**: Retrofit 2 with Gson Converter.
- **Model**: `User` class mapping name, email, phone, and company name.

## Testing Procedures
1. **Login Test**: Verify login with correct and incorrect credentials. Check empty field validation.
2. **Registration Test**: Add a new student, verify if it appears in the list.
3. **Update/Delete Test**: Select a student from the list, update their details, and verify changes. Test deletion.
4. **API Test**: Navigate to API Users and verify if data is fetched and displayed correctly.
5. **Reports Test**: Check if the total count and course-wise breakdown match the database content.
6. **Error Scenarios**: Test with no internet connection and invalid email formats.

## Conclusion
The Student Management System successfully demonstrates key Android development concepts including UI/UX design, local data persistence, networking, and modular code architecture (MVC).
