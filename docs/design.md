# System Design

## Project Name
Workshop Registration System

## 1. System Overview
The system is designed to manage educational
workshops and student registrations.

## 2. Main Classes

### Student
Attributes:
- student_id
- name
- student_number

Methods:
- view_workshops()
- register_for_workshop()
- cancel_registration()

### Workshop
Attributes:
- workshop_id
- title
- instructor
- date
- total_capacity

Methods:
- create_workshop()
- check_capacity()
- view_participants()

### Registration
Attributes:
- registration_id
- registration_date
- status

Methods:
- create_registration()
- cancel_registration()
- check_status()

### EducationAdministrator
Attributes:
- administrator_id
- name

Methods:
- manage_workshops()
- view_participants()
- cancel_registration()

## 3. Class Relationships

- One Student can have multiple Registrations.
- One Workshop can have multiple Registrations.
- Each Registration belongs to one Student.
- Each Registration belongs to one Workshop.
- An EducationAdministrator can manage multiple Workshops.

## 4. Main Sequence: Workshop Registration

1. Student selects a workshop.
2. Student sends a registration request.
3. System checks for duplicate registration.
4. System checks available capacity.
5. If registration is valid, a new Registration is created.
6. Registration date and time are saved.
7. System confirms successful registration.

## 5. Error Handling

- Duplicate registration is rejected.
- Registration is rejected when capacity is full.
- An appropriate error message is displayed.

## 6. Design Rules

- Active registrations must not exceed workshop capacity.
- Cancelled registrations do not count as active.
- Each registration belongs to one student and one workshop.

## 7. UML Diagrams

The following diagrams must be added
as separate image files:

- Class Diagram
- Sequence Diagram for Workshop Registration

## 8. Project Team
Group C - Four Members
