# Part II - Starting with the Bricks: Programming Paradigms

## Chapter 3 Paradigm Overview

There are 3 paradigms: Structured Programming, Object-Oriented Programming and Functional Programming. These paradigms are very close with the three bnig concerns of architecture: function, separation of components, and data management.

## Chapter 4 Structured Programming

Testing shows the presence, not the absence, of bugs. A program can be proven incorrect by a test, but it cannot be proven correct. Tests allow us to check if a program is correct enough for our purposes.

Structured programing forces us to recursively decompose a program into a small set of provable functions. We use tests to try to prove those provable functions incorrect. If those tests fail to prove incorrectness, then we deem the functions to be correcr enough for our purposes.
Functional decomposition is one of our best practices.

## Chapter 5 Object-Oriented Programming

What is OO: encapsulation, inheritance and polymorphism? Not really, we already had those before OO. OO is the ability, through the use of polymorphism, to gain absolute control over every source code dependency the system. It allows the architect to create a plugin architecture, in which high-level policies are independent of modules that contain low-level details. Low-level details are relegated to plugin modules that can be deployed and developed independently from the high level modules.

## Chapter 6 Functional Programming

Functional programming: variables do not vary.
All the problems that we face in concurrent applications - all the problems we face in applications that require multiple threads, and multiple processors - cannot happen if there are no mutable variables.
Event sourcing is a strategy wherein we store the transactions, but not the state. When state is required, we simply apply all the transactions from the beginning of time. Rules of software have teached us what not to do.
Rules of software are the same as they were in 1946.
Software is composed of sequence, selection , iteration and indirection. Nothing more. Nothing less
