# Campus Course & Records Manager (CCRM)

### Project Overview

The **Campus Course & Records Manager (CCRM)** is a console-based Java application designed to manage students, courses, enrollments, and grades for an educational institute. This project demonstrates core and advanced Java concepts, including a robust object-oriented design, modern I/O with NIO.2, the Stream API, and various design patterns.

The application features a menu-driven command-line interface (CLI) that allows a user to perform all administrative tasks, from adding a new student to generating a full academic transcript.

### How to Run

1.  **Prerequisites:** Ensure you have the **Java Development Kit (JDK)** version 8 or higher installed. You can verify your installation by running `java -version` in your terminal.
2.  **Clone the Repository:**
    ```bash
    git clone [Your-Repository-URL]
    ```
3.  **Navigate to the Project Directory:**
    ```bash
    cd CCRM
    ```
4.  **Compile and Run:**
      * **Using a Command Line:**
        ```bash
        # Compile all Java files
        javac -d bin -sourcepath src src/edu/ccrm/cli/Main.java

        # Enable assertions and run the application
        java -ea -cp bin edu.ccrm.cli.Main
        ```
      * **Using an IDE (e.g., Eclipse):**
          * Open the project in your IDE.
          * Right-click the `Main.java` file in the `edu.ccrm.cli` package.
          * Select `Run As > Java Application`.
          * To enable assertions in Eclipse, go to `Run > Run Configurations...`. Under the `Arguments` tab, add `-ea` to the `VM arguments` field.

-----

### Java Ecosystem & Architecture

#### Evolution of Java

  * **1995:** Java is introduced by Sun Microsystems as a programming language and computing platform.
  * **1997:** Java 1.1 introduces inner classes, a more robust event model, and JDBC.
  * **2004:** Java 5.0 (codename Tiger) marks a significant leap, introducing generics, enhanced `for` loops, autoboxing, and enums.
  * **2014:** Java 8 is released, introducing the biggest changes since Java 5. It includes **lambda expressions**, the **Stream API**, and the modern **Date/Time API (java.time)**.
  * **2017-Present:** With a new six-month release cycle, new versions introduce smaller, more focused features (e.g., modules, text blocks, sealed classes).

#### Java ME vs. Java SE vs. Java EE

| Feature | **Java SE (Standard Edition)** | **Java ME (Micro Edition)** | **Java EE (Enterprise Edition)** |
| :--- | :--- | :--- | :--- |
| **Purpose** | General-purpose programming. | Small, embedded devices (legacy). | Large-scale, distributed enterprise apps. |
| **Platform** | Desktops, servers, laptops. | Mobile phones, IoT devices. | Web servers, application servers. |
| **Key APIs** | Core libraries (JFC, JDBC, RMI). | Limited APIs, specific to devices. | Comprehensive APIs (Servlets, JSF, EJB). |
| **Typical Use**| Standalone applications, CLI tools. | Legacy mobile apps (J2ME). | Web services, e-commerce, banking systems. |

#### JDK, JRE, and JVM

  * **Java Development Kit (JDK):** A software development environment used for developing Java applications. It includes the JRE, a compiler (`javac`), and other tools.
  * **Java Runtime Environment (JRE):** The environment required to run Java applications. It includes the JVM and the Java class libraries.
  * **Java Virtual Machine (JVM):** The core component that executes Java bytecode. It provides a platform-independent environment, allowing code to run on any machine with a JRE.

**Interaction:** A developer uses the **JDK** to write and compile Java source code (`.java`) into platform-agnostic bytecode (`.class`). The end user, who only has the **JRE**, can then run this bytecode. The **JVM** inside the JRE interprets and executes the bytecode on their specific operating system.

-----

### Windows & Eclipse Setup Guide

This section contains screenshots of the setup process.

1.  **JDK Installation Verification:** (Screenshot of `java -version` command output)
2.  **Eclipse Project Setup:** (Screenshot of the "New Java Project" wizard in Eclipse)
3.  **Eclipse Run Configuration:** (Screenshot showing the Run Configurations window)
4.  **Program Execution:** (Screenshot of the CCRM menu and a sample operation in the console)
5.  **Backup Folder Structure:** (Screenshot showing a timestamped backup folder with exported files)

-----

### Syllabus Topic Mapping

This table provides a cross-reference between the project requirements and where they are implemented in the source code.

| Topic | Location (File/Class/Method) |
| :--- | :--- |
| **OOP Pillars** | `edu.ccrm.domain/` classes (`Person`, `Student`, `Course`). |
| **Inheritance (`super`)** | `Student` & `Instructor` constructors calling `super()`. |
| **Abstraction** | `edu.ccrm.domain/Person.java` (abstract class and methods). |
| **Polymorphism** | `edu.ccrm.service/TranscriptService.java` (invoking `toString()` on `Person` objects). |
| **Encapsulation** | Private fields and public getters/setters across all domain classes. |
| **NIO.2 (Path, Files)** | `edu.ccrm.io/ImportExportService.java`, `edu.ccrm.io/BackupService.java`. |
| **Stream API** | `edu.ccrm.service/CourseService.java` (search/filter methods). |
| **Date/Time API** | `edu.ccrm.domain/Student.java`, `edu.ccrm.io/BackupService.java`. |
| **Singleton Pattern** | `edu.ccrm.config/AppConfig.java`. |
| **Builder Pattern** | `edu.ccrm.domain/Course.java` (static nested class `Course.Builder`). |
| **Custom Exceptions** | `edu.ccrm.exceptions/` package (`MaxCreditLimitExceededException`, `DuplicateEnrollmentException`). |
| **Recursion** | `edu.ccrm.io/BackupService.java` (to compute directory size). |
| **Enums with Fields** | `edu.ccrm.domain/Grade.java` and `Semester.java`. |
| **Lambdas & Func. Interfaces** | `edu.ccrm.util/Comparators.java` or `edu.ccrm.cli/Main.java`. |
| **Assertions (`-ea`)** | `edu.ccrm.domain/Course.java` (in the constructor). |

