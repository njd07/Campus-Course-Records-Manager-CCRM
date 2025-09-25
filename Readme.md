<h1 align="center">Campus Course & Records Manager (CCRM)</h1>

<p align="center">
A comprehensive, console-based Java application designed to manage student and course records for an educational institution. This project is built with pure Java SE, focusing on core language features and Object-Oriented principles.
</p>

<p align="center">
<a href="https://github.com/njd07/Campus-Course-Records-Manager-CCRM">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Java-11%252B-blue.svg" alt="Java Version">
</a>
<a href="https://www.google.com/search?q=https://github.com/njd07/Campus-Course-Records-Manager-CCRM/issues">
<img src="https://www.google.com/search?q=https://img.shields.io/github/issues/njd07/Campus-Course-Records-Manager-CCRM" alt="Issues">
</a>
<a href="https://www.google.com/search?q=https://github.com/njd07/Campus-Course-Records-Manager-CCRM/stargazers">
<img src="https://www.google.com/search?q=https://img.shields.io/github/stars/njd07/Campus-Course-Records-Manager-CCRM" alt="Stars">
</a>
</p>
📋 Table of Contents

    Key Features

    Project Structure

    Requirements

    How to Build and Run

    Setup Guide for Windows

    Core Java Concepts Demonstrated

    Screenshots

✨ Key Features

    Student Management: Add new students and list all students currently in the system.

    Course Management: View a comprehensive list of all available courses.

    Enrollment System: Enroll students in courses with built-in validation for duplicates and credit limits.

    Grading & Transcripts: Record student marks, which are automatically converted to letter grades, and view a full student transcript with a calculated GPA.

    Data Persistence: Export the current student and course data to organized CSV files.

    Backup Utility: Create timestamped backups of all exported data for archival purposes.

📂 Project Structure

The project follows a clean, package-by-feature architecture to ensure a clear separation of concerns, making the codebase modular and easy to maintain.

Campus-Course-Records-Manager-CCRM/
├── .gitignore
├── README.md
├── USAGE.md
├── screenshots/
│   ├── file_struct.png
│   ├── java_version_check.png
│   ├── menu.png
│   └── menu_test.png
├── proj_data/
│   ├── courses_sample.csv
│   └── students_sample.csv
└── src/
└── edu/
└── ccrm/
├── CrmApp.java             # Main application entry point
├── config/                 # Singleton configuration
├── model/                  # Data classes (POJOs)
├── service/                # Business logic
└── util/                   # Utility classes (I/O, Exceptions)

🔧 Requirements

    Java Development Kit (JDK): Version 11 or newer is recommended.

    IDE: Any modern Java IDE such as IntelliJ IDEA or Eclipse.

🚀 How to Build and Run

