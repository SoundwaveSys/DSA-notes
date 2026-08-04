# Java Object-Oriented Programming (OOP) Notes

## Introduction

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of **Classes** and **Objects**. It helps write organized, reusable, modular, and maintainable code, making it essential for Data Structures and Algorithms (DSA).

---

# Classes and Objects

## Class
A **Class** is a blueprint or template for creating objects.

- Defines data (variables) and methods (functions)
- No memory is allocated until an object is created
- Everything in Java revolves around classes

### Example

```java
class Student {
    int age;
    void study() {
        System.out.println("Studying...");
    }
}
```

---

## Object

An **Object** is an instance of a class.

- Holds actual data
- Uses methods defined in the class
- Multiple objects are independent of each other

### Example

```java
Student s1 = new Student();
Student s2 = new Student();
```

---

# Access Specifiers

Access specifiers control visibility.

| Access Specifier | Accessible From |
|-----------------|-----------------|
| public | Anywhere |
| private | Same class only |
| protected | Same package + subclasses |
| Default | Same package |

---

# Main Method

The execution of every Java program starts from the **main()** method.

```java
class Basics {

    public static void main(String[] args) {

        System.out.println("Hello World");

    }

}
```

### Explanation

- **public** → Accessible everywhere
- **static** → JVM calls it without creating an object
- **void** → Returns nothing
- **String[] args** → Stores command-line arguments

---

# Static Methods

Static methods belong to the class instead of an object.

Call using:

```java
ClassName.methodName();
```

Example

```java
Math.sqrt(25);
```

---

# Creating Objects

```java
ClassName object = new ClassName();
```

Example

```java
class Test {

    int age;

    void assignAge(int num){

        age = num;

    }

}

public class Main{

    public static void main(String[] args){

        Test t1 = new Test();

        t1.assignAge(10);

        Test t2 = new Test();

        t2.assignAge(20);

        System.out.println(t1.age);

        System.out.println(t2.age);

    }

}
```

Output

```
10
20
```

Each object stores its own data independently.

---

# Method Arguments

Arguments are values passed into methods.

Example

```java
class Test{

    int sum(int a,int b){

        return a+b;

    }

}
```

Method Call

```java
Test obj = new Test();

int ans = obj.sum(10,15);
```

Output

```
25
```

---

# Constructors

A constructor initializes an object automatically.

## Rules

- Same name as class
- No return type
- Called automatically

---

## Default Constructor

```java
class Student{

    Student(){

        System.out.println("Object Created");

    }

}
```

---

## Parameterized Constructor

```java
class Student{

    int age;

    Student(int a){

        age=a;

    }

}
```

---

## Constructor Overloading

A class can have multiple constructors.

```java
Student(){}

Student(int age){}

Student(String name){}
```

---

# Encapsulation

Encapsulation means hiding data and allowing controlled access using methods.

Example

```java
class BankAccount{

    private int balance;

    public int getBalance(){

        return balance;

    }

    public void setBalance(int amount){

        balance=amount;

    }

}
```

Advantages

- Data security
- Controlled access
- Better maintainability

---

# Inheritance

Inheritance allows one class to acquire properties and methods of another class.

Parent → Superclass

Child → Subclass

Example

```java
class Vehicle{

    void honk(){

        System.out.println("Honk");

    }

}

class Car extends Vehicle{

}
```

Usage

```java
Car c = new Car();

c.honk();
```

Benefits

- Code reuse
- Easier maintenance
- Hierarchical design

---

# Polymorphism

Polymorphism means "Many Forms".

Two Types

## 1. Method Overloading

Same method name

Different parameters

```java
class Calculator{

    int sum(int a,int b){

        return a+b;

    }

    int sum(int a,int b,int c){

        return a+b+c;

    }

}
```

---

## 2. Method Overriding

Subclass changes parent method.

```java
class Vehicle{

    void honk(){

        System.out.println("Vehicle Honk");

    }

}

class Car extends Vehicle{

    @Override

    void honk(){

        System.out.println("Car Honk");

    }

}
```

---

# Abstraction

Abstraction hides implementation details and exposes only essential functionality.

Example

Driving a car without knowing how the engine works.

Java supports abstraction using:

- Abstract Classes
- Interfaces

---

# Abstract Class

Cannot create objects directly.

May contain

- Abstract methods
- Normal methods

Example

```java
abstract class Animal{

    abstract void sound();

    void sleep(){

        System.out.println("Sleeping");

    }

}

class Dog extends Animal{

    void sound(){

        System.out.println("Dog Barks");

    }

}
```

---

# Interface

Contains abstract methods (and default/static methods in Java 8+).

Used for complete abstraction.

Example

```java
interface Animal{

    void sound();

}

class Dog implements Animal{

    public void sound(){

        System.out.println("Dog Barks");

    }

}
```

Advantages

- Multiple inheritance
- Loose coupling
- Better flexibility

---

# OOP Pillars Summary

| Concept | Purpose |
|----------|---------|
| Class | Blueprint |
| Object | Instance of class |
| Encapsulation | Hide data |
| Inheritance | Code reuse |
| Polymorphism | One interface, many implementations |
| Abstraction | Hide complexity |

---

# Advantages of OOP

- Code Reusability
- Modularity
- Data Security
- Easy Maintenance
- Scalability
- Flexibility
- Better Software Design

---

# Quick Revision

- Class → Blueprint
- Object → Instance of class
- Constructor → Initializes object
- Static → Belongs to class
- Encapsulation → Data hiding
- Inheritance → Code reuse
- Polymorphism → One method, many behaviors
- Abstraction → Hide implementation
- Interface → Pure abstraction
- Abstract Class → Partial abstraction

---

# End of Notes
