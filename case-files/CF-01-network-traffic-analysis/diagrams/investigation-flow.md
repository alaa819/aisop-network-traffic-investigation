# CF-01 Investigation Workflow

[Case report](../../../README.md#investigation-workflow)

This mirrors the workflow embedded in the root case report. The handshake and followed stream are separate connections.

```mermaid
flowchart TD
    A[Review interfaces and Wi-Fi capture context] --> B[Review captured packet list]
    B --> C[Identify protocols and endpoints]
    C --> D[Filter and examine DNS]
    D --> E[Inspect handshake in packets 163, 165, 166]
    E --> F[Inspect TCP header in packet 232]
    F --> G[Follow separate TCP stream 13]
    G --> H[Document findings and evidence limits]
    H --> I[Collect missing capture metadata]
```
