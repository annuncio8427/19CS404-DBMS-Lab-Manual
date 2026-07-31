# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
<img width="1536" height="1024" alt="er1" src="https://github.com/user-attachments/assets/2e27a507-50e3-4e01-9cc5-93769e6d1d36" />


# City Fitness Club Management – ER Model Documentation

## Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|----------------------|-------|
| **Member** | **MemberID (PK)**, Name, MembershipType, StartDate | Stores registered gym members. |
| **Program** | **ProgramID (PK)**, ProgramName, Description, Duration | Fitness programs such as Yoga, Zumba, Weight Training. |
| **Trainer** | **TrainerID (PK)**, Name, Specialization, Phone | Trainers assigned to one or more programs. |
| **Member_Program** | **MemberID (PK, FK)**, **ProgramID (PK, FK)**, JoinDate | Associative entity for Member–Program relationship. |
| **Session_Booking** | **BookingID (PK)**, MemberID (FK), TrainerID (FK), SessionDate, SessionTime | Records personal training bookings. |
| **Attendance** | **AttendanceID (PK)**, BookingID (FK), AttendanceStatus | Stores attendance for each booked session. |
| **Payment** | **PaymentID (PK)**, MemberID (FK), BookingID (FK), Amount, PaymentDate, PaymentType | Records membership and session payments. |

---

## Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|-------------|-------------|---------------|-------|
| Member **enrolls in** Program | M : N | Total (Member), Partial (Program) | A member can enroll in multiple programs; each program has many members. |
| Program **assigned to** Trainer | M : N | Total (Program), Partial (Trainer) | A program may have multiple trainers; a trainer can teach multiple programs. |
| Member **books** Session_Booking | 1 : N | Total (Session), Partial (Member) | One member can book many personal training sessions. |
| Trainer **conducts** Session_Booking | 1 : N | Total (Session), Partial (Trainer) | One trainer can conduct many personal training sessions. |
| Session_Booking **has** Attendance | 1 : 1 | Total (Both) | Every booked session has one attendance record. |
| Member **makes** Payment | 1 : N | Total (Payment), Partial (Member) | A member can make multiple payments. |
| Session_Booking **may generate** Payment | 1 : 1 | Partial | Session payment is linked to a booking when applicable. |

---

## Assumptions

- Every member has a unique **MemberID**.
- Every trainer has a unique **TrainerID**.
- Every fitness program has a unique **ProgramID**.
- Members can enroll in multiple fitness programs.
- A fitness program may have one or more trainers.
- Personal training sessions are booked by exactly one member with one trainer.
- Attendance is recorded for every booked session.
- Payments can be for either **Membership** or **Personal Training Session**.
- Membership types (Basic, Premium, Elite, etc.) are predefined.
- A booking cannot exist without both a valid member and a valid trainer.
- Only active members can enroll in programs and book training sessions.
---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_library.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_restaurant.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
