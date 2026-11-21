# Use Cases

## Project Name
Workshop Registration System

## 1. Actors

### Student
The student can:
- View available workshops.
- Register for a workshop.
- Cancel an active registration.

### Education Administrator
The administrator can:
- Create and manage workshops.
- View workshop participants.
- View active registration counts.
- Cancel a student's registration.

## 2. Main Use Case: Register for Workshop

Use Case ID: UC-01

Primary Actor: Student

Goal: Register a student in an available workshop.

### Preconditions
- The workshop must exist.
- The workshop must have available capacity.
- The student must not already be registered in the workshop.

### Main Flow
1. The student views available workshops.
2. The student selects a workshop.
3. The system checks for duplicate registration.
4. The system checks workshop capacity.
5. The system records the registration date and time.
6. The system confirms successful registration.

### Alternative Flows
- If the student is already registered, the request is rejected.
- If the workshop is full, the request is rejected.
- The system displays an appropriate error message.

### Postconditions
- A new active registration is recorded.
- The available capacity decreases by one.

## 3. Main Use Case: Cancel Registration

Use Case ID: UC-02

Primary Actor: Student

Secondary Actor: Education Administrator

Goal: Cancel an active workshop registration.

### Preconditions
- The student must have an active registration.

### Main Flow
1. The student or administrator selects the registration.
2. The system checks the registration status.
3. The system changes the status to cancelled.
4. The system releases one workshop seat.
5. The system confirms successful cancellation.

### Alternative Flows
- If the registration is already cancelled, the request is rejected.
- If no active registration exists, the system displays an error message.

### Postconditions
- The registration is marked as cancelled.
- One seat becomes available.

## 4. Additional Use Cases

- Create Workshop
- View Available Workshops
- View Workshop Participants
- View Active Registration Count
- View Workshop Capacity

## 5. UML Use Case Diagram

The UML Use Case Diagram is provided
as a separate image in the project repository.

## 6. Project Team
Group C - Four Members
