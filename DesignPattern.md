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

#### Design Principles(SOLID)
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


### gamma categoriazation
- Creational Patterns  
Deal with the creations(construction) of objects  
Explicit(constructor) vs implicit(DI, reflection, etc)  
Wholesale(single statement) vs piecewise(step-by-step)
- Structural Patterns  
Concerned with the structure(eg: class members)  
Many patterns are wrappers that mimic the underlying class interface  
Stree the importance of good api design  
- Behavioral Patterns  
They are all different, no central theme


### Design Pattern
- Builder  
piecewise  
- Factory  
A component responsible solely for the wholesale(not piecewise) creation of objects  
Code Example:
```
class Point{
  private double x, y;
  private Point(double x, double y){
    this.x=x;
    this.y=y;
  }
  public static class Factory{
    public static newCartesianPoint(double x, double y){
      return new Point(x, y);
    }
    public static Point newPolarPoint(double rho, double theta){
      return new Point(rho*Math.cos(theta), rho*Math.sin(theta));
    }
  }
}

class Demo{
  public static void main(Strings[] args){
    Point point=Point.Factory.newCartesionPoint(3, 4);
    Point point2=new Point(3, 4);
  }
}
```
- Singleton
A component which is stantiated only once . 
```
class BasicSingleton{
  private BasicSingleton(){};
  private static final BasicSingleton INSTANCE = new BasicSingleton();
  public static BasicSingleton getInstance()
  {
    return INSTANCE;
  }
  private int value;
  public getValue(){
    return value;
  }
  public setValue(value){
    this.value=value;
  }
}

class Demo{
  public static void main(Strings[] args){
    BasicSingleton singleton=BasicSingleton.getInstance();
    
  }
}
```








