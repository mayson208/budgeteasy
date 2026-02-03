BudgetEasy 💸

A modern envelope-based budgeting API built with Java & Spring Boot

BudgetEasy is a backend service that implements the classic envelope budgeting system: money is allocated into envelopes (categories), and transactions move money between them in a safe, rule-driven way.

This project is intentionally designed with clean architecture and domain-driven design (DDD) principles to showcase strong backend fundamentals.

🚀 Tech Stack

Java 17

Spring Boot 3

Maven (multi-module)

JUnit 5

(Planned) PostgreSQL, Flyway, Spring Data JPA

🧱 Architecture

This is a multi-module Maven project:

envelope-finance-tracker
├── core-domain
│   ├── model        # Entities (Envelope, Transaction, Category)
│   ├── valueobject  # Immutable value objects (Money)
│   └── exception    # Domain-specific exceptions
│
├── application
│   └── (use cases / services – coming next)
│
├── api
│   ├── controller   # REST controllers
│   └── BudgetEasyApplication.java
│
└── pom.xml          # Parent Maven configuration