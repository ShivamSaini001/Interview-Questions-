# Accenture Java Developer Interview Questions & Answers

> Based on the interview experience shared in the video **"Accenture
> Java Developer Interview Experience & Questions \[16 LPA+\]"**

------------------------------------------------------------------------

# Table of Contents

1.  Core Java
2.  Exception Handling
3.  Java 8 Features
4.  Spring Boot
5.  Hibernate
6.  Microservices
7.  Important Topics

------------------------------------------------------------------------

# 1. Can private methods be overridden? Why?

**Answer:**

No. Private methods cannot be overridden because they are accessible
only within the class in which they are declared. Since child classes
cannot access private methods, they cannot override them.

``` java
class A {
    private void show() {}
}

class B extends A {
    private void show() {} // New method, not overriding
}
```

------------------------------------------------------------------------

# 2. Can static methods be overridden?

**Answer:**

No. Static methods belong to the class rather than objects. They are
resolved at compile time (static binding), whereas overriding happens at
runtime (dynamic binding).

If a subclass defines a static method with the same signature, it is
called **method hiding**, not overriding.

------------------------------------------------------------------------

# 3. Can private and static methods be overloaded?

**Answer:**

Yes. Overloading depends only on the method signature (number, type, or
order of parameters), not on inheritance.

``` java
class Demo {
    private void test() {}
    private void test(int a) {}

    static void show() {}
    static void show(String s) {}
}
```

------------------------------------------------------------------------

# 4. What is JVM? Explain its components.

**Answer:**

JVM (Java Virtual Machine) executes Java bytecode.

## Components

-   Class Loader
-   Method Area
-   Heap Memory
-   Stack Memory
-   Program Counter Register
-   Native Method Stack
-   Execution Engine
-   Garbage Collector

------------------------------------------------------------------------

# 5. Why is Java platform independent?

**Answer:**

Java source code is compiled into **bytecode**, which can run on any
operating system having a JVM.

**Write Once, Run Anywhere (WORA).**

------------------------------------------------------------------------

# 6. Explain the String Pool.

**Answer:**

The String Pool is a special area inside the heap where string literals
are stored. If the same literal already exists, JVM reuses it instead of
creating another object.

``` java
String s1 = "Java";
String s2 = "Java";

System.out.println(s1 == s2); // true
```

**Benefits**

-   Saves memory
-   Improves performance

------------------------------------------------------------------------

# 7. Why is String immutable?

**Answer:**

Strings are immutable because they provide:

-   Security
-   Thread Safety
-   Performance
-   String Pool Optimization
-   Cached HashCode

------------------------------------------------------------------------

# 8. How do you create a custom exception?

**Answer:**

Extend either `Exception` or `RuntimeException`.

``` java
class InvalidAgeException extends Exception {
    public InvalidAgeException(String msg) {
        super(msg);
    }
}
```

Throw it using:

``` java
throw new InvalidAgeException("Age must be above 18");
```

------------------------------------------------------------------------

# 9. Difference between Checked and Unchecked Exceptions

  Checked Exception         Unchecked Exception
  ------------------------- ---------------------------------
  Checked at compile time   Occurs at runtime
  Must be handled           Handling is optional
  Extends `Exception`       Extends `RuntimeException`
  Example: `IOException`    Example: `NullPointerException`

------------------------------------------------------------------------

# 10. Can exceptions be handled inside static blocks or constructors?

**Answer:**

Yes. Both static blocks and constructors can use `try-catch`.

``` java
static {
    try {
        // code
    } catch(Exception e) {}
}
```

------------------------------------------------------------------------

# 11. Difference between `throw` and `throws`

  throw                        throws
  ---------------------------- ----------------------------
  Used inside a method         Used in method declaration
  Throws an exception object   Declares exception classes

``` java
throw new IOException();
```

``` java
void test() throws IOException {}
```

------------------------------------------------------------------------

# 12. Difference between `private` and `protected`

  private                 protected
  ----------------------- ---------------------------
  Same class only         Same package + subclasses
  Highest encapsulation   Supports inheritance

------------------------------------------------------------------------

