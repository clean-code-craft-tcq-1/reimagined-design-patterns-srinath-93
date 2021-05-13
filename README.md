# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.

**ADAPTER**
Intro - software design pattern that allows the interface of an existing class to be used as another interface.
 
**Q1. WHAT KIND OF PROBLEM(S) YOU CAN SOLVE WITH THAT PATTERN AND WHEN YOU USE IT, MAYBE WITH A SHORT EXAMPLE**
ANS:
a. In design, adapters are used when we have a class (Client) expecting some type of object and we have an object (Adaptee) offering the same features but exposing a different interface. For example, 
    * The client makes a request to the adapter by calling a method on it using the target interface.
    * The adapter translates that request on the adaptee using the adaptee interface.
    * Client receive the results of the call and is unaware of adapter’s presence.

b. Consider a memory device and a system, where as a system cannot directly interact with the memory without an interface.
Hence this interface can be a communication protocol which helps these two different incompatible things to interact.

**Q2. HOW THE PATTERN WORKS, WHAT THE BASIC IDEA OF THE PATTERN IS**
ANS:	
a. To be precise, an adapter pattern converts the interface of a class into another interface expected by the clients. Adapters let the classes work together that couldn’t otherwise because of incompatible interfaces.
b. It also depends on the requirement from customer/user end. We are using a communication protocol, which itself is having set of rules.
c. So the user's requirement may depend on the speed of Erasing, writing or reading the data from the memory device or about supporting multiple devices on same bus.
d. For an application which requires multiple devices to be connected to same bus will use I2C communication protocol.
   For another application which  uses more speed might prefer SPI communication protocol.

**Q3. WHAT IS THE MAIN ADVANTAGE AND DISADVANTAGE OF USING THIS PATTERN **

ANS:
Disadvantages:
a. All requests are forwarded, so there is a slight increase in the overhead.
b. Sometimes many adaptations are required along an adapter chain to reach the type which is required.
Advantages:
a. It provides transparency by presenting the design of an application in a modular manner.
b. Contributes to software flexibility.


**Q4. SUMMARY:** The primary purpose of the adapter pattern is to do what physical adapters do in the real world. Just as power adapters provide a wrapper around a power plug for use in a foreign wall socket, an implementation of a software adapter will wrap around a class to provide it with a more common interface that consumers would expect.

**DECORATOR**
**Q1. WHAT KIND OF PROBLEM(S) YOU CAN SOLVE WITH THAT PATTERN AND WHEN YOU USE IT, MAYBE WITH A SHORT EXAMPLE**
ANS:
What problems can it solve?
•  Responsibilities should be added to (and removed from) an object dynamically at run-time
•  Allows an existing rigid functionality to become user-friendly and interactive as well.
Example: In a smart home setup, remote control of the lights or utilities is enabled by the use of decorators.

**Q2. HOW THE PATTERN WORKS, WHAT THE BASIC IDEA OF THE PATTERN IS**
ANS:	
The decorator pattern can be used to extend (decorate) the functionality of a certain object statically, or in some cases at run-time, independently of other instances of the same class, provided some groundwork is done at design time. This is achieved by designing a new Decorator class that wraps the original class.

**Q3. WHAT IS THE MAIN ADVANTAGE AND DISADVANTAGE OF USING THIS PATTERN**
ANS:
Disadvantages:
Decorators need adapters to implememt the new feature or flexibility aspect. This makes it complex in a coding perspective.

Advantages:
It is user friendly and indepedent. It removes dependency especially when a large system is considered.

**Q4. SUMMARY:** To brief a little into what the most common use cases for a decorator are – 
Applying or removing decorators based on changes in state is another common use case. Depending on the scope of the state, decorators can be applied or removed in bulk.
In conclusion, it helps add new behavior at run time, and functionality as well.

**OBSERVER**
**Q1. WHAT KIND OF PROBLEM(S) YOU CAN SOLVE WITH THAT PATTERN AND WHEN YOU USE IT, MAYBE WITH A SHORT EXAMPLE**
ANS:
The Observer defines a one-to-many relationship so that when one object changes state, the others are notified and updated automatically. For example, in a Battery Management System, upon detection of an over current or thermal runaway, the warning systems are automatically triggered and notify the end application/front-end solution about this high priority alert.

**Q2. HOW THE PATTERN WORKS, WHAT THE BASIC IDEA OF THE PATTERN IS**
ANS:	There would be a “keeper" of the data model or the subject. The Observers register themselves with the subject as they are created. Whenever the Subject changes, it broadcasts to all registered Observers that it has changed, and each Observer queries the Subject for that subset of the Subject's state that it is responsible for monitoring.
This allows the number and "type" of "view" objects to be configured dynamically, instead of being statically specified at compile-time.

**Q3. WHAT IS THE MAIN ADVANTAGE AND DISADVANTAGE OF USING THIS PATTERN** 
ANS:
Disadvantages: The Observer interface involves inheritance and becomes complex during implementation. There is no option for composition, as the Observer interface can be instantiated.

Advantages: The Observer pattern lets you vary subjects and observers independently. You can reuse subjects without reusing their observers, and vice versa. It lets you add observers without modifying the subject or other observers.

**Q4. SUMMARY:** This design pattern specifies a "pull" interaction model. Instead of the Subject "pushing" what has changed to all Observers, each Observer is responsible for "pulling" its particular "window of interest" from the Subject.

**MEDIATOR**
**Q1. WHAT KIND OF PROBLEM(S) YOU CAN SOLVE WITH THAT PATTERN AND WHEN YOU USE IT, MAYBE WITH A SHORT EXAMPLE**
ANS: In a complexly interconnected system, the requirement for communication between various modules is provided by a mediator. For example, based on the validations performed internally by the BMS software, the mediator acts as the principle routing facility for the information from the software to the front-end user - either as an alert or as a normal status update.


**Q2. HOW THE PATTERN WORKS, WHAT THE BASIC IDEA OF THE PATTERN IS**
ANS:	Define a separate object - called a mediator, that encapsulates the interaction between a set of objects.
Objects delegate their interaction to a mediator object instead of interacting with each other directly - reducing the complexity and communication overhead of the overall system.

**Q3. WHAT IS THE MAIN ADVANTAGE AND DISADVANTAGE OF USING THIS PATTERN**
ANS:
Disadvantages: As you would have noticed, the mediator implementation is heavy. It would seem to know a lot of things. If not careful, it can become a God object.
Advantages: Mediators keep track of all interfaces - regardless of the number of interfaces. Effectively the communication is faster.

**Q4. SUMMARY:**
The mediator knows about all the components and thus can identify which component has sent the message. The mediator reads the state of the component and decides what to do. It calls the other components based on that. With this, the source component does not know what the receiving component(s) will be. Similarly, the receiving component does not know what the source is. Thus, the components are decoupled.
