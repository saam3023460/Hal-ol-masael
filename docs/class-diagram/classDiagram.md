
# Class Diagram — Problem Reporting System

## Overview

An initial domain model for a system that allows members
of a target community to report and track problems.

The target community is not finalized yet.

## Class Diagram

```mermaid
classDiagram
    class User {
        +UUID id
        +String fullName
        +String phoneNumber
        +String email
        +DateTime createdAt
    }

    class Problem {
        +UUID id
        +String title
        +String description
        +String location
        +DateTime reportedAt
        +ProblemStatus status
        +ProblemPriority priority
    }

    class SupportAgent {
        +UUID id
        +String fullName
        +String email
    }

    class FieldAgent {
        +UUID id
        +String fullName
        +String employeeCode
        +String specialization
    }

    class ProblemStatus {
        <<enumeration>>
        SUBMITTED
        UNDER_REVIEW
        ASSIGNED
        IN_PROGRESS
        RESOLVED
        REJECTED
        CLOSED
    }

    class ProblemPriority {
        <<enumeration>>
        LOW
        MEDIUM
        HIGH
        CRITICAL
    }

    User "1" --> "0..*" Problem : reports
    SupportAgent "1" --> "0..*" Problem : reviews
    FieldAgent "0..1" --> "0..*" Problem : handles
    Problem --> ProblemStatus : has
    Problem --> ProblemPriority : has
```

## Open Questions

- Who is the target user community?
- Can a problem have multiple field agents?
- Can a problem be reassigned?
- Are problem categories required?
- Is location mandatory for every problem?
- Can users comment on or reopen a problem?
- Should support agents and field agents share a common base class?
