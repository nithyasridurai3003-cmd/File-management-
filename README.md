# TradeFileManagementSystem – API & Model Modules

This repository contains the **API layer and Model layer** of the Trade File Management System.

The project is part of a **Spring Boot multi-module backend application** used to manage trade file uploads, process trade records, and track trade errors.

---

## Tech Stack

* Java 21
* Spring Boot
* Maven
* Spring Data JPA

---

## API Layer

The **API layer** exposes REST endpoints that allow external clients to interact with the system.

The API is implemented using **Spring Boot REST Controllers**.

### Example APIs

```
POST /api/trades/upload
GET /api/trades
GET /api/trades/{id}
GET /api/errors
```

### Responsibilities

* Accept HTTP requests from clients
* Trigger backend business logic
* Return responses to the client
* Provide endpoints for trade file processing

Example Controller:

```
TradeController.java
```

---

## Model Layer

The **Model layer** defines the core data structures used in the system.

These models represent database tables and are used throughout the application.

### Entities

* **FileLoad**
  Stores information about uploaded trade files.

* **TradeRecord**
  Stores individual trade details extracted from uploaded files.

* **TradeError**
  Stores validation errors that occur during trade processing.

### DTO

* **TradeDTO**
  Used for transferring trade data between layers of the application.

---

## Project Structure

```
TradeFileManagementSystem
│
├── model
│   └── src/main/java/com/trade/model
│       ├── entity
│       │   ├── FileLoad.java
│       │   ├── TradeRecord.java
│       │   └── TradeError.java
│       │
│       └── dto
│           └── TradeDTO.java
│
└── controller
    └── src/main/java/com/trade/controller
        └── TradeController.java
```

---

## Purpose of This Repository

This repository isolates the **API and Model modules** from the full backend system to demonstrate:

* API endpoint design
* Data model structure
* Backend interface for trade management operations
