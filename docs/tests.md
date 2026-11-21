# Test Plan

## Project Name
Workshop Registration System

## 1. Testing Objectives

- Verify workshop creation.
- Verify student registration.
- Prevent duplicate registrations.
- Control workshop capacity.
- Verify registration cancellation.
- Check participant reports.

## 2. Test Cases

### TC-01: Create Workshop
Requirement: FR-01

Input:
- Title: Python Workshop
- Instructor: Ali
- Date: 2026-12-10
- Capacity: 20

Expected Result:
The workshop should be created successfully.

### TC-02: View Available Workshops
Requirement: FR-02

Action:
Student requests the list of workshops.

Expected Result:
The system should display available workshops.

### TC-03: Successful Registration
Requirement: FR-03

Precondition:
The workshop has available capacity.

Action:
A student registers for the workshop.

Expected Result:
Registration should be successful.

### TC-04: Record Registration Time
Requirement: FR-04

Action:
A student registers for a workshop.

Expected Result:
The registration date and time should be saved.

### TC-05: Duplicate Registration
Requirement: FR-05

Precondition:
The student is already registered in the workshop.

Action:
The same student attempts to register again.

Expected Result:
The request should be rejected.
The active registration count must not change.

### TC-06: Workshop Capacity Limit
Requirement: FR-06

Precondition:
The workshop capacity is 20 and has 20 active registrations.

Action:
A 21st student attempts to register.

Expected Result:
The request should be rejected.
The system should display "Workshop is full."
No new registration record should be created.

### TC-07: Registration After Cancellation
Requirement: FR-06, FR-07

Precondition:
The workshop is full and one student cancels their registration.

Action:
A new student attempts to register.

Expected Result:
The new registration should be successful.
The active registration count should remain within capacity.

### TC-08: Cancel Registration
Requirement: FR-07

Precondition:
The student has an active registration.

Action:
The student or administrator cancels the registration.

Expected Result:
The registration status should change to cancelled.
One seat should become available.

### TC-09: Repeated Cancellation
Requirement: FR-07

Precondition:
The registration is already cancelled.

Action:
The same registration is cancelled again.

Expected Result:
The request should be rejected.
The available capacity must not increase again.

### TC-10: View Participant Report
Requirement: FR-08

Action:
The administrator requests the participant list.

Expected Result:
The system should display the participants and the correct number of active registrations.

## 3. Boundary and Error Testing

The following cases are especially important:

- Registration when workshop capacity is exactly full.
- Duplicate registration by the same student.
- Registration after a cancellation.
- Repeated cancellation of the same registration.
- Registration when no available seats remain.

## 4. Test Environment

- Operating System: Windows
- Programming Language: Python 3
- Database: SQLite
- Testing Framework: pytest (if code is implemented)

## 5. Test Results

Test execution results will be recorded
after implementation or prototype testing.

## 6. Project Team

Group C - Four Members
