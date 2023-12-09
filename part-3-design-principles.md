# Part III - Design Principles

## Chapter 7 SRP: The Single Responsibility Principle

A module should be responsible to one, and only one, user or stakeholder -> A module should be responsible to one, and only one, actor.
SRP is about functions and classes, but it reappears in a  different form at two more levels. At the level of components, it becomes the Common Closure Principle. At the architectural level, it becomes the Axis of Change responsible for the creation of Architectural boundaries.

## Chapter 8 OCP: The Open-Closed Principle

A software artifact should be open for extension but closed for modification. The goal is to make the system easy to extend without incurring a high impact of change. This goal is accomplished by partitioning the system into components, and arraging those components into a dependency hierarchy that protects higher-level components from changes in lower-level components.

## Chapter 9 LSP: The Liskov Substitution Principle

The LSP, can, and should, be extended to the level of architecture. A simple violation of substitutability, can cause a system's architecture to be polluted with a significant amount of extra mechanisms.

## Chapter 10 ISP: The Interface Segregation Principle

Depending on something that carries baggage than you dont need can cause you troubles that you didnt expect.

## Chapter 11 DIP: The Dependency Inversion Principle

It tells us that the most flexible systems are those in which source code dependencies refer only to abstractions, not to concretions.
- Dont refer to volatile concrete classes -> refer to abstract interfaces instead
- Dont derive from volatile concrete classes
- Dont override concrete functions
- Never mention the name of anything concrete and volatile

When source code dependencies are inverted against the flow of control it is called Dependency Inversion