This project is designed to be run directly from a Java IDE, which is the simplest and most effective method.

    Clone the Repository

    git clone [https://github.com/njd07/Campus-Course-Records-Manager-CCRM.git](https://github.com/njd07/Campus-Course-Records-Manager-CCRM.git)

    Open the Project in your IDE

        Launch IntelliJ IDEA or Eclipse.

        Select File > Open... (or Import Project...).

        Navigate to the cloned Campus-Course-Records-Manager-CCRM directory and select it. The IDE will automatically detect the project structure.

    Run the Application

        In the project explorer, navigate to the main application file located at src/edu/ccrm/CrmApp.java.

        Right-click on the CrmApp.java file.

        Select "Run 'CrmApp.main()'" from the context menu.

        The application will compile and start, displaying the main menu in the IDE's console.

💻 Setup Guide for Windows

This guide provides the essential steps for configuring a Java development environment on a Windows machine.
1. Install the Java Development Kit (JDK)

   Download a recent JDK version (e.g., Java 17 LTS) from a trusted source like Oracle or Adoptium.

   Execute the installer and follow the on-screen prompts to complete the installation.

2. Configure System Environment Variables

   Use the Windows Search bar to find and open "Edit the system environment variables".

   In the System Properties window, click the Environment Variables... button.

   Under the "System variables" section, click New... to create a new variable:

        Variable name: JAVA_HOME

        Variable value: C:\Program Files\Java\jdk-17 (This path must match your specific JDK installation directory).

   Locate the Path variable in the "System variables" list, select it, and click Edit....

   Click New and add a new entry that points to the JDK's bin directory: %JAVA_HOME%\bin

3. Verify the Installation

   Open a new Command Prompt or PowerShell window.

   Execute the following commands. Each should return the version of the installed Java components.

   java -version
   javac -version

📘 Core Java Concepts Demonstrated

This project was built to demonstrate a wide range of core Java SE features as required by the course syllabus.
A. Java Platform Explanations
Evolution of Java

    1995 (Java 1.0): The initial public release from Sun Microsystems, introducing the "Write Once, Run Anywhere" philosophy.

    2004 (Java 5): A pivotal update that added modern language essentials like Generics, Enums, and Annotations.

    2014 (Java 8): A landmark release that brought functional programming to Java with Lambda Expressions and the Stream API.

    2018 (Java 11): The first Long-Term Support (LTS) version under the new, faster six-month release cycle.

    2021 (Java 17): The next major LTS release, which continues to add performance improvements and modern language features.

Java SE vs. ME vs. EE

Platform


Target Audience


Core Purpose

SE (Standard Edition)


Developers of desktop & server apps


The fundamental, core Java platform (this project).

EE (Enterprise Edition)


Developers of large-scale web systems


Extends SE with APIs for web services, servlets, and enterprise features.

ME (Micro Edition)


Developers for embedded devices


A lightweight, compact subset of SE for resource-constrained devices.
JDK, JRE, and JVM

    JVM (Java Virtual Machine): An abstract machine that provides a runtime environment to execute Java bytecode. It is the core component that enables Java's platform independence.

    JRE (Java Runtime Environment): The software package containing the JVM plus the core Java libraries, which is everything needed to run a compiled Java application.

    JDK (Java Development Kit): The complete software development kit for Java programmers. It includes the full JRE, plus development tools like the compiler (javac) and debugger.

B. Technical Implementation Map

Syllabus Topic & Feature


Implementation Location (src/edu/ccrm/...)

Object-Oriented Programming



┣ Encapsulation


model/Person.java (private fields with public getters/setters)

┣ Inheritance


model/Student.java extends model/Person.java

┣ Abstraction


model/Person.java (is an abstract class with an abstract method)

┣ Polymorphism


CrmApp.java (A Person object could be a Student or Instructor)

Advanced Concepts



┣ Design Pattern: Singleton


config/AppConfig.java (private constructor and a static getInstance method)

┣ Design Pattern: Builder


model/Course.java (contains a static nested Builder class for object construction)

┣ Custom Exceptions


util/exception/DuplicateEnrollmentException.java

┣ Exception Handling


CrmApp.java handleEnrollment (uses a try-catch block to handle custom exceptions)

┣ Enums with Constructors


model/Grade.java (enum with fields and a constructor)

┣ Static Nested Class


model/Course.java (the Builder class is a static nested class)

Core Language Features



┣ File I/O with NIO.2


util/io/FileHandler.java (uses Path, Paths, and Files classes)

┣ Recursion (Conceptual)


util/io/FileHandler.java (the getFolderSize method uses Files.walk to traverse the directory tree)

┣ Streams API


service/CourseService.java (findCoursesByInstructor method uses a stream pipeline)

┣ Date/Time API


model/Enrollment.java (uses LocalDate.now() to timestamp enrollments)
📸 Screenshots

Here are some screenshots demonstrating the project setup and the application running.
1. JDK Version Check

This screenshot confirms that the Java Development Kit is installed and configured correctly on the system.
2. Project File Structure in IDE

This shows the organization of all packages and source files within the IntelliJ IDEA development environment.
3. Application Main Menu

A view of the main menu that is displayed in the console when the application starts.
4. Application in Use (Listing Students)

An example of the application listing all students after a new student has been successfully added.