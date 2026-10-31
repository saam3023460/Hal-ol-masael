# Software Requirements Specification (SRS)
## Hal Ol Masael

**Team Name:** Bisahab

**Team Members:**
- Saam Shahrouzi
- Zahra Yaghoubi
- Sajad Davoodabadi

---

## 1. Introduction

### 1.1 Purpose

The purpose of this document is to define the functional and non-functional requirements of Hal Ol Masael, a 137-like issue-reporting and management system. This document serves as a reference for the development, testing, and evaluation of the system.

### 1.2 Scope

Hal Ol Masael is a platform that enables members of a target community to report problems and follow their resolution progress. The system allows responsible authorities or administrators to review, categorize, prioritize, and manage reported issues.

The system aims to improve communication between community members and responsible organizations, making issue resolution more organized, transparent, and efficient.

### 1.3 Definitions

- **Issue:** A problem reported by a member of the target community.
- **User:** A person who uses the system to report or track issues.
- **Administrator:** A person responsible for managing users, categories, and system operations.
- **Responsible Authority:** A person or team assigned to handle and resolve reported issues.

## 2. Overall Description

### 2.1 Product Perspective

Hal Ol Masael is a centralized issue-reporting system that connects community members with the authorities responsible for addressing their problems.

### 2.2 User Classes

- **Community Member:** Reports issues and tracks their status.
- **Responsible Authority:** Reviews assigned issues, updates their status, and records resolution details.
- **Administrator:** Manages users, issue categories, and system-wide settings.

### 2.3 Operating Environment

The system is intended to be accessible through a web-based interface using a modern web browser. It requires a server-side application and a database for storing users, reports, and related information.

## 3. Functional Requirements

### FR-1: User Registration and Authentication

The system shall allow users to register and log in to their accounts.

### FR-2: Issue Reporting

The system shall allow authenticated users to submit issues with a title, description, category, and relevant location or other identifying information when applicable.

### FR-3: Issue Categorization

The system shall organize reported issues into categories to facilitate filtering and assignment.

### FR-4: Issue Tracking

The system shall allow users to view their submitted issues and check their current status.

### FR-5: Issue Status Management

The system shall allow authorized personnel to update issue statuses, such as:
- Submitted
- Under Review
- In Progress
- Resolved
- Rejected

### FR-6: Issue Assignment

The system shall allow administrators or authorized personnel to assign issues to the appropriate responsible authority or team.

### FR-7: Issue Prioritization

The system shall allow authorized personnel to assign priorities to issues based on their urgency or importance.

### FR-8: Issue Resolution

The system shall allow responsible personnel to record resolution details when an issue is resolved.

### FR-9: Issue Search and Filtering

The system shall allow users to search for and filter issues based on available criteria, such as category, status, or priority.

### FR-10: Notifications

The system should notify users when significant changes occur to their reported issues, such as assignment, status updates, or resolution.

### FR-11: User Management

The system shall allow administrators to manage user accounts and assign appropriate roles and permissions.

## 4. Non-Functional Requirements

### NFR-1: Usability

The system shall provide a simple and understandable interface that users can navigate without specialized technical knowledge.

### NFR-2: Security

The system shall protect user information and prevent unauthorized access to restricted functions and data.

### NFR-3: Performance

The system should respond to ordinary user actions within a reasonable time under normal operating conditions.

### NFR-4: Reliability

The system shall preserve submitted issue information and maintain data consistency during normal operation.

### NFR-5: Maintainability

The system should be organized into understandable components to facilitate future maintenance and development.

### NFR-6: Accessibility

The system should be usable across common screen sizes and support accessibility best practices.

## 5. Data Requirements

The system shall store and manage the following information:

- **User:** User ID, name, contact information, authentication data, and role.
- **Issue:** Issue ID, title, description, category, location when applicable, submission date, status, and priority.
- **Assignment:** Issue ID, responsible authority or team, assignment date, and assignment details.
- **Resolution:** Issue ID, resolution description, and resolution date.
- **Notification:** Recipient, related issue, notification content, and creation date.

## 6. Use Case Summary

| Actor | Use Cases |
|---|---|
| Community Member | Register, log in, submit an issue, view submitted issues, track status |
| Responsible Authority | View assigned issues, update status, record resolution details |
| Administrator | Manage users, manage categories, assign issues, manage priorities |

## 7. Constraints and Assumptions

- Users require access to the system through a supported web browser.
- Certain operations, such as assigning issues or managing users, require appropriate permissions.
- Issue resolution depends on the availability and actions of the responsible authorities.
- The exact categories and assignment rules may vary depending on the target community.
- The system does not guarantee that every reported issue will be resolved; it provides tools for organizing and tracking the resolution process.

## 8. Future Enhancements

Possible future enhancements include:
- File and image attachments for issue reports.
- Maps and location-based issue reporting.
- Comments and communication between users and responsible authorities.
- Statistical dashboards and reports.
- Duplicate issue detection.
- Public visibility for selected issues and their resolution progress.

---

