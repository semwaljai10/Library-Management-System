# **Library Management System**

A simple Library Management System to demonstrate **Object-Oriented Programming (OOP)** concepts in Java. The system allows users to manage a library of books by adding, borrowing, returning, and viewing them.

---

## **Overview of the Code**

The system is designed to manage a library's books efficiently. It involves three main components:

1. **`Book`**: Represents an individual book with details like title, author, and availability status.
2. **`Library`**: Manages a collection of books and provides operations such as adding, borrowing, and returning books.
3. **`LibraryManagementSystem` (LMS)**: The main class that serves as the interface for users to interact with the library.

---

## **Key OOP Concepts Used**

### **1. Classes and Objects**
- A **class** is a blueprint for creating objects.
- In this system:
  - **`Book`**: Represents individual books with attributes like `title`, `author`, and `isBorrowed`.
  - **`Library`**: Manages a collection of `Book` objects.
  - **`LMS`**: Simulates the system and interacts with the `Library` class.

---

### **2. Encapsulation**
Encapsulation restricts direct access to class fields and provides methods to access and modify them.

- **Example**:
  - In the `Book` class:
    - Fields (`title`, `author`, `isBorrowed`) are **private**.
    - Controlled access is provided via **public methods** like `getTitle()`, `borrowBook()`, and `returnBook()`.

---

### **3. Abstraction**
Abstraction hides complex implementation details while exposing only the essential features.

- **Example**:
  - The `Library` class abstracts operations like `addBook()`, `borrowBook()`, and `returnBook()`.
  - The `LMS` class interacts with `Library` through these methods without worrying about internal details.

---

### **4. Inheritance**
Inheritance allows one class to inherit properties and methods from another.

- **Not directly used in this project**, but it could be extended:
  - A `DigitalBook` class could inherit from `Book` and include additional attributes like `fileFormat`.

---

### **5. Polymorphism**
Polymorphism enables objects to be treated as instances of their parent class.

- **Not directly used**, but could be applied by overriding methods for different types of books (e.g., `DigitalBook`).

---

### **6. Object Arrays or Collections**
Collections are used to store and manage multiple objects dynamically.

- **Example**:
  - The `Library` class uses an `ArrayList<Book>` to manage all `Book` objects.

---

## **Detailed Explanation of the Classes**

### **1. Book Class**
- Represents a single book.
- **Fields**:
  - `title`, `author`: Store book details.
  - `isBorrowed`: Tracks whether the book is borrowed.
- **Methods**:
  - `borrowBook()`: Marks the book as borrowed.
  - `returnBook()`: Marks the book as returned.
  - `toString()`: Returns a string representation of the book.

---

### **2. Library Class**
- Manages a collection of books.
- **Fields**:
  - `books`: A list to store multiple `Book` objects.
- **Methods**:
  - `addBook(Book book)`: Adds a book to the collection.
  - `borrowBook(String title)`: Searches for and borrows a book by title.
  - `returnBook(String title)`: Searches for and returns a book by title.
  - `displayBooks()`: Displays details of all books.

---

### **3. LMS (Main Class)**
- Provides a command-line interface for the user to interact with the library.
- Uses the `Scanner` class to take user input and invoke methods in the `Library` class.

---

## **Workflow of the Program**

### **1. Initialization**
- A `Library` object is created in the `LMS` class's `main` method.
- Preloaded books are added using the `addBook()` method.

### **2. User Interaction**
- A menu is displayed with options:
  1. Display Books
  2. Add Book
  3. Borrow Book
  4. Return Book
  5. Exit
- Based on the user’s selection, the corresponding method in the `Library` class is invoked.

### **3. Example Execution**
- **Add Book**:  
  The user enters the book details. A new `Book` object is created and added to the library.
- **Borrow Book**:  
  The library searches for the book by title and marks it as borrowed.
- **Display Books**:  
  The library prints the details of all books, including their availability status.

---

## **Real-World OOP Concepts in This System**
1. **Encapsulation**: Protects fields and provides methods to modify/access them.
2. **Modularity**: Each class has a distinct responsibility, making the code manageable and extendable.
3. **Scalability**: The system can be enhanced with features like user management or late fees.
4. **Code Reusability**: The `Book` and `Library` classes can be reused in other inventory or library management projects.

---

## **Future Enhancements**
- **Inheritance**: Introduce subclasses like `DigitalBook` for different book types.
- **Persistence**: Save and load data from a file or database.
- **Polymorphism**: Use a parent class for various book types.

---
