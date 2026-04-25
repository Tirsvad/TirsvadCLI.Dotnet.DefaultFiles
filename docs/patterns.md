

# 🧩 Software Design Patterns

## Table of Contents

- [🏛️ Conceptual (Architectural) Patterns](#conceptual-patterns)
- [🛠️ Creational Patterns](#creational-patterns)
- [🏗️ Structural Patterns](#structural-patterns)
- [🤹 Behavioral Patterns](#behavioral-patterns)

This document summarizes common software design patterns, grouped by category, and indicates which programming languages they are most applicable to (C, C++, C#, Python).

<a name="conceptual-patterns"></a>
## 🏛️ Conceptual (Architectural) Patterns

- **Layered Architecture (e.g., Clean Architecture, Onion, Hexagonal)**
  - Organizes code into layers with clear responsibilities and separation of concerns.
  - Good for: C, C++, C#, Python (and most languages)
- **Client-Server**
  - Separates client and server responsibilities, common in networked and web applications.
  - Good for: C, C++, C#, Python
- **Model-View-Controller (MVC)**
  - Separates data (model), UI (view), and logic (controller) for better maintainability.
  - Good for: C#, Python, C++, web frameworks
- **Event-Driven Architecture**
  - Uses events to trigger and communicate between components, promoting loose coupling.
  - Good for: C#, Python, C++, C
- **Microservices**
  - Decomposes applications into small, independent services that communicate over a network.
  - Good for: C#, Python, C++, (primarily used in distributed/cloud systems)

<a name="creational-patterns"></a>
## 🛠️ Creational Patterns

- **Singleton**
  - Ensures a class has only one instance and provides a global point of access.
  - Good for: C, C++, C#, Python
- **Factory Method**
  - Defines an interface for creating an object, but lets subclasses alter the type of objects that will be created.
  - Good for: C++, C#, Python
- **Abstract Factory**
  - Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
  - Good for: C++, C#, Python
- **Builder**
  - Separates the construction of a complex object from its representation.
  - Good for: C++, C#, Python
- **Prototype**
  - Creates new objects by copying an existing object, known as the prototype.
  - Good for: C++, C#, Python
 
<a name="structural-patterns"></a>
## 🏗️ Structural Patterns

- **Adapter**
  - Allows incompatible interfaces to work together.
  - Good for: C++, C#, Python
- **Bridge**
  - Decouples an abstraction from its implementation.
  - Good for: C++, C#, Python
- **Composite**
  - Composes objects into tree structures to represent part-whole hierarchies.
  - Good for: C++, C#, Python
- **Decorator**
  - Adds responsibilities to objects dynamically.
  - Good for: C++, C#, Python
- **Facade**
  - Provides a simplified interface to a complex subsystem.
  - Good for: C++, C#, Python
- **Flyweight**
  - Reduces memory usage by sharing as much data as possible with similar objects.
  - Good for: C++, C#, Python
- **Proxy**
  - Provides a surrogate or placeholder for another object.
  - Good for: C++, C#, Python

<a name="behavioral-patterns"></a>
## 🤹 Behavioral Patterns

- **Chain of Responsibility**
  - Passes a request along a chain of handlers.
  - Good for: C++, C#, Python
- **Command**
  - Encapsulates a request as an object.
  - Good for: C++, C#, Python
- **Interpreter**
  - Implements a grammar for a language and an interpreter to interpret sentences in the language.
  - Good for: C++, C#, Python
- **Iterator**
  - Provides a way to access elements of a collection sequentially.
  - Good for: C, C++, C#, Python
- **Mediator**
  - Defines an object that encapsulates how a set of objects interact.
  - Good for: C++, C#, Python
- **Memento**
  - Captures and restores an object's internal state.
  - Good for: C++, C#, Python
- **Observer**
  - Defines a one-to-many dependency between objects.
  - Good for: C++, C#, Python
- **State**
  - Allows an object to alter its behavior when its internal state changes.
  - Good for: C++, C#, Python
- **Strategy**
  - Defines a family of algorithms, encapsulates each one, and makes them interchangeable.
  - Good for: C++, C#, Python
- **Template Method**
  - Defines the skeleton of an algorithm in a method, deferring some steps to subclasses.
  - Good for: C++, C#, Python
- **Visitor**
  - Separates an algorithm from the object structure on which it operates.
  - Good for: C++, C#, Python

---
For more details and code examples, refer to language-specific documentation or design pattern books.
