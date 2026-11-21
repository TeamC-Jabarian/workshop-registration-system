# System Analysis

## Project Name
Workshop Registration System

## 1. Activity Diagram: Student Registration

### Main Process
1. Student views available workshops.
2. Student selects a workshop.
3. System checks if the student is already registered.
4. If duplicate registration exists, the request is rejected.
5. System checks workshop capacity.
6. If the workshop is full, the request is rejected.
7. System records the registration date and time.
8. System confirms successful registration.

### Activity Conditions
- Duplicate registration is not allowed.
- Registration is rejected when capacity is full.
- Successful registration decreases available capacity by one.

## 2. Activity Diagram: Registration Cancellation

### Main Process
1. Student or administrator selects a registration.
2. System checks registration status.
3. If registration is already cancelled, the request is rejected.
4. System changes registration status to cancelled.
5. System releases one workshop seat.
6. System confirms successful cancellation.

### Activity Conditions
- Only active registrations can be cancelled.
- Each cancellation releases exactly one seat.
- Repeated cancellation must not increase capacity again.

## 3. Conceptual Domain Model

### Main Classes

#### Student
- student_id
- name
- student_number

#### Workshop
- workshop_id
- title
- instructor
- date
- total_capacity

#### Registration
- registration_id
- registration_date
- status

#### Education Administrator
- administrator_id
- name

## 4. Relationships

- A student can have multiple registrations.
- A workshop can have multiple registrations.
- Each registration belongs to one student.
- Each registration belongs to one workshop.
- An administrator can manage multiple workshops.

## 5. Important Business Rules

- A student cannot register twice for the same workshop.
- Active registrations must not exceed workshop capacity.
- Cancelled registrations do not count as active registrations.
- Cancelling a registration releases one available seat.

## 6. Project Team
Group C - Four Members
