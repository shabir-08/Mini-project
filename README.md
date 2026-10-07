Smart Student Ranking & Search System

Overview

Smart Student Ranking & Search System is a menu-driven C program for managing student records while demonstrating important Data Structures and Algorithms concepts.

The system stores student information such as:

- Roll Number
- Student Name
- Marks

It provides functionality to add and display students, generate a rank list, compare sorting algorithms, and search for students using Binary Search.

---

Features

1. Add Students

Allows the user to add multiple student records.

Each record contains:

- Roll Number
- Name
- Marks

The system supports a maximum of 100 students.

2. Display All Students

Displays all currently stored student records in a formatted table.

Example:

Roll No    Name                 Marks
------------------------------------------
101        Rahul                85.50
102        Priya                92.00
103        Amit                 78.50

3. Generate Rank List

Generates a ranking of students based on their marks in descending order.

The highest-scoring student is displayed as the Topper.

Two sorting algorithms are implemented:

- Selection Sort
- Insertion Sort

The program also compares their operation counts.

4. Algorithm Performance Analysis

The program counts:

Selection Sort

- Number of comparisons
- Number of swaps

Insertion Sort

- Number of comparisons
- Number of shifts

This allows users to observe how different sorting algorithms behave on the same student dataset.

5. Search Student by Roll Number

The program uses Binary Search to find a student by their roll number.

Before performing Binary Search, the student records are sorted in ascending order of roll number.

The program also displays the number of steps required to find the student.

6. Exit

Terminates the program safely.

---

Algorithms Used

Selection Sort

Students are sorted by marks in descending order.

At every iteration, the student with the highest remaining marks is selected and placed at the correct position.

Time Complexity:

- Best Case: "O(n²)"
- Average Case: "O(n²)"
- Worst Case: "O(n²)"

Space Complexity:

"O(1)" auxiliary space apart from the input array.

---

Insertion Sort

Students are sorted by marks in descending order by inserting each student into its correct position among the previously sorted students.

Time Complexity:

- Best Case: "O(n)"
- Average Case: "O(n²)"
- Worst Case: "O(n²)"

Space Complexity:

"O(1)" auxiliary space apart from the input array.

---

Binary Search

Binary Search is used to find a student using their roll number.

The records must first be sorted by roll number.

Time Complexity:

- Best Case: "O(1)"
- Average Case: "O(log n)"
- Worst Case: "O(log n)"

Space Complexity:

"O(1)"

---

 Data Structure

The project uses a C "struct" to represent each student.

typedef struct {
    int roll;
    char name[50];
    float marks;
} Student;

An array of "Student" structures is used to store the records:

Student students[MAX_STUDENTS];

The maximum number of students is:

100

---

 Menu

When the program starts, the following menu is displayed:

=== Smart Student Ranking & Search System ===
1. Add Students
2. Display All Students
3. Generate Rank List & Compare Algorithms
4. Search Student by Roll No
5. Exit
Enter choice:

---

Sample Input

Enter choice: 1
How many students to add? 3

Student 1 details:
Roll No: 101
Name: Rahul
Marks: 85

Student 2 details:
Roll No: 102
Name: Priya
Marks: 95

Student 3 details:
Roll No: 103
Name: Amit
Marks: 78

---

Sample Ranking Output

--- Rank List (Descending by Marks) ---

Roll No    Name                 Marks
------------------------------------------
102        Priya                95.00
101        Rahul                85.00
103        Amit                 78.00

--- Topper Details ---
Name: Priya | Marks: 95.00

Example algorithm analysis:

--- Algorithm Performance Analysis ---
Selection Sort : 3 comparisons, 1 swaps.
Insertion Sort : 3 comparisons, 3 shifts.

The exact operation counts depend on the input data.

---

Sample Search

Enter Roll Number to search: 101

Records have been sorted by Roll Number for Binary Search.

Student Found! (in 2 steps)
Roll: 101 | Name: Rahul | Marks: 85.00

If the roll number does not exist:

Record 'Not Found' for Roll Number 110.

---

 Project Structure

Smart-Student-Ranking-System/
│
├── main.c
└── README.md

---

 Technologies Used

- Language: C
- Concepts: Structures, Arrays, Functions, Sorting, Searching
- Algorithms:
  - Selection Sort
  - Insertion Sort
  - Binary Search
- Libraries:
  - "stdio.h"
  - "stdlib.h"
  - "string.h"

---

Learning Objectives

This project demonstrates:

1. Using structures to store records.
2. Managing multiple records using arrays.
3. Implementing Selection Sort.
4. Implementing Insertion Sort.
5. Implementing Binary Search.
6. Comparing sorting algorithms using operation counts.
7. Using functions for modular programming.
8. Working with strings using "fgets()" and "strcspn()".
9. Using "memcpy()" to create copies of data for algorithm comparison.
10. Understanding basic time complexity of algorithms.

---

 How to Compile and Run

Using GCC

Compile:

gcc main.c -o student_system

Run:

./student_system

Windows

gcc main.c -o student_system.exe
student_system.exe

---

Limitations

- Maximum of 100 students can be stored.
- Student data is stored only during program execution.
- Data is lost when the program exits.
- Roll numbers are assumed to be suitable for identifying students.
- Binary Search requires the records to be sorted by roll number.

---

Future Improvements

The project can be extended by adding:

- File handling to permanently save student records.
- Update and delete student functionality.
- Search by student name.
- Sorting by roll number or name.
- Grade calculation.
- Percentage calculation.
- Multiple subject marks.
- Student attendance tracking.
- More sorting algorithms such as Merge Sort and Quick Sort.
- Graphical User Interface (GUI).

---

👨‍💻 Conclusion

The Smart Student Ranking & Search System combines student record management with fundamental DSA algorithms. It demonstrates how sorting and searching techniques can be applied to a practical problem while also allowing comparison of algorithmic operations.

The project is particularly useful for understanding the practical implementation and complexity of Selection Sort, Insertion Sort, and Binary Search in C.
