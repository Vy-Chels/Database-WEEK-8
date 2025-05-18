# Student Records Management System Database

## Project Description
This is a comprehensive MySQL database system designed for managing student records in an educational institution. The database supports various academic operations including student enrollment, course management, grade tracking, and faculty information management.

### Key Features
- Student information management
- Course and department organization
- Faculty records
- Enrollment tracking
- Grade management
- Address management
- Course prerequisites
- Performance optimized with proper indexing

## Database Structure
The database consists of the following main tables:
- `departments`: Stores department information
- `students`: Student personal and academic information
- `faculty`: Faculty member details
- `courses`: Course information and details
- `enrollments`: Manages student-course relationships
- `grades`: Academic performance records
- `student_addresses`: Student address information
- `course_prerequisites`: Course prerequisite relationships

## Setup Instructions

### Prerequisites
- MySQL Server (version 5.7 or higher)
- MySQL Command Line Client or MySQL Workbench

### Installation Steps

1. **Clone or download the repository**
   ```bash
   git clone [repository-url]
   ```

2. **Import the Database**
   
   Using MySQL Command Line:
   ```bash
   mysql -u your_username -p < student_records_db.sql
   ```

   Using MySQL Workbench:
   1. Open MySQL Workbench
   2. Connect to your MySQL server
   3. Go to File > Open SQL Script
   4. Select the `student_records_db.sql` file
   5. Click the lightning bolt icon to execute the script

3. **Verify Installation**
   ```sql
   USE student_records_db;
   SHOW TABLES;
   ```

### Database Credentials
- Database Name: `student_records_db`
- Default Character Set: UTF-8
- Default Collation: utf8mb4_general_ci

## Table Relationships
- One-to-Many:
  - Department to Students
  - Department to Faculty
  - Department to Courses
  - Student to Addresses
- Many-to-Many:
  - Students to Courses (via enrollments)
  - Courses to Prerequisites

## Performance Features
- Optimized indexes on frequently queried columns
- Proper foreign key constraints
- Timestamp tracking for all records
- Unique constraints to prevent duplicate entries

Link to ERD
https://app.diagrams.net/?src=about
