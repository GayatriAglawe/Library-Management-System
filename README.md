📚 Library Management System — Theory & Explanation
🔍 Introduction

The Library Management System is a simple Python-based console application designed to handle basic operations in a library such as adding, viewing, searching, issuing, and returning books. It helps in maintaining an organized list of available books, tracking issued books, and managing return deadlines and fines.

This system uses lists, dictionaries, and functions to manage book records dynamically, making it easy to store and retrieve data without using external databases.

🎯 Objective

The main aim of this project is to:

Manage books and their details efficiently.

Keep track of issued and returned books.

Calculate fines for late returns.

Provide a user-friendly interface for performing library operations.

🧠 Theoretical Concepts Used
1. Data Structures

The program uses a list (library) to store all book records.

Each book is represented as a dictionary with keys such as:

title, author, year, copies, issue_date, return_date, and status.

Example book record:

{
    "title": "The Great Gatsby",
    "author": "F. Scott Fitzgerald",
    "year": "1925",
    "copies": 3,
    "issue_date": "",
    "return_date": "",
    "status": "Available"
}

2. Functions

The program is modular, with separate functions for each operation:

add_book() → Adds a new book record to the library.

display_books() → Displays all books currently in the library.

search_book() → Finds a specific book by title.

delete_book() → Removes a book record from the list.

issue_book() → Issues a book and records issue and return dates.

return_book() → Returns a book and checks for late submission.

main() → Provides a menu-driven interface for user interaction.

3. Conditional Logic

The if, elif, and else statements are used extensively to:

Validate user input.

Determine whether a book is available or out of stock.

Handle incorrect user choices gracefully.

4. Exception Handling

The program uses try–except blocks to manage errors (e.g., entering non-numeric values for number of copies).

5. Date and Time Operations

The datetime module is used to record the issue date and calculate the return date (7 days later).

Late return fines are calculated based on the difference between the actual return date and the expected return date.

6. Loops

The program uses a while True loop in the main() function to continuously display the menu until the user chooses to exit.

for loops are used to iterate through the library list when searching or deleting books.

⚙️ Functional Overview
➕ 1. Add Book

Takes book details from the user.

Automatically sets the book’s status to:

"Available" if copies > 0

"Out of Stock" if copies = 0

Appends the book record to the library list.

📋 2. Display Books

Lists all books stored in the library with their details such as title, author, year, copies, and status.

🔎 3. Search Book

Prompts for a book title and searches the library list.

Displays book information if found; otherwise prints “Book not found.”

❌ 4. Delete Book

Allows the user to remove a book record permanently by entering the book title.

📖 5. Issue Book

Reduces the number of copies by one when a book is issued.

Records:

Issue date (current date)

Return date (7 days from issue)

Updates book status based on remaining copies.

📥 6. Return Book

Increases the book’s copy count by one.

Clears issue and return dates.

Calculates fine if the book is returned late (₹10 per day late).

🚪 7. Exit

Terminates the program gracefully with a thank-you message.

📅 Fine Calculation Logic

When a book is returned, the system:

Reads the stored return_date from the book record.

Compares it with the current date.

Calculates the difference in days:

If late_days > 0, fine = late_days * 10.

Otherwise, no fine is charged.

⚡ Limitations

Data is stored only in memory (not saved permanently).

No user authentication (anyone can access all features).

Search uses only title; cannot search by author or year.

Input validation is limited to basic checks.

🚀 Possible Improvements

Save library data in a text file or database for persistence.

Add login system for admin and members.

Implement book categories and unique book IDs.

Create a graphical user interface (GUI) using Tkinter or PyQt.

🧾 Conclusion

This project demonstrates fundamental Python programming concepts such as data structures, functions, conditional statements, loops, and file handling concepts (if extended). It provides a clear understanding of how a real-world library system can be modeled and managed through simple logic and structured programming.
