# Advanced Ticket Management System Lab

## Overview

Building on your completed Ticket Management System, you will now extend the application by integrating additional features and best practices commonly used in real-world Java development. This lab focuses on applying advanced design patterns, improving debugging and file operations, enhancing the code with modern language constructs, and incorporating external data and robust concurrency mechanisms.

---

## Features to Implement

### 1. **Robust Service Architecture**

- **Singleton Pattern:**  
  Refactor your service class (e.g., `TicketService`) to ensure only one instance exists throughout the application. This centralizes ticket management and resource access.

- **Factory Pattern:**  
  Create a factory (e.g., `UserFactory` or `TicketFactory`) that instantiates different objects based on input parameters. For example, your factory can generate either an admin or regular user, or even different types of tickets based on urgency.

- **Builder Pattern:**  
  Develop a fluent builder for the `Ticket` class. This builder should allow the optional setting of attributes like an assigned user or extra metadata while maintaining immutability where possible.

### 2. **Enhanced Debugging and Logging**

- **IDE Debugging:**  
  Use breakpoints to step through critical parts of your code. Set up **conditional breakpoints** (e.g., stop execution when a ticket’s priority is HIGH) to isolate issues during runtime.

- **Logging:**  
  Integrate a logging framework (or Java’s built-in logging) to record significant events. Replace print statements with logs that capture information at different levels (INFO, DEBUG, ERROR).

- **Mockito for Testing:**  
  Refine your JUnit tests by using Mockito to simulate parts of your system. For instance, mock external API calls or service dependencies to ensure your tests remain focused on logic rather than external factors.

### 3. **File I/O and Data Persistence**

- **Buffered I/O:**  
  Add a feature to persist your ticket data to a file. Use `BufferedWriter` to write ticket summaries or details to a file, and `BufferedReader` to read from it when your application starts. This ensures your system can recover state after a shutdown.

### 4. **Modern Java Language Features**

- **Anonymous Classes:**  
  Use an anonymous class to implement a custom comparator or event listener in a concise way, rather than creating a named class.

- **Varargs and var Keyword:**  
  Implement a utility method that accepts a variable number of ticket IDs (varargs) to generate a formatted report of selected tickets. Also, use the `var` keyword for local variable type inference where applicable to simplify your code.

- **String Formatting:**  
  Utilize `String.format()` to generate neatly formatted output for reports or log messages (for example, a summary display of ticket statuses).

- **Record Classes and Enums:**  
  Introduce a record class (e.g., `TicketSummary`) to hold immutable, lightweight ticket information. Enhance your use of enums by adding new categories or states that further define your domain model.

### 5. **External API Integration**

- **API Communication:**  
  Integrate a feature that communicates with an external API. For example, simulate retrieving external data (such as service status updates or weather information that might affect ticket priorities) using HTTP calls. Ensure you handle responses and potential errors gracefully.

### 6. **Advanced Data Structures and Concurrency**

- **Custom Algorithms:**  
  Implement an efficient search or sorting algorithm (or use a non-standard data structure) to improve ticket lookup and management, showing your understanding of underlying data structure concepts.

- **Advanced Locks:**  
  Enhance thread-safety by incorporating advanced locking mechanisms (e.g., using `ReentrantLock`) to control access to shared resources, particularly when your application performs file I/O or updates tickets concurrently.

---

## Deliverables

1. **Updated Maven Project:**  
   Submit your enhanced Maven project including all new features and modifications.

2. **Source Code Documentation:**  
   Ensure your code is well commented, and include a brief write-up that explains how each advanced feature was integrated. Highlight how design patterns, modern syntax, and concurrency enhancements have improved your system.

3. **JUnit and Mockito Tests:**  
   Provide an updated test suite demonstrating:
   - Behavior validation of your service classes.
   - Mocked API calls and simulated service behaviors using Mockito.
   - Edge cases for file I/O operations and concurrency.

4. **Demonstration:**  
   Prepare a short video or live demonstration that:
   - Shows your debugging process using breakpoints and conditional breakpoints.
   - Walks through a feature such as saving/loading data from a file or communicating with an external API.
   - Demonstrates thread-safe operations under concurrent access.

---

## Bonus Challenge

- **Algorithmic Recommendation:**  
  Develop a feature that analyzes historical ticket data (using advanced data structures or algorithms) to recommend optimal ticket assignments or prioritizations.
  
- **Enhanced Logging:**  
  Implement log rotation or a more sophisticated logging configuration using an external library (e.g., Log4j) to further professionalize your application’s logging capabilities.
