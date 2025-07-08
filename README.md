**Java Concepts and Highlights **

These are key technical points and refined concepts to help you in learning Java :


### 1. `printf()` and Method Chaining

* In Java, `System.out.printf()` allows formatted output similar to C.
* Unlike `print()` and `println()`, `printf()` returns a `PrintStream`, allowing method chaining.


### 2. Short-Circuiting in Logical Operators

* Logical operators (`&&` and `||`) in Java are short-circuiting.
* For `&&`, if the first condition is false, the second is not evaluated.
* For `||`, if the first condition is true, the second is not evaluated.


### 3. Scanner and Buffer Clearing

* When using `next()`, `nextInt()`, `nextDouble()`, etc., and then `nextLine()`, always add an extra `scanner.nextLine()` to clear the newline left in the buffer.


### 4. Reading Boolean Values with Scanner

* `Scanner.nextBoolean()` reads a boolean value.
* Input is case-insensitive (e.g., "true", "FALSE").


### 5. Multiple Scanners on System.in

* Multiple Scanner objects can be created from `System.in`, but they share the same stream.
* Closing one will close `System.in` for all, so Scanner on `System.in` should only be closed at the end of the program.


### 6. Try-With-Resources (Java 7+)

* Allows automatic closing of resources.
* Only works with classes that implement `AutoCloseable`, such as `FileInputStream`, `BufferedReader`, `PrintWriter`.


### 7. Java Arrays and Cloning

* Cloning a 1D array of primitives creates an independent copy.
* Cloning a 1D array of objects copies references (shallow copy).
* Cloning a 2D array clones only the outer array (also a shallow copy).


### 8. Method Signatures and Overloading

* According to the Java Language Specification, a method’s signature includes the method name and parameter types.
* Return type is not part of the method signature.


### 9. Wildcard Imports and Sub-Packages

* `import java.util.*;` imports all classes/interfaces from `java.util`.
* It does **not** import sub-packages (e.g., `java.util.concurrent`).


### 10. Static Import (Java 1.5+)

* Allows access to static members without class qualification.
* Example: `import static java.lang.Math.*;` lets you use `sqrt(4)` directly.


### 11. Exception Handling

* If an exception occurs in a `try` block and is not caught in the `catch`, the default exception handler runs.
* The `finally` block executes regardless of exception handling.


### 12. Dynamic Dispatch and Overridden Methods

* Java uses dynamic dispatch to resolve overridden methods at runtime based on the actual object type.
* Even if the method is called from a superclass (e.g., `super.start()`), the child class’s overridden method (e.g., `run()`) executes.


### 13. ExecutorService and Thread Pools

* `ExecutorService` manages a thread pool, allowing task submission, controlled shutdown, and scheduling.
* A thread pool is a group of pre-instantiated threads ready to execute submitted tasks.


### 14. Immutability of Strings

* Java `String` objects are immutable—once created, their characters cannot be changed.
* However, you can reassign the reference to a new string.


### 15. Static Method Redefinition: Method Hiding

* When a static method is redefined in a subclass, it is **method hiding**, not overriding.
* Method calls are resolved at compile time based on the reference type.


### 16. References vs. Pointers

* Java references are not like C++ pointers.
* You can't perform pointer arithmetic or access raw memory addresses.


### 17. Flaoting Number 

* Float literals must be suffixed with f or F, because by default, decimal numbers are treated as double in Java. Since assignment evaluates from right to left,
  assigning a double to a float without casting or f/F suffix causes a compilation error.


### 18. Integer Type casting 

* All integer literals in Java are of type int by default. To represent a long value, append L or l.
  Implicit narrowing is allowed only if the value fits within the target type's range, otherwise a compilation error occurs.


### Why This Repo?
This is a personal documentation project I built while preparing for Java-based interviews. It reflects real learning, project experience, and deep understanding of Java internals.

Feel free to fork or contribute!

### Related Project
This work supported my project on banking process simulation using ExecutorService for concurrency, which is also available in https://github.com/vineeshagandhe25/Multithreaded-Banking-System
