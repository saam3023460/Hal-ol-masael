Activity Diagrams — Problem Reporting System


Overview


This document describes the initial activity diagrams for the Problem Reporting System proposed by Team Halolmasayel.


The diagrams represent three main processes: problem reporting, report review and assignment, and report status tracking.


The target community has not been finalized yet. Therefore, the diagrams use the general role "User".


1. Problem Reporting and Handling


This diagram shows the process from submitting a problem report to reviewing it, assigning it for investigation, and recording the outcome.


flowchart TD
    A([Start]) --> B[User enters report information]
    B --> C{Is the information valid?}
    C -- No --> D[Show validation errors]
    D --> B
    C -- Yes --> E[Submit the report]
    E --> F[Create problem report]
    F --> G[Set status to SUBMITTED]
    G --> H[SupportAgent reviews the report]
    H --> I{Is the report acceptable?}
    I -- No --> J[Set status to REJECTED]
    J --> K[Record rejection reason]
    I -- Yes --> L[Determine report priority]
    L --> M{Is a FieldAgent needed?}
    M -- Yes --> N[Assign a FieldAgent]
    N --> O[Set status to ASSIGNED]
    O --> P[Record the outcome]
    M -- No --> Q[Keep the report under review]
    Q --> P
    K --> R([End])
    P --> R



2. Report Review and Assignment


This diagram focuses on the SupportAgent's review of a submitted problem, priority determination, and assignment to a FieldAgent when appropriate.


flowchart TD
    A([Start]) --> B[SupportAgent reviews the report]
    B --> C{Is the report acceptable?}
    C -- No --> D[Set status to REJECTED]
    D --> E[Record rejection reason]
    E --> J([End])
    C -- Yes --> F[Determine report priority]
    F --> G{Is a FieldAgent needed?}
    G -- Yes --> H[Assign a FieldAgent]
    H --> I[Set status to ASSIGNED]
    I --> K[Record the review result]
    G -- No --> L[Keep the report under review]
    L --> K
    K --> J



3. Problem Status Tracking


This diagram shows how a user searches for a report and views its current status and priority.


flowchart TD
    A([Start]) --> B[User searches for a report]
    B --> C{Is the report found?}
    C -- No --> D[Show report not found]
    D --> E([End])
    C -- Yes --> F[Display report status]
    F --> G[Display report priority]
    G --> H{Does the user want to view details?}
    H -- Yes --> I[Display report details]
    H -- No --> E
    I --> E



Assumptions and Open Questions


These diagrams represent an initial model and may be revised as the team clarifies the system requirements.


The rejection criteria, priority assignment rules, report closure process, and permissions for changing report status still need further discussion.


The diagrams are intended to remain consistent with the initial Class Diagram. Any changes to roles, statuses, or relationships should be reviewed with the team.