# 13. Difference between Method Overloading and Overriding

  Overloading            Overriding
  ---------------------- ----------------------
  Same class             Parent & Child class
  Different parameters   Same signature
  Compile time           Runtime
  Static Binding         Dynamic Binding

------------------------------------------------------------------------

# 14. What is a Functional Interface?

**Answer:**

A Functional Interface contains exactly **one abstract method**.

``` java
@FunctionalInterface
interface Test {
    void display();
}
```

**Uses**

-   Lambda Expressions
-   Streams
-   Method References

------------------------------------------------------------------------

# 15. Can Functional Interfaces have default methods?

**Answer:**

Yes. They can have default and static methods but only **one abstract
method**.

------------------------------------------------------------------------

# 16. Why were Default Methods introduced?

**Answer:**

To provide **backward compatibility**, allowing new methods to be added
to interfaces without breaking existing implementations.

------------------------------------------------------------------------

# 17. Difference between Intermediate and Terminal Stream Operations

## Intermediate Operations

-   `map()`

-   `filter()`

-   `sorted()`

-   Return another stream.

-   Lazy execution.

## Terminal Operations

-   `collect()`

-   `reduce()`

-   `forEach()`

-   `count()`

-   Produce the final result.

------------------------------------------------------------------------

# 18. Difference between `map()` and `flatMap()`

### `map()`

-   One input → One output

### `flatMap()`

-   One input → Multiple outputs
-   Flattens nested collections into a single stream.

------------------------------------------------------------------------

# 19. Difference between `@Controller` and `@RestController`

  @Controller                @RestController
  -------------------------- ----------------------------------------
  Returns View               Returns JSON/XML
  Used in MVC                Used for REST APIs
  Requires `@ResponseBody`   Includes `@ResponseBody` automatically

------------------------------------------------------------------------

# 20. What is CORS?

**Answer:**

CORS (Cross-Origin Resource Sharing) is a browser security mechanism
that controls whether a web page from one origin can access resources
from another origin.

Example:

-   Frontend: `localhost:3000`
-   Backend: `localhost:8080`

------------------------------------------------------------------------

# 21. Difference between `@PathVariable` and `@RequestParam`

### `@PathVariable`

``` text
/users/101
```

``` java
@GetMapping("/users/{id}")
```

### `@RequestParam`

``` text
/users?id=101
```

``` java
@RequestParam int id
```

------------------------------------------------------------------------

# 22. What is Hibernate?

**Answer:**

Hibernate is an ORM (Object Relational Mapping) framework that maps Java
objects to database tables.

**Features**

-   CRUD Operations
-   Relationships
-   Caching
-   Lazy Loading
-   Automatic SQL Generation

------------------------------------------------------------------------

# 23. Difference between Eager and Lazy Fetching

  Eager                    Lazy
  ------------------------ -------------------------
  Loads immediately        Loads when required
  More memory              Better performance
  Default for `OneToOne`   Default for `OneToMany`

------------------------------------------------------------------------

# 24. Difference between `get()` and `load()` in Hibernate

  get()                      load()
  -------------------------- ----------------------------
  Fetches immediately        Returns proxy
  Returns `null` if absent   Throws exception if absent
  Hits DB immediately        Hits DB when needed

------------------------------------------------------------------------

# 25. What are Microservices?

**Answer:**

Microservices is an architecture where an application is divided into
small, independent services.

Each service:

-   Has its own database
-   Can be deployed independently
-   Communicates using REST APIs, gRPC, or messaging systems like Kafka

## Advantages

-   Scalability
-   Fault Isolation
-   Independent Deployment
-   Better Maintainability

## Disadvantages

-   Increased complexity
-   Distributed transactions
-   Monitoring challenges
-   Network latency

------------------------------------------------------------------------

# Important Topics to Prepare

1.  JVM Architecture
2.  String Pool & String Immutability
3.  Exception Handling
4.  OOP Concepts
5.  Method Overloading vs Overriding
6.  Java 8 (Streams, Lambda, Functional Interfaces)
7.  Spring Boot Annotations
8.  CORS
9.  Hibernate
10. Microservices
