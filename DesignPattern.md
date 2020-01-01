### Design Pattern

#### Creational 
- Builder  
- Factorties  
-Abstract Factory  
-Factory Method  

#### Structural
- Adapter  
- Bridge  
- Facade  
...

#### Behavioral
- Iterator  
- Observer  
- Strategy  
...

#### Design Principles
- Single Responsibility Principle(SRP)  
 *separation of concern  
 Every class take only one kind of responsibility. For example, you create a journal class, the CRUD of journal is within
 the responsibility of this class, but the read and write from and to the system is not part of job from here.  
- Open-closed Principle(OCP)  
 open for extension, but closed for modification" that is, such an entity can allow its behaviour to be extended without modifying its source code.
- Liskov Substitution Principle(LSP)  
 if S is a subtype of T, then objects of type T may be replaced with objects of type S (i.e. an object of type T may be substituted with any object of a subtype S) without altering any of the desirable properties of the program (correctness, task performed, etc.)  
 Typical example:   
 `Rectangle` and `Square`
 If the derived class can't use all the methods(extends all the behavours of base class), it breaks LSP
- Interface Segregation Principle(ISP)  
ISP splits large interfaces into smaller and more specific ones so that clients will only have to know about the methods that are of interest to them. ISP is focused on the idea of each interface representing one discrete and cohesive behavior.
- Dependency Inversion Principle(DIP)  
A. High-level modules should not depend on low level modules, both should depend on abstractions. 
B. Abstractions should not depend on details, details should depend on abstractions.   
An object shouldn't control the creation of its dependencies, it should just advertise what dependency it needs and let the caller provide it. But it doesn't specify whether the dependency should be a concrete type or an interface.





