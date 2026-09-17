# SHS Enrollment System

A simple **Senior High School (SHS) Enrollment System** developed using Python. This console-based application allows users to enroll students, validate student information, select an SHS track and strand, save enrollment records, and view enrolled students.

## 📌 Project Description

The **SHS Enrollment System** is a console-based Python application designed to manage basic student enrollment information.

The system provides a menu-driven interface that allows users to:

- Enroll a student
- Enter student information
- Validate required information
- Select an SHS track and strand
- Save student records using file handling
- Load previously saved student records
- View enrolled students
- Exit the application

The project demonstrates fundamental Python programming concepts and the use of **file handling for data persistence**.

---

## ✨ Features

### 1. Student Enrollment

The system collects the following information:

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
- Guardian

After the required information is entered and validated, the student record is saved to the system.

### 2. Input Validation

The system performs basic input validation to help prevent invalid or incomplete information.

Validation includes:

- Student ID cannot be empty
- First name cannot be empty
- Last name cannot be empty
- Age must be a valid number greater than zero
- Gender must be Male or Female
- Grade level must be Grade 11 or Grade 12
- Contact number must contain numbers only
- Address cannot be empty
- Guardian cannot be empty

### 3. Track and Strand Selection

The system provides two available Senior High School tracks.

#### Academic

- STEM
- ABM
- HUMSS
- GAS

#### TVL

- ICT - Programming
- ICT - CSS

Users first select a track and then select the corresponding strand.

### 4. File Handling and Data Persistence

The system uses a text file named:

```text
students.txt
```

Student records are saved to this file using file handling.

When the program starts, previously saved student records are loaded from `students.txt`. If the file does not exist, the system automatically creates it.

This allows student records to remain available even after the program has been closed.

### 5. View Enrolled Students

The system allows users to view all enrolled student records.

The displayed information includes:

- Student ID
- Name
- Age
- Gender
- Grade Level
- Track
- Strand
- Contact
- Address
- Guardian

If there are no enrolled students, the system displays:

```text
No students enrolled.
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Python Functions | Organize program operations |
| Lists | Store student records during program execution |
| Dictionaries | Store individual student information |
| Conditional Statements | Process choices and validation |
| Loops | Repeatedly request user input |
| Exception Handling | Handle input and file-related errors |
| File Handling | Save and load student records |
| Text File | Persistent data storage |
| Console Interface | User interaction |

---

## 📂 Project Structure

The project consists of two Python files:

```text
SHSEnrollmentFormV1/
│
├── main.py
├── enrollment.py
└── README.md
```

The application also uses:

```text
students.txt
```

The `students.txt` file is created automatically by the program if it does not already exist.

### `main.py`

`main.py` serves as the main entry point of the application.

It displays the main menu and allows the user to choose between:

1. Enroll Student
2. View Enrolled Students
3. Exit

The selected option calls the appropriate function from `enrollment.py`.

### `enrollment.py`

`enrollment.py` contains the main functionality of the enrollment system.

It handles:

- Loading student records
- Saving student records
- Adding students
- Selecting tracks and strands
- Validating student information
- Viewing enrolled students

---

## ⚙️ Requirements

To run the project, you need:

- Python 3.x
- A terminal or command prompt
- The project files in the same directory

No external Python packages are required.

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the Project Folder

```bash
cd SHSEnrollmentFormV1
```

### 3. Run the Program

```bash
python main.py
```

If your system uses `python3`, use:

```bash
python3 main.py
```

---

## 🖥️ Main Menu

When the program starts, the following menu is displayed:

```text
==============================
     SHS ENROLLMENT SYSTEM
==============================
1. Enroll Student
2. View Enrolled Students
3. Exit
```

### Menu Options

| Option | Function |
|---|---|
| 1 | Enroll a new student |
| 2 | View enrolled students |
| 3 | Exit the application |

---

## 📝 Enrollment Process

To enroll a student, select:

```text
1. Enroll Student
```

The system will ask for the student's information.

Example:

```text
===== STUDENT ENROLLMENT =====

