# Java OOP Challenge: Geometric Shape Manager Refactoring

## Problem Statement

You are working on a geometry calculation library. The current design uses a base class, `Shape`, but it's fundamentally flawed: it allows for the creation of generic `Shape` objects that have no defined area or perimeter, which is a logic error in the application.

Your task is to refactor the existing code to enforce proper design principles, ensuring that only concrete, well-defined shapes (like `Circle` and `Rectangle`) can be instantiated, and that **every** shape guarantees it can provide its `calculateArea()` and `calculatePerimeter()` methods.

## The Brownfield Scenario and Required Changes

The current `Shape` class is a concrete class with placeholder methods. This design violates the principles of **Abstraction** and creates maintenance risk.

**Required Refactoring Steps:**

1.  **Enforce Abstraction/Inheritance:** Modify the `Shape` class so that it cannot be instantiated directly and forces all its subclasses to implement the methods for calculating area and perimeter.
2.  **Maintain Encapsulation:** Ensure all instance variables in the subclasses remain private and are only set via the constructor.
3.  **Ensure Polymorphism:** The unit tests rely on the ability to treat all concrete shapes uniformly as the base type (`Shape`). Your refactoring must maintain this ability.

## Files to Modify/Complete

* `Shape.java` (MUST BE MODIFIED)
* `Circle.java` (Requires a simple constructor and method implementation)
* `Rectangle.java` (Requires a simple constructor and method implementation)

You must make the necessary changes to pass all the provided JUnit 5 tests in `ShapeManagerTest.java`.
