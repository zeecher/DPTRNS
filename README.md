# DPTRNS


__The Strategy Pattern__ defines a family of algorithms,
encapsulates each one, and makes them interchangeable.
Strategy lets the algorithm vary independently from
clients that use it.

__The Observer Pattern__ defines a one-to-many
dependency between objects so that when one
object changes state, all of its dependents are
notified and updated automatically.

__The Decorator Pattern__ attaches additional
responsibilities to an object dynamically.
Decorators provide a fl exible alternative to
subclassing for extending functionality.

---

__The Factory Method__ Pattern defi nes an interface
for creating an object, but lets subclasses decide which
class to instantiate. Factory Method lets a class defer
instantiation to subclasses.

###### adheres:

* Dependency Inversion Principle

----

# OO Design Principles

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
 
</dl>