Student ID: 2026-001
First Name: Juan
Middle Name: Dela
Last Name: Cruz
Age: 17
Gender: Male
Grade Level (11/12): 11
```

The system then asks the user to select a track:

```text
===== TRACK =====
1. Academic
2. TVL

Choose track:
```

If Academic is selected:

```text
===== ACADEMIC STRANDS =====
1. STEM
2. ABM
3. HUMSS
4. GAS

Choose strand:
```

If TVL is selected:

```text
===== TVL STRANDS =====
1. ICT - Programming
2. ICT - CSS

Choose strand:
```

After all required information is successfully entered and validated, the system displays:

```text
Student enrolled successfully!
```

The student record is then saved to `students.txt`.

---

## 💾 Data Storage

Student information is stored in `students.txt`.

Each student record uses a pipe (`|`) as a separator between fields.

The format is:

```text
Student ID|First Name|Middle Name|Last Name|Age|Gender|Grade Level|Track|Strand|Contact|Address|Guardian
```

Example:

```text
2026-001|Juan|Dela|Cruz|17|Male|Grade 11|Academic|STEM|09123456789|Sample Address|Maria Dela Cruz
```

When the application starts, the records in `students.txt` are loaded into the program.

When a new student is enrolled, the new record is added to the file.

---

## 🔄 System Flow

```text
                    START
                      │
                      ▼
             Load Student Records
              from students.txt
                      │
                      ▼
                 Main Menu
                      │
          ┌───────────┼───────────┐
          │           │           │
          ▼           ▼           ▼
       Enroll       View         Exit
       Student     Students
          │           │           │
          ▼           ▼           ▼
    Enter Student   Display      END
     Information    Records
          │
          ▼
    Validate Input
          │
          ▼
    Select Track
     and Strand
          │
          ▼
     Save Record
          │
          ▼
      Main Menu
```

---

## 🧩 Program Functions

### `load_students()`

Loads previously saved student records from `students.txt`.

### `save_student(student)`

Saves a newly enrolled student record to `students.txt`.

### `add_student()`

Handles the student enrollment process and collects the required student information.

### `choose_strand()`

Allows the user to select an SHS track and its corresponding strand.

### `validate_student(student)`

Checks the required student information before the record is accepted.

### `view_students()`

Displays the student records currently loaded in the system.

---

## 📚 Python Concepts Demonstrated

This project demonstrates the following Python programming concepts:

- Variables
- Functions
- Lists
- Dictionaries
- Conditional statements
- `while` loops
- User input
- String manipulation
- Input validation
- Exception handling
- File handling
- Data persistence
- Modular programming

---

## 🔐 Privacy and Security Notice

This project stores student information in a plain-text file.

Because this repository is **public on GitHub**, do not upload real student information to the repository.

Do not use real:

- Student names
- Contact numbers
- Addresses
- Guardian information
- Other personally identifiable information

For testing and demonstrations, use fictional data.

Example:

```text
2026-001|Juan|Dela|Cruz|17|Male|Grade 11|Academic|STEM|09123456789|Sample Address|Maria Dela Cruz
```

---

## ⚠️ Current Limitations

The current version of the system is a basic console-based enrollment application.

It currently does not include:

- Graphical User Interface (GUI)
- Database storage
- Student search functionality
- Student record editing
- Student record deletion
- User authentication
- Automatic Student ID generation
- Duplicate Student ID detection

---

## 🔮 Future Improvements

Possible improvements for future versions include:

- Add a graphical user interface
- Add student search functionality
- Add edit and delete functionality
- Add duplicate Student ID checking
- Implement database storage such as SQLite
- Add administrator authentication
- Improve input validation
- Generate enrollment reports
- Add data export functionality

---

## 🎯 Project Purpose

The purpose of this project is to apply fundamental Python programming concepts to a practical student enrollment scenario.

The project demonstrates how functions, data structures, input validation, exception handling, modular programming, and file handling can be combined to create a functional console-based application.

---

## 📄 License

This project is intended for educational purposes.

---

## 👤 Author

**Your Name**

Senior High School Enrollment System

GitHub: **Your GitHub Profile**
