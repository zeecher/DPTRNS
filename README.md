Design Patterns
==================

The 23 Gang of Four (GoF) patterns are generally considered the foundation for all other patterns. They are categorized in three groups: Creational, Structural, and Behavioral (for a complete list see below).


### Creational

----

__Abstract Factory__ Creates an instance of several families of classes

###### Definition:
Provide an interface for creating families of related or dependent objects without specifying their concrete classes.

[link1](http://www.dofactory.com/net/abstract-factory-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/AbstractFactory/README.html)

----

__The Factory Method Pattern__ Pattern defines an interface
for creating an object, but lets subclasses decide which
class to instantiate. Factory Method lets a class defer
instantiation to subclasses.

###### adheres:

* Dependency Inversion Principle

[link1](http://www.dofactory.com/net/factory-method-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/FactoryMethod/README.html)

---

__The Simple Factory Pattern__ To separate the process of creating
concrete objects from the client that uses those objects.
To reduce the dependency of the client on that concrete implementations.

It differs from the static factory because it is not static. Therefore, you can have multiple factories, differently parametrized, you can subclass it and you can mock it. It always should be preferred over a static factory!

[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/SimpleFactory/README.html)

----

__Static Factory__

###### Definition:
Similar to the AbstractFactory, this pattern is used to create series of related or dependent objects. The difference between this and the abstract factory pattern is that the static factory pattern uses just one static method to create all types of objects it can create. It is usually named factory or build.

[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/StaticFactory/README.html)

----

__Builder__ Separates object construction from its representation 
Builder is an interface that build parts of a complex object.

###### Definition:
Separate the construction of a complex object from its representation so that the same construction process can create different representations.

[link1](http://www.dofactory.com/net/builder-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/Builder/README.html)

----

__Prototype__ A fully initialized instance to be copied or cloned 

###### Definition:
* Specify the kind of objects to create using a prototypical instance, and create new objects by copying this prototype.
* To avoid the cost of creating objects the standard way (new Foo()) and instead create a prototype and clone it.

###### Examples:
Large amounts of data (e.g. create 1,000,000 rows in a database at once via a ORM).

[link1](http://www.dofactory.com/net/prototype-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/Prototype/README.html)

----

__The Singleton Pattern__ A class of which only a single instance can exist

###### Definition:
Ensure a class only has one instance and provide a global point of access to it.

[link1](http://www.dofactory.com/net/singleton-design-pattern)

----

__Multiton__ To have only a list of named instances that are used, like a singleton but with n instances.

__THIS IS CONSIDERED TO BE AN ANTI-PATTERN! FOR BETTER TESTABILITY AND MAINTAINABILITY USE DEPENDENCY INJECTION!__

[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/Multiton/README.html)

----

__Pool__

The object pool pattern is a software creational design pattern that uses a set of initialized objects kept ready to use – a “pool” – rather than allocating and destroying them on demand. A client of the pool will request an object from the pool and perform operations on the returned object. When the client has finished, it returns the object, which is a specific type of factory object, to the pool rather than destroying it.

Object pooling can offer a significant performance boost in situations where the cost of initializing a class instance is high, the rate of instantiation of a class is high, and the number of instances in use at any one time is low. The pooled object is obtained in predictable time when creation of the new objects (especially over network) may take variable time.

However these benefits are mostly true for objects that are expensive with respect to time, such as database connections, socket connections, threads and large graphic objects like fonts or bitmaps. In certain situations, simple object pooling (that hold no external resources, but only occupy memory) may not be efficient and could decrease performance.

[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Creational/Pool/README.html)

----

### Structural

In Software Engineering, Structural Design Patterns are Design Patterns that ease the design by identifying a simple way to realize relationships between entities.

__Adapter / Wrapper__ Match interfaces of different classes

###### Definition:
Convert the interface of a class into another interface clients expect. Adapter lets classes work together that couldn't otherwise because of incompatible interfaces.

###### Examples
* DB Client libraries adapter
* Using multiple different webservices and adapters normalize data so that the outcome is the same for all

----

__The Bridge Pattern__ Separates an object’s interface from its implementation

###### Definition:
Decouple an abstraction from its implementation so that the two can vary independently.

[codeproject](https://www.codeproject.com/Articles/98598/How-I-explained-Design-Patterns-to-my-wife-Part)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Structural/Bridge/README.html)
[youtube](https://youtu.be/9jIgSsIfh_8)

----

__The Composite Pattern__ A tree structure of simple and composite objects

###### Definition 
* To treat a group of objects the same way as a single instance of the object.
* Compose objects into tree structures to represent part-whole hierarchies. Composite lets clients treat individual objects and compositions of objects uniformly.

[dofactory](http://www.dofactory.com/net/composite-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Structural/Composite/README.html)
[youtube](https://youtu.be/2HUnoKyC9l0)

----
__Data Mapper__

###### Definition:

A Data Mapper, is a Data Access Layer that performs bidirectional transfer of data between a persistent data store (often a relational database) and an in memory data representation (the domain layer). The goal of the pattern is to keep the in memory representation and the persistent data store independent of each other and the data mapper itself. The layer is composed of one or more mappers (or Data Access Objects), performing the data transfer. Mapper implementations vary in scope. Generic mappers will handle many different domain entity types, dedicated mappers will handle one or a few.

The key point of this pattern is, unlike Active Record pattern, the data model follows Single Responsibility Principle.

----

__The Decorator Pattern__ Add responsibilities to objects dynamically

###### Definition:
* To dynamically add new functionality to class instances.
* Attaches additional responsibilities to an object dynamically.
* Decorators provide a flexible alternative to subclassing for extending functionality.

[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Structural/Decorator/README.html)
[dofactory](http://www.dofactory.com/net/decorator-design-pattern)
[youtube](https://youtu.be/j40kRwSm4VE)

local references:
/home/zeecher/Videos/Development/Design Patterns/Design Patterns in PHP/1 - The Decorator Pattern.mp4

----

__Facade__ A single class that represents an entire subsystem

###### Defenition:
Provide a unified interface to a set of interfaces in a subsystem. Façade defines a higher-level interface that makes the subsystem easier to use.

[dofactory](http://www.dofactory.com/net/facade-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Structural/Facade/README.html)
[youtube](https://youtu.be/B1Y8fcYrz5o)

----

__Flyweight__	A fine-grained instance used for efficient sharing

###### Defenition:

* Use sharing to support large numbers of fine-grained objects efficiently.
* To minimise memory usage, a Flyweight shares as much as possible memory with similar objects. It is needed when a large amount of objects is used that don’t differ much in state. A common practice is to hold state in external data structures and pass them to the flyweight object when needed.

[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Structural/Flyweight/README.html)
[dofactory](http://www.dofactory.com/net/flyweight-design-pattern)
[youtube](https://youtu.be/0vV-R2926ss)

----

__Proxy__	An object representing another object

###### Defenition:
* Provide a surrogate or placeholder for another object to control access to it.
* To interface to anything that is expensive or impossible to duplicate.

[youtube](https://youtu.be/cHg5bWW4nUI)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Structural/Proxy/README.html)
[dofactory](http://www.dofactory.com/net/proxy-design-pattern)

----
### Behavioral

Behavioral design patterns are design patterns that identify common communication patterns between objects and realize these patterns. By doing so, these patterns increase flexibility in carrying out this communication.

[Behavioral Design Patterns](https://www.codeproject.com/Articles/455228/Design-Patterns-of-Behavioral-Design-Patterns#Command)


__ Null Object Design Pattern__


__Momento Design Pattern__
Undo/Redo

__The Chain of Responsibility Pattern__ A way of passing a request between a chain of objects 

###### Definition:
Chain object calls while giving each of then objects 
the ability to eigher end the execution and handle the request, if it can't handle the request then 
send the request up the chain.

###### pattern similarities:

* Decorator Pattern -> Destinction: but in chain u can stop the execution any time in the chain

local : /home/zeecher/Videos/Development/Design Patterns/Design Patterns in PHP
[codeproject](https://www.codeproject.com/Articles/455228/Design-Patterns-of-Behavioral-Design-Patterns#Chain)
[dofactory](http://www.dofactory.com/net/chain-of-responsibility-design-pattern)
[designpatternsphp](http://designpatternsphp.readthedocs.io/en/latest/Behavioral/ChainOfResponsibilities/README.html)


---

__The Command Pattern__


---

__The Strategy Pattern__ defines a family of algorithms,
encapsulates each one, and makes them interchangeable.
Strategy lets the algorithm vary independently from
clients that use it.

---

__The Observer Pattern__ defines a one-to-many
dependency between objects so that when one
object changes state, all of its dependents are
notified and updated automatically.

---

__The State Pattern__ allows an object to alter its behavior when its internal state changes. The object will appear to change its class. 

###### pattern similarities:

* Strategy Pattern

---

__The Iterator Pattern__ provides a way to access the elements of an aggreage object 
sequentially without exposing its unberlying representation.

---

__The Template Method Pattern__ Define the skeleton of an algorithm in an operation, 
deferring some steps to subclasses. Template Method lets subclasses redefine certain steps of an algorithm without changing the algorithm's structure.

###### adheres:

* Don't call us, we'll call you

---

OO Design Principles
===================================
[Object Oriented Design principles explained](https://www.codeproject.com/Articles/93369/How-I-explained-OOD-to-my-wife)

<dl>
  <dt>Encapsulate what varies</dt>
  <dd></dd>
  
  <dt>Favor composition over inheritance</dt>
  <dd></dd>
  
  <dt>Program to interface, not implementations</dt>
  <dd>identify the
aspects that vary and separate them from what stays the same.</dd>

  <dt>Strive for loosely coupled designs between objects that interact.</dt>
  <dd>Loosely coupled designs allow us to build flexible OO systems that can handle change because they minimize the    interdependency between objects.</dd>
  
  <dt>Classes should be open for extension, but closed for modification. (Open-Closed)</dt>
  <dd>
Our goal is to allow classes to be easily extended to
incorporate new behavior without modifying existing code.
What do we get if we accomplish this? Designs that are
resilient to change and fl exible enough to take on new
functionality to meet changing requirements.

While it may seem like a contradiction,
there are techniques for allowing code to be
extended without direct modif ication.
Be careful when choosing the areas of code
that need to be extended; applying the
Open-Closed Principle EVERYWHERE
is wasteful, unnecessary, and can lead to
complex, hard to understand code

Strive to design our system so that the closed parts are isolated from our new extensions.
</dd>
 
 <dt>Depend upon abstractions. Do not
depend upon concrete classes.</dt>
<dd>
Our high-level components should not depend on our low-level
components; rather, they should both depend on abstractions.</dd>

<dt>Don't call us, we'll call you</dt>
<dd>Superclasses are running the show, so let them call your subclasses when 
they're needed, just like they do in Hollywood</dd>
 
</dl>

###### Inversion of Control Containers and the Dependency Injection pattern
* [Dependency Injection Explained](https://docs.phalconphp.com/en/3.0.0/reference/di-explained.html)
* [Dependency Injection/Service Location¶](https://docs.phalconphp.com/en/3.0.0/reference/di.html)
* Inversion of Control pattern

###### Example containers
* [Getting started with PHP-DI](http://php-di.org/doc/getting-started.html)

patterns user in LV
The Builder (Manager) pattern
The Factory pattern
The Repository pattern
The Strategy pattern
The Provider pattern
The Facade pattern
