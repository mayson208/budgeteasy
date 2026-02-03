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

💡 Core Concepts
Envelope

Represents a bucket of money (e.g. Groceries, Rent, Entertainment).

Money (Value Object)

Immutable

Currency-safe

Uses BigDecimal with enforced scale

Prevents invalid arithmetic (currency mismatches, negatives, etc.)

Transaction Types

INCOME – adds money to an envelope

EXPENSE – removes money from an envelope

TRANSFER – moves money between envelopes

All rules are enforced at the domain level.

▶️ Running the Project
Build everything
mvn clean test

Run the API
mvn -pl api spring-boot:run


The server will start on:

http://localhost:8080

🛠️ Current Status

✅ Multi-module Maven setup
✅ Spring Boot API module
✅ Domain model (Money, Envelope, Transaction, Category)
✅ Health endpoint

🗺️ Roadmap

 Application-layer use cases

 In-memory repositories

 REST endpoints for envelopes & transactions

 Persistence with PostgreSQL + Flyway

 Authentication

 Frontend or mobile client

🎯 Goals of This Project

Demonstrate real-world backend architecture

Practice DDD and clean separation of concerns

Serve as a strong portfolio project

Be extendable into a full personal finance app

🧠 Author

Built by Mason
GitHub: https://github.com/mayson208