# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.

**ADAPTER**
Intro - software design pattern that allows the interface of an existing class to be used as another interface.
 
Q1. WHAT KIND OF PROBLEM(S) YOU CAN SOLVE WITH THAT PATTERN AND WHEN YOU USE IT, MAYBE WITH A SHORT EXAMPLE
ANS:
a. In design, adapters are used when we have a class (Client) expecting some type of object and we have an object (Adaptee) offering the same features but exposing a different interface. For example, 
    * The client makes a request to the adapter by calling a method on it using the target interface.
    * The adapter translates that request on the adaptee using the adaptee interface.
    * Client receive the results of the call and is unaware of adapter’s presence.

b. Consider a memory device and a system, where as a system cannot directly interact with the memory without an interface.
Hence this interface can be a communication protocol which helps these two different incompatible things to interact.

Q2. HOW THE PATTERN WORKS, WHAT THE BASIC IDEA OF THE PATTERN IS
ANS:	
a. To be precise, an adapter pattern converts the interface of a class into another interface expected by the clients. Adapters let the classes work together that couldn’t otherwise because of incompatible interfaces.
b. It also depends on the requirement from customer/user end. We are using a communication protocol, which itself is having set of rules.
c. So the user's requirement may depend on the speed of Erasing, writing or reading the data from the memory device or about supporting multiple devices on same bus.
d. For an application which requires multiple devices to be connected to same bus will use I2C communication protocol.
   For another application which  uses more speed might prefer SPI communication protocol.

Q3. WHAT IS THE MAIN ADVANTAGE AND DISADVANTAGE OF USING THIS PATTERN 
ANS:
Disadvantages:
a. All requests are forwarded, so there is a slight increase in the overhead.
b. Sometimes many adaptations are required along an adapter chain to reach the type which is required.

Advantages:
a. It provides transparency by presenting the design of an application in a modular manner.
b. Contributes to software flexibility.
