Perfect — let’s switch gears and make this **JavaScript (ES6 Classes)**.
Here’s a clean README with the **JS code implementation**:

---

# Person Class Inheritance Example (JavaScript)

## 📌 Overview

This project demonstrates **Object-Oriented Programming (OOP)** in JavaScript using **classes, inheritance, and method overriding**.

We define a base `Person` class with common properties and extend it into two subclasses:

* `Student` → Adds a `grade` property.
* `Teacher` → Adds a `subject` property.

Each subclass **overrides** the method to display complete details.

---

## 📂 Class Structure

1. **Person Class**

   * Properties: `name`, `age`
   * Method: `displayInfo()` → shows basic person info.

2. **Student Class (extends Person)**

   * Additional Property: `grade`
   * Method: `displayInfo()` → overrides parent method to include student details.

3. **Teacher Class (extends Person)**

   * Additional Property: `subject`
   * Method: `displayInfo()` → overrides parent method to include teacher details.

---

## 🧩 Example Code (JavaScript)

```javascript
// Base Person class
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  displayInfo() {
    console.log(`Name: ${this.name}, Age: ${this.age}`);
  }
}

// Student class extending Person
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age);
    this.grade = grade;
  }

  displayInfo() {
    super.displayInfo();
    console.log(`Grade: ${this.grade}`);
  }
}

// Teacher class extending Person
class Teacher extends Person {
  constructor(name, age, subject) {
    super(name, age);
    this.subject = subject;
  }

  displayInfo() {
    super.displayInfo();
    console.log(`Subject: ${this.subject}`);
  }
}

// Demonstration
const student = new Student("Alice", 20, "A");
const teacher = new Teacher("Mr. Smith", 40, "Mathematics");

console.log("=== Student Info ===");
student.displayInfo();

console.log("\n=== Teacher Info ===");
teacher.displayInfo();
```

---

## 🚀 Output Example

```
=== Student Info ===
Name: Alice, Age: 20
Grade: A

=== Teacher Info ===
Name: Mr. Smith, Age: 40
Subject: Mathematics
```

---

## 🎯 Key Learning Points

* **Inheritance (`extends`)** lets subclasses reuse properties/methods from the parent.
* **`super()`** is used to call the parent constructor and methods.
* **Method overriding** customizes behavior for each subclass.

---
