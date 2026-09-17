# SHS Enrollment System

A simple Senior High School (SHS) Enrollment System developed using Python. This console-based application allows users to enroll students, validate student information, select an SHS track and strand, save enrollment records, and view enrolled students.

## Project Description

The SHS Enrollment System is a console-based Python application designed to manage basic student enrollment information.

The system provides a menu-driven interface that allows users to:

- Enroll a student
- Enter student information
- Validate required information
- Select an SHS track and strand
- Save student records using file handling
- Load previously saved student records
- View enrolled students
- Exit the application

The project demonstrates fundamental Python programming concepts and the use of file handling for data persistence.

## Features

### 1. Student Enrollment

The system collects the following student information:

- Student ID
- First Name
- Middle Name
- Last Name
- Age
- Gender
- Grade Level
- Track
- Strand
- Contact Number
- Address
- Guardian Name

### 2. Input Validation

The system validates important student information before saving a record.

Examples include:

- Student ID cannot be empty.
- First name and last name cannot be empty.
- Age must be a positive integer.
- Gender must be selected as Male or Female.
- Grade level must be Grade 11 or Grade 12.
- Contact number must contain digits only.
- Address and guardian name cannot be empty.

### 3. SHS Tracks and Strands

The system allows users to select from the following tracks and strands:

#### Academic Track

- STEM
- ABM
- HUMSS
- GAS

#### TVL Track

- ICT - Programming
- ICT - CSS

### 4. File Handling and Data Persistence

The system uses a text file named `students.txt` to store enrolled student records.

Each student record is saved using the pipe character (`|`) as the separator.

The system can also load previously saved records when the program starts.

The `students.txt` file is excluded from GitHub using `.gitignore` to help prevent student information from being accidentally uploaded to the public repository.

### 5. View Enrolled Students

Users can select the View Enrolled Students option from the main menu to display all saved enrollment records.

If there are no enrolled students, the system displays:

```text
No students enrolled.
```

## Technologies Used

- Python
- Python dictionaries
- Lists
- Functions
- Conditional statements
- Loops
- Input validation
- File handling
- Text file storage

## Project Structure

```text
SHSEnrollmentFormV1/
├── .gitignore
├── README.md
├── enrollment.py
└── main.py
```

### `main.py`

Contains the main menu and controls the overall flow of the application.

### `enrollment.py`

Contains the student enrollment functions, input validation, SHS track and strand selection, student display, and file handling.

## Requirements

- Python 3.x
- No external Python libraries are required.

## How to Run

1. Download or clone the repository.
2. Open a terminal in the project folder.
3. Run the following command:

```bash
python main.py
```

The program will display the main menu.

## Main Menu

The application provides the following options:

```text
1. Enroll Student
2. View Enrolled Students
3. Exit
```

### Enroll Student

Select option `1` to enter and save a new student's enrollment information.

### View Enrolled Students

Select option `2` to display the student records currently stored in the system.

### Exit

Select option `3` to close the application.

## Enrollment Process

The enrollment process follows these general steps:

```text
Start
  |
  v
Main Menu
  |
  +--> Enroll Student
  |       |
  |       v
  |   Enter Student Information
  |       |
  |       v
  |   Validate Information
  |       |
  |       v
  |   Select Track and Strand
  |       |
  |       v
  |   Save Student Record
  |
  +--> View Enrolled Students
  |
  +--> Exit
  |
  v
End
```

## Program Functions

### `main.py`

- `main()` - Displays the main menu and handles the user's selected option.

### `enrollment.py`

- `load_students()` - Loads previously saved student records from `students.txt`.
- `save_student(student)` - Saves a student record to `students.txt`.
- `add_student()` - Collects student information, validates it, and saves the record.
- `choose_strand()` - Allows the user to select an SHS track and strand.
- `validate_student(student)` - Checks required student information.
- `view_students()` - Displays enrolled student records.

## Python Concepts Demonstrated

This project demonstrates the following Python concepts:

- Variables and data types
- Lists
- Dictionaries
- Functions
- Loops
- Conditional statements
- Exception handling
- User input
- String processing
- File handling
- Basic data validation
- Modular programming using multiple Python files

## Data Storage

Student records are stored locally in:

```text
students.txt
```

The application automatically creates the file if it does not already exist.

Because student records may contain personal information, `students.txt` should not be uploaded to a public repository.

## Limitations

The current version is a basic console-based enrollment system. It does not include:

- A graphical user interface
- A database management system
- User authentication
- Student record editing or deletion
- Advanced search functionality
- Duplicate student ID detection
- Encryption of stored information

## Future Improvements

Possible improvements for future versions include:

- Adding a graphical user interface
- Using a database for student records
- Adding search functionality
- Adding edit and delete features
- Adding duplicate student ID checking
- Improving data validation
- Adding user authentication
- Improving data security

## Project Purpose

This project was developed as a Python programming project to demonstrate fundamental programming concepts, modular code organization, input validation, and file handling for data persistence.

## License

This project is intended for educational purposes.

## Author

**Your Name**

**Your GitHub Profile**
