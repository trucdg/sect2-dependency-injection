# 🧸 Section 2: Dependency Injection
##  🔑 What is Dependency Injection?
> Key Takeaways:
>
> Dependency Injection is a process through which the Spring container "injects" objects into other objects (injecting dependencies).
>
> This allows loose coupling of components and moves the responsibility of managing components onto the Container
- Dependency Injection is the main functionality provided by Spring IoC (Inversion of Control)
- Dependency Injection is a pattern we can use to implement IoC, where the control is being inverted is setting and object's dependencies.
- Connecting objects with other objects, or "injecting" objects into other objects, is done by an assembler rather than by the objects themselves.
- The Spring-Core module is responsible for injecting dependencies through either `Constructor` or `Setter` methods.
- The design principle of IoC emphasizes keeping the Java classes **independent** of each other and the container frees them from object creation and maintenance.
- These classes, managed by Spring, must adhere to standard definition of Java-Bean (Java Bean are objects that form the backbone of your application and that are managed by the Spring IoC Container. A bean is an object that is instantiated, assembled, and otherwise managed by a Spring IoC Container). [Java Bean](https://www.baeldung.com/spring-bean#:~:text=Here's%20a%20definition%20of%20beans,by%20a%20Spring%20IoC%20container.)
  
Here's how we would create an object dependency in traditional programming:

```java
public class Store {
  private Item item;
  public Store() {
    item = new ItemImpl1() ;
  }
}
```
In the example above, we need to instantiate an implementation of the ***Item*** interface within the ***Store** class itself.

However, by using DI, we can rewrite the example without specifying the implementation of the ***Item*** that we want:

```java
public class Store {
  private Item item;
  public Store(Item item) {
    this.item = item;
  }
}
```

In the next sections, we will look at how we can provide the implementation of ***Item*** through metadata.

## 🔑 Advantages of Dependency Injection
- Dependency Injection in Spring also ensures loose-coupling between the classes
- Improves code reusability
- Ease the unit testing of applications through mocking/ stubbing injected dependencies
- Reduce the boilerplate code because dependencies are initialized by their injector component
- Decouples component logic
- Makes it easier to extend the application classes
- Enhances the configuration of applications






