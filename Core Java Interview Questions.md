## Most Important Core Java Interview Questions

#### 1. What are the features of java 8, 11, 17 and 21 ?

| Java Version | Key Features |
|-------------|-------------|
| **Java 8 (2014)** | - Lambda Expressions and Functional Interfaces  |
|             | - Streams API for functional-style operations on collections |
|             | - Default and Static Methods in Interfaces |
|             | - New Date and Time API (`java.time` package) |
|             | - Optional Class for Handling Nulls |
|             | - Nashorn JavaScript Engine |
|             | - Collectors and Improvements in `java.util.function` |
|             | - `CompletableFuture` for Asynchronous Programming |
| **Java 11 (2018) (LTS)** | - `var` for Lambda Parameters |
|             | - HTTP Client API (Standard) |
|             | - New String Methods (`isBlank()`, `lines()`, `strip()`, etc.) |
|             | - `Files.readString()` and `Files.writeString()` Methods |
|             | - Running Java Files Without Compilation (`java MyProgram.java`) |
|             | - Garbage Collector (Epsilon and ZGC Introduced) |
|             | - Removal of Java EE and CORBA Modules |
| **Java 17 (2021) (LTS)** | - Sealed Classes (`sealed`, `permits` keyword) |
|             | - Pattern Matching for `switch` (Preview) |
|             | - Strongly Encapsulated JDK Internals |
|             | - New macOS Rendering Pipeline |
|             | - Foreign Function & Memory API (Incubator) |
|             | - New Random Number Generator API |
|             | - Deprecation of `SecurityManager` |
| **Java 21 (2023) (LTS)** | - Virtual Threads (Project Loom) for Lightweight Concurrency |
|             | - Sequenced Collections API (`SequencedSet`, `SequencedMap`) |
|             | - Record Patterns (Finalized) |
|             | - Unnamed Classes and Instance `main()` Methods (Preview) |
|             | - String Templates (Preview) |
|             | - Scoped Values for Thread-local Variables |
|             | - Structured Concurrency API |
|             | - Key GC Improvements (ZGC and G1) |


#### 1. What is JDK, JRE and JVM? What is the difference between them?

**What is JDK?** 
- JDK stands for Java Development Kit. JDK is a complete software development kit that provides everything needed to develop, compile, debug, and run Java applications.
- It provides all the necessary tools, libraries, and environments to compile, debug, and run Java programs.
- It includes the JRE (Java Runtime Environment) and essential development tools like the Java Compiler (javac), Debugger (jdb), and various libraries.
- It provides javac (Java Compiler) to convert source code (.java) into bytecode (.class).
- It allows the packaging of Java applications using jar (Java Archive).
- Developers must install JDK to write and run Java programs.

**Components of JDK:**
- JRE (Java Runtime Environment) - To run Java applications.
- Java Compiler (javac) - Converts Java code into bytecode.
- Java Debugger (jdb) - Helps debug Java programs.
- Java Archive Tool (jar) - Used to create JAR files.
- Java Documentation Tool (javadoc) - Generates documentation.
- Additional Tools - For monitoring, security, and management.

https://www.ggorantala.dev/content/images/2023/10/JDK-JVM-JRE-Diagram.png

**What is JRE?**
- JRE stands for Java Runtime Environment.
- JRE is a subset of JDK that provides an environment for running Java applications but does not include development tools like the compiler.
- The JRE (Java Runtime Environment) includes everything needed to run Java applications.
- JRE includes native libraries (.dll, .so, .dylib) that help JVM interact with the operating system.
- JRE is used only for running Java programs, not for development.
- It includes JVM (Java Virtual Machine) to execute Java bytecode.
- It does not include the Java Compiler (javac).
- If you only need to run Java applications, JRE is sufficient.
- JRE = JVM + Core Java Libraries + Native Libraries + Config Files

**Components of JRE**
- JVM (Java Virtual Machine) - Executes Java bytecode.
- Java Class Libraries - Collections, File handling, Networking, etc.
- Supporting Files - Configuration files for execution.

**What is JVM?** 
- JVM Stands for Java Virtual Machine?
- It is responsible for converting Java bytecode into machine-specific code and executing it.
- JVM is platform-independent, meaning the same Java bytecode can run on different operating systems.
- It performs Just-In-Time (JIT) compilation for optimized execution.
- It manages memory allocation and garbage collection automatically.
- It provides runtime security by preventing unauthorized memory access.
- JVM follows the WORA (Write Once, Run Anywhere) principle.

**Components of JVM:**
- Class Loader - Loads .class files into memory.
- Runtime Memory Areas - Stack, Heap, Method Area, etc.
- Execution Engine - Converts bytecode into native code (machine-level).
- Garbage Collector - Manages memory automatically.
- Security Manager - Ensures Java application security
- JIT Compiler (Just-In-Time Compiler) → Mostly written in C++ for optimizing bytecode execution.
- JVM = Class Loader + Memory Areas + Execution Engine + Native Interface




3. What is String, StringBuffer and StringBuilder classes ? Explain when thay are introduced in Java ? Explain what are the difference between them ? 

