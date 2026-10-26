Activity Diagrams — Problem Reporting System


Overview


This document presents three initial activity diagrams for the Problem Reporting System proposed by Team Halolmasayel.


The diagrams describe problem reporting and handling, report review and assignment, and problem status tracking.


The target community has not been finalized yet. Therefore, the diagrams use the general role User.


1. Problem Reporting and Handling


This diagram shows the initial process of submitting and handling a problem report.


flowchart TD
    A([Start]) --> B[User enters report information]
    B --> C{Is the information valid?}
    C -- No --> D[Show validation errors]
    D --> B
    C -- Yes --> E[Submit the report]
    E --> F[Create problem report]
    F --> G[Set status to SUBMITTED]
    G --> H([End])



2. Report Review and Assignment


This diagram focuses on the SupportAgent's review of a submitted problem, priority determination, and assignment to a FieldAgent when appropriate.


flowchart TD
    A([Start]) --> B[SupportAgent reviews the report]
    B --> C{Is the report acceptable?}
    C -- No --> D[Set status to REJECTED]
    D --> E[Record the review result]
    C -- Yes --> F[Determine report priority]
    F --> G{Is a FieldAgent needed?}
    G -- Yes --> H[Assign a FieldAgent]
    H --> I[Set status to ASSIGNED]
    G -- No --> J[Keep the report under review]
    I --> K[Record the review result]
    J --> K
    E --> L([End])
    K --> L



3. Problem Status Tracking


This diagram shows how a user searches for a report and views its current status and priority.


flowchart TD
    A([Start]) --> B[User searches for a report]
    B --> C{Is the report found?}
    C -- No --> D[Show report not found]
    D --> E([End])
    C -- Yes --> F[Display report status]
    F --> G[Display report priority]
    G --> E



Assumptions and Open Questions


These diagrams represent an initial model and may be revised as the team clarifies the system requirements.


The rejection criteria, priority assignment rules, report closure process, and permissions for changing report status still need further discussion.


The diagrams are intended to remain consistent with the initial Class Diagram. Any changes to roles, statuses, or relationships should be reviewed with the team.

