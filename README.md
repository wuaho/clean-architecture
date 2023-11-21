# Clean Architecture
Summary of the Clean Architecture book

### PART I Introduction

Chapter 1 What Is Design and Architecture?


Architecture and Design are the same thing. The goal of software architecture is to minimize the human resources required to build and maintain the required system. So you dont spend money on more programmers and have less productivity.

Chapter 2 A Tale of Two Values

Behaviour and Structure. Software developers are responsible for ensuring that both of these values remain high. We are software developers are the ones that need to know and fight when structure changes are needed because no one else knows the importance of architecture over the urgency of features. 

### PART II Starting with the Bricks: Programming Paradigms

Chapter 3 Paradigm Overview


There are 3 paradigms: Structured Programming, Object-Oriented Programming and Functional Programming. These paradigms are very close with the three bnig concerns of architecture: function, separation of components, and data management.

Chapter 4 Structured Programming

Testing shows the presence, not the absence, of bugs. A program can be proven incorrect by a test, but it cannot be proven correct. Tests allow us to check if a program is correct enough for our purposes.

Structured programing forces us to recursively decompose a program into a small set of provable functions. We use tests to try to prove those provable functions incorrect. If those tests fail to prove incorrectness, then we deem the functions to be correcr enough for our purposes.
Functional decomposition is one of our best practices.

Chapter 5 Object-Oriented Programming

What is OO: encapsulation, inheritance and polymorphism? Not really, we already had those before OO. OO is the ability, through the use of polymorphism, to gain absolute control over every source code dependency the system. It allows the architect to create a plugin architecture, in which high-level policies are independent of modules that contain low-level details. Low-level details are relegated to plugin modules that can be deployed and developed independently from the high level modules.

Chapter 6 Functional Programming

Functional programming: variables do not vary.
All the problems that we face in concurrent applications - all the problems we face in applications that require multiple threads, and multiple processors - cannot happen if there are no mutable variables.
Event sourcing is a strategy wherein we store the transactions, but not the state. When state is required, we simply apply all the transactions from the beginning of time. Rules of software have teached us what not to do.
Rules of software are the same as they were in 1946.
Software is composed of sequence, selection , iteration and indirection. Nothing more. Nothing less

### PART III Design Principles

Chapter 7 SRP: The Single Responsibility Principle

A module should be responsible to one, and only one, user or stakeholder -> A module should be responsible to one, and only one, actor.
SRP is about functions and classes, but it reappears in a  different form at two more levels. At the level of components, it becomes the Common Closure Principle. At the architectural level, it becomes the Axis of Change responsible for the creation of Architectural boundaries.

Chapter 8 OCP: The Open-Closed Principle

A software artifact should be open for extension but closed for modification. The goal is to make the system easy to extend without incurring a high impact of change. This goal is accomplished by partitioning the system into components, and arraging those components into a dependency hierarchy that protects higher-level components from changes in lower-level components.

Chapter 9 LSP: The Liskov Substitution Principle

The LSP, can, and should, be extended to the level of architecture. A simple violation of substitutability, can cause a system's architecture to be polluted with a significant amount of extra mechanisms.

Chapter 10 ISP: The Interface Segregation Principle

Depending on something that carries baggage than you dont need can cause you troubles that you didnt expect.

Chapter 11 DIP: The Dependency Inversion Principle

It tells us that the most flexible systems are those in which source code dependencies refer only to abstractions, not to concretions.
- Dont refer to volatile concrete classes -> refer to abstract interfaces instead
- Dont derive from volatile concrete classes
- Dont override concrete functions
- Never mention the name of anything concrete and volatile

When source code dependencies are inverted against the flow of control it is called Dependency Inversion

### PART IV Component Principles
If the SOLID principles tell us how to arrange the bricks into walls and rooms, then the component principles tell us how to arrange the rooms into buildings. Large software system, like large buildings, are built out of smaller componentes.

Chapter 12 Components

Componentes are the units of deployment. They are the smallest entities that can be deployed as part of a system.
Murphy's law of program size: Programs will grow to fill all available compile and link time. Moore law won vs Murphy's law.

Chapter 13 Component Cohesion

Which classes being in which components?
Principles of component cohesion:
- REP: the Reuse/Release Equivalence Principle
- CCP: the Common Closure Principle
- CRP: the Common Reuse Principle

Explanations:
- REP: modules in a component should make sense together.
- CCP: gather into components those classes that change for the same reasons and at the same times. Separate into different components those classes that change at different times and for different reasons. Is like SRP for components.
- SRP + CCP summarized: gather together those things that change at the same times and for the same reasons. Separate those things that change at different times or for different reasons.
- CRP: dont force users of a component to depend on things they dont need.



