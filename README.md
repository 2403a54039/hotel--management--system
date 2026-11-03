# hotel--management--system


# HOTEL MANAGEMENT SYSTEM

## Objective
To develop a Hotel Management System that manages room reservations, customer check-in, check-out and billing.

## 1. Room Reservation UML Diagram

```mermaid
sequenceDiagram
    actor Customer
    participant Receptionist
    participant System
    participant Room
    Customer->>Receptionist: Request room booking
    Receptionist->>System: Enter customer details
    System->>Room: Check availability
    Room-->>System: Room available
    System-->>Customer: Display available rooms
    Customer->>Receptionist: Select room
    Receptionist->>System: Confirm reservation
    System-->>Customer: Booking confirmed
```

## 2. Customer Check-in UML Diagram

```mermaid
sequenceDiagram
    actor Customer
    participant Receptionist
    participant System
    participant Room
    Customer->>Receptionist: Request check-in
    Receptionist->>System: Verify reservation
    System-->>Receptionist: Reservation verified
    Receptionist->>Customer: Request ID proof
    Customer-->>Receptionist: Provide ID proof
    Receptionist->>System: Confirm check-in
    System->>Room: Update room status
    System-->>Customer: Check-in successful
```

## 3. Customer Check-out UML Diagram

```mermaid
sequenceDiagram
    actor Customer
    participant Receptionist
    participant System
    participant Room
    Customer->>Receptionist: Request check-out
    Receptionist->>System: Retrieve booking details
    System-->>Receptionist: Display stay details
    Receptionist->>System: Calculate final charges
    System-->>Customer: Display total bill
    Customer->>Receptionist: Make payment
    Receptionist->>System: Confirm payment
    System->>Room: Update status to Cleaning
    System-->>Customer: Check-out successful
```

## 4. Billing UML Diagram

```mermaid
sequenceDiagram
    actor Customer
    participant Receptionist
    participant Billing
    participant Payment
    Customer->>Receptionist: Request bill
    Receptionist->>Billing: Generate bill
    Billing->>Billing: Calculate room charges
    Billing->>Billing: Add service charges
    Billing->>Billing: Calculate taxes
    Billing-->>Customer: Display final bill
    Customer->>Payment: Make payment
    Payment-->>Billing: Payment successful
    Billing->>Billing: Generate receipt
    Billing-->>Customer: Provide receipt
```

## Conclusion
The Hotel Management System simplifies room reservations, check-in, check-out and billing. UML diagrams represent the interactions between customers, receptionists and the system.
