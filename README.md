# 🧸 Section 2: Dependency Injection
## What is Dependency Injection?
> Summary: Dependency Injection is a process through which the Spring container "injects" objects into other objects (injecting dependencies).
> This allows loose coupling of components and moves the responsibility of managing components onto the Container
- Dependency Injection is the main functionality provided by Spring IoC (Inversion of Control)
- The Spring-Core module is responsible for injecting dependencies through either `Constructor` or `Setter` methods.
- The design principle of IoC emphasizes keeping the Java classes **independent** of each other and the container frees them from object creation and maintenance.
- These classes, managed by Spring, must adhere to standard definition of Java-Bean (Java Bean are objects that form the backbone of your application and that are managed by the Spring IoC Container. A bean is an object that is instantiated, assembled, and otherwise managed by a Spring IoC Container). [Java Bean](https://www.baeldung.com/spring-bean#:~:text=Here's%20a%20definition%20of%20beans,by%20a%20Spring%20IoC%20container.)
- Dependency Injection in Spring also ensures loose-coupling between the classes
- 
