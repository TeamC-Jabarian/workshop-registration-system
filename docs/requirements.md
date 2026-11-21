# System Requirements

## Project Name
Workshop Registration System

## 1. Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | The system shall allow the administrator to create workshops with title, instructor, date, and capacity. | Must |
| FR-02 | The system shall display the list of available workshops. | Must |
| FR-03 | The system shall allow students to register for a workshop. | Must |
| FR-04 | The system shall record the registration date and time. | Must |
| FR-05 | The system shall prevent duplicate registrations by the same student in the same workshop. | Must |
| FR-06 | The system shall prevent registrations when workshop capacity is full. | Must |
| FR-07 | The system shall allow students or the administrator to cancel a registration. | Must |
| FR-08 | The system shall display the list of participants and active registration count for each workshop. | Must |

## 2. Non-Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| NFR-01 | The system shall respond to normal operations within 2 seconds under the agreed test conditions. | Should |
| NFR-02 | The system shall correctly preserve registration records after the application is restarted in all persistence tests. | Must |
| NFR-03 | The system shall validate all registration requests before saving them to prevent invalid or duplicate records. | Must |

## 3. MoSCoW Prioritization

- Must: Essential requirements that must be implemented.
- Should: Important requirements that should be implemented.
- Could: Optional features that may be implemented.
- Won't: Features excluded from the current project scope.

## 4. Acceptance Criteria

### AC-01: Workshop Capacity
If a workshop has a capacity of 20 students and already has 20 active registrations, the 21st registration must be rejected.

The system must display:
"Workshop is full."

After one registration is cancelled, a new registration must be accepted.

### AC-02: Duplicate Registration
If a student is already registered in a workshop, another registration request by the same student for the same workshop must be rejected.

The number of active registrations must not change.

### AC-03: Registration Cancellation
When a student or administrator cancels an active registration, the registration status must change to cancelled and one seat must become available.

A cancelled registration must not be cancelled again.

### AC-04: Workshop Participant Report
The system must display the participants of each workshop and the number of active registrations.

The displayed count must match the actual active registrations.

## 5. Project Scope

The system includes:
- Workshop management.
- Student registration.
- Duplicate registration prevention.
- Capacity control.
- Registration cancellation.
- Participant reporting.

The following features are outside the project scope:
- Tuition payment.
- SMS and email notifications.
- Certificate generation.
- Multi-branch management.

## 6. Project Team
Group C - Four Members
