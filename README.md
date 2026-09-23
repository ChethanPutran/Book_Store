# 📚 Book Store

A simple desktop-based **Book Store Management System** built with **Python, Tkinter, and SQLite**. The application provides a graphical interface for managing a collection of books with basic CRUD operations.

## ✨ Features

* 📖 **View All Books** — Display all books stored in the database.
* 🔍 **Search Books** — Search books using title, author, year, or ISBN.
* ➕ **Add Books** — Add new books to the collection.
* ✏️ **Update Books** — Modify the details of an existing book.
* 🗑️ **Delete Books** — Remove selected books from the database.
* 🖥️ **Desktop GUI** — Interactive graphical interface built using Tkinter.
* 💾 **Persistent Storage** — Book information is stored locally using SQLite.

## 🛠️ Tech Stack

| Technology  | Purpose                          |
| ----------- | -------------------------------- |
| **Python**  | Application development          |
| **Tkinter** | Desktop graphical user interface |
| **SQLite**  | Local database storage           |
| **sqlite3** | Python interface for SQLite      |

## 🏗️ Project Structure

```text
Book_Store/
│
├── frontend.py      # Tkinter-based graphical user interface
├── backend.py       # Database operations and CRUD logic
├── books.db         # SQLite database
├── __pycache__/     # Python generated cache files
└── README.md        # Project documentation
```

## 🧩 Architecture

The application follows a simple separation between the user interface and database layer:

```text
┌─────────────────────────┐
│       Tkinter GUI       │
│       frontend.py       │
└────────────┬────────────┘
             │
             │ Function Calls
             ▼
┌─────────────────────────┐
│    Database Layer       │
│       backend.py        │
└────────────┬────────────┘
             │
             │ SQL Queries
             ▼
┌─────────────────────────┐
│       SQLite DB         │
│        books.db         │
└─────────────────────────┘
```

### Frontend

`frontend.py` is responsible for:

* Creating the Tkinter application window.
* Providing input fields for:

  * Title
  * Author
  * Year
  * ISBN
* Displaying database records in a list.
* Handling user interactions.
* Calling backend functions for database operations.

### Backend

`backend.py` handles the SQLite database and provides functions for:

* Creating the database table.
* Inserting books.
* Retrieving books.
* Searching books.
* Updating books.
* Deleting books.

The database table is created automatically if it does not already exist.

## 🗄️ Database Schema

The application uses a SQLite database named `books.db`.

### `book` Table

| Column   | Type    | Description      |
| -------- | ------- | ---------------- |
| `id`     | INTEGER | Primary key      |
| `title`  | TEXT    | Book title       |
| `author` | TEXT    | Book author      |
| `year`   | INTEGER | Publication year |
| `isbn`   | INTEGER | ISBN number      |

## 🚀 Getting Started

### Prerequisites

Make sure Python 3 is installed on your system.

Check your Python installation:

```bash
python --version
```

Tkinter and SQLite are part of the standard Python ecosystem on most desktop Python installations.

### Clone the Repository

```bash
git clone https://github.com/ChethanPutran/Book_Store.git
cd Book_Store
```

### Run the Application

Start the application using:

```bash
python frontend.py
```

The Tkinter desktop application will open.

The backend automatically initializes the SQLite database and creates the `book` table if it does not already exist.

## 📖 Using the Application

### Add a Book

1. Enter the book title.
2. Enter the author's name.
3. Enter the publication year.
4. Enter the ISBN.
5. Click **Add Entry**.

### View Books

Click **View All** to display all books currently stored in the database.

### Search

Enter one or more search values and click **Search Entry**.

The application searches using the provided:

* Title
* Author
* Year
* ISBN

### Update a Book

1. Select a book from the list.
2. Its details will be loaded into the input fields.
3. Modify the required information.
4. Click **Update Selected**.

### Delete a Book

1. Select a book from the list.
2. Click **Delete Selected**.

### Close

Click **Close** to exit the application.

## 🔄 CRUD Operations

The project demonstrates the fundamental database CRUD operations:

```text
Create  → Add a new book
Read    → View and search books
Update  → Modify book information
Delete  → Remove a book
```

These operations are implemented in `backend.py` and triggered through the Tkinter interface.

## 🎯 Learning Objectives

This project demonstrates practical concepts including:

* Python GUI development with Tkinter
* SQLite database integration
* CRUD operations
* SQL queries from Python
* Separation of frontend and backend logic
* Event-driven programming
* Local data persistence

## 🔮 Possible Improvements

Potential future enhancements include:

* Input validation for year and ISBN.
* Improved error handling.
* Better search functionality with partial matches.
* Sorting books by title, author, or year.
* Confirmation dialogs before deletion.
* Improved GUI styling and layout.
* Separate database configuration.
* ISBN stored as text to support ISBN-13 and leading zeros.
* Unit tests for database operations.
* Packaging the application as a standalone executable.
