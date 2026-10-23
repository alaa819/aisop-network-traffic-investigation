# CF-01 Investigation Workflow

[Case file](../../../README.md)

The primary [Investigation Workflow](../../../README.md#investigation-workflow) is now embedded directly in the root case-report README. This companion diagram describes the planned method, not completed activity or observed traffic.

```mermaid
flowchart TD
    A[Confirm authorization and lab scope] --> B[1. Select interface]
    B --> C[2. Capture controlled activity]
    C --> D[Preserve original capture privately]
    D --> E[3. Identify protocols and endpoints]
    E --> F[4. Review DNS]
    F --> G[5. Inspect TCP handshake]
    G --> H[6. Examine TCP header]
    H --> I[7. Follow TCP stream]
    I --> J{Evidence sufficient?}
    J -->|No| K[Record gaps and plan authorized follow-up]
    J -->|Yes| L[Write supported findings and limitations]
    K --> L
    L --> M[Review and redact public evidence copies]
    M --> N[Request approval before publishing]
```

Steps 1–7 map to the seven planned screenshot filenames in the [Evidence Collected](../../../README.md#evidence-collected). Any unobserved behavior must be documented as unavailable or inconclusive. Publication review must preserve the distinction between original private evidence and redacted public copies.
