# DIU Transport Management System

A simple **Java OOP-based Transport Management System** developed as a basic Java project.

The main purpose of this project is to practice and demonstrate the fundamental concepts of **Object-Oriented Programming (OOP) in Java** through a small real-world management system.

## Project Overview

The **DIU Transport Management System** manages basic information about:

* Students
* Drivers
* Buses
* Routes
* Student transport fee
* Student-to-bus assignment

This is a **console-based project** and does not use a database, GUI, or external frameworks.

## OOP Concepts Used

This project demonstrates the following Java concepts:

* Class and Object
* Constructors
* Constructor Overloading
* `this` keyword
* `super` keyword
* Encapsulation
* Inheritance
* Method Overloading
* Method Overriding
* Abstract Class
* Abstract Method
* Interface
* `implements`
* Upcasting
* Downcasting
* Dynamic Method Dispatch
* `static`
* `instanceof`
* Passing Objects as Method Parameters

## Project Structure

```text
DIUTransportManagement/
│
├── Person.java
├── Student.java
├── Driver.java
├── Transport.java
├── Bus.java
├── Route.java
├── Payable.java
├── TransportService.java
└── Main.java
```

## Class Relationship

```text
                    Person
                  (Abstract)
                   /      \
                  /        \
             Student      Driver
                |
             Payable
            (Interface)


                  Transport
                  (Abstract)
                      |
                     Bus


                  Route

                    |

            TransportService
```

## Class Description

### `Person.java`

An abstract parent class containing common information for people such as:

* Name
* Age

It also contains the abstract `showInfo()` method.

### `Student.java`

Extends the `Person` class and implements the `Payable` interface.

Contains:

* Student ID
* Department
* Transport fee payment

Also demonstrates constructor overloading and method overriding.

### `Driver.java`

Extends the `Person` class.

Contains:

* Driver ID
* License number

### `Transport.java`

An abstract parent class for transport vehicles.

Contains:

* Vehicle number
* Capacity
* Abstract `showTransportInfo()` method

Also demonstrates method overloading using the `start()` method.

### `Bus.java`

Extends `Transport`.

Contains:

* Bus type
* Bus information

### `Route.java`

Contains basic route information:

* Route name
* Starting point
* Destination

### `Payable.java`

An interface that defines:

```java
void payTransportFee();
```

The `Student` class implements this interface.

### `TransportService.java`

Handles basic transport operations such as:

* Adding students
* Adding buses
* Showing students
* Showing buses
* Assigning a student to a bus
* Showing total students

### `Main.java`

The main entry point of the application.

It creates objects and demonstrates the different Java OOP concepts.

##
