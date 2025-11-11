# Library Management System

## Project Overview
This project implements a **Library Management System** in Python, demonstrating both **procedural** and **object-oriented programming (OOP)** approaches.
It allows you to:
- Add and manage books and members
- Borrow and return books
- Track borrowed books and available copies
- Handle edge cases like borrowing limits, unavailable books, and invalid operations

---

## Project Structure
```
library-management-oop/
│
├── README.md                        # This file
│
├── procedural_version/
│   ├── library_procedural.py        # Original procedural code
│   └── test_procedural.py           # Comprehensive test suite for procedural version
│
└── oop_solution/
    ├── library_oop.py               # OOP implementation
    └── test_oop.py                  # Comprehensive test suite for OOP version
```

---

## Design Overview

### Procedural Version
- Functions and global lists manage books, members, and borrowed books.
- Key functions include:
  - `add_book()`, `add_member()`
  - `borrow_book()`, `return_book()`
  - `display_available_books()`, `display_member_books()`

---

### OOP Version

#### Classes

**1. `Book`**
- Represents a book.
- Attributes:
  - `id`, `title`, `author`, `available_copies`
- Methods: `__init__`

**2. `Member`**
- Represents a library member.
- Attributes:
  - `id`, `name`, `email`, `borrowed_books`
- Methods: `__init__`

**3. `Library`**
- Manages the system.
- Attributes:
  - `books`, `members`, `borrowed_books`
- Key Methods:
  - `add_book(book_id, title, author, available_copies)`
  - `add_member(member_id, name, email)`
  - `find_book(book_id)`, `find_member(member_id)`
  - `borrow_book(member_id, book_id)`, `return_book(member_id, book_id)`
  - `display_available_books()`, `display_member_books(member_id)`

---

## Testing

### Test Coverage

**Procedural Version:** `procedural_version/test_procedural.py`  
**OOP Version:** `oop_solution/test_oop.py`  

Both test suites cover:

#### Basic Operations
- Adding books and members
- Borrowing and returning books
- Displaying available books and member's borrowed books

#### Edge Cases
- Borrowing unavailable books
- Exceeding borrowing limit (3 books max per member)
- Returning books not borrowed
- Non-existent members or books

---

### How to Run Tests

1. Open a terminal in the project folder.
2. Run tests in your terminal by:
```bash
# Run procedural tests
python procedural_version/test_procedural.py

# Run OOP tests
python oop_solution/test_oop.py
```