Design Patterns
==================
[Behavioral Design Patterns](https://www.codeproject.com/Articles/455228/Design-Patterns-of-Behavioral-Design-Patterns#Command)

### Creational

__The Factory Method Pattern__ Pattern defines an interface
for creating an object, but lets subclasses decide which
class to instantiate. Factory Method lets a class defer
instantiation to subclasses.

###### adheres:

* Dependency Inversion Principle

---

__The Simple Factory Pattern__ To separate the process of creating
concrete objects from the client that uses those objects.
To reduce the dependency of the client on that concrete implementations.

----

__The Singleton Pattern__ Ensure a class only has one instance and provide a global point of access to it.

----

### Structional

__The Bridge Pattern__

[Explenation](https://www.codeproject.com/Articles/98598/How-I-explained-Design-Patterns-to-my-wife-Part)

---

__The Decorator Pattern__ attaches additional
responsibilities to an object dynamically.
Decorators provide a fl exible alternative to
subclassing for extending functionality.

---

### Behavioral

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

patterns user in LV
The Builder (Manager) pattern
The Factory pattern
The Repository pattern
The Strategy pattern
The Provider pattern
The Facade pattern
