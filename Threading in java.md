# Threading In Java

### **What is Thread?**

- A thread in java is a light-weighted process, or we can say the smallest part of the process that allows a program to operate/execute more efficiently by running multiple tasks simultaneously.    
- In order to perform complicated tasks in the background, we use the thread concept in java. All the tasks are executed without affecting the main program.  
- In a program/process, all the threads have their own separate path for execution. So, each thread of a process is independent.
- Another benifit of using threads is that if a thread gets an exception or error at the time of its execution, it does not affect execution of the other threads.
- The Java Virtual Machine allows an application to have multiple threads of execution running concurrently.

### **What is Multi-threading?**

- When multiple threads are executed parallel at the same time, this process is known as multi-threading.

### **Single-threaded vs. Multi-threaded Applications?**

 - **Single-threaded Applications:** A single-threaded application executes all tasks in a single sequence using only one thread. This means that the program runs one task at a time and processes each instruction sequentially.  

    **Advantages:**
    - **No Race Conditions** – Since only one thread runs, no data inconsistency occurs due to parallel execution.
    - **Lower Memory Usage** – Single-threaded applications consume less system memory compared to multi-threaded applications.
    - **No Deadlocks** – Deadlocks happen in multi-threaded programs when multiple threads wait for resources. In single-threaded applications, this is not an issue.

    **Disadvantages:**
    - **Slow Performance** – The program executes tasks sequentially, which means it cannot take advantage of multi-core processors.
    - **Cannot Utilize Multi-Core Processors** – Modern CPUs have multiple cores, but single-threaded applications cannot use them efficiently.


- **Multi-threaded Applications:** A multi-threaded application can execute multiple tasks at the same time using multiple threads. Each thread runs independently, which improves performance and responsiveness.

    **Advantages:**
    - **Faster Execution** – Tasks run simultaneously, improving speed.
    - **Better CPU Utilization** – Uses multiple CPU cores efficiently.
    - **Improved Responsiveness** – Useful for UI applications, preventing freezing.
    - **Efficient Resource Sharing** – Threads share memory and data, reducing redundancy.













