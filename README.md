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

---

__The Composite Pattern__

[link1](https://youtu.be/2HUnoKyC9l0)


---

__The Decorator Pattern__ attaches additional
responsibilities to an object dynamically.
Decorators provide a fl exible alternative to
subclassing for extending functionality.

local references:
/home/zeecher/Videos/Development/Design Patterns/Design Patterns in PHP/1 - The Decorator Pattern.mp4

---

### Behavioral

[Behavioral Design Patterns](https://www.codeproject.com/Articles/455228/Design-Patterns-of-Behavioral-Design-Patterns#Command)


__ Null Object Design Pattern__


__Momento Design Pattern__
Undo/Redo

__The Chain of Responsibility Pattern__ Chain object calls while giving each of then objects 
the ability to eigher end the execution and handle the request, if it can't handle the request then 
send the request up the chain.

###### pattern similarities:

* Decorator Pattern -> Destinction: but in chain u can stop the execution any time in the chain

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
