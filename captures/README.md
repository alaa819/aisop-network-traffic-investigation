# Capture Handling

[CF-01 case file](../README.md)

**Status:** No capture has been collected for this project.

Raw packet captures can contain sensitive metadata and application data. Store originals in a private location outside the repository. The root `.gitignore` also excludes common capture formats as a secondary safeguard.

For each future capture, record the following in the case documentation:

| Field | Current value |
| --- | --- |
| Private capture filename | Pending |
| Collection source and authorized scope | Pending |
| Start and stop times with timezone | Pending |
| Host, interface, and tool version | Pending |
| Controlled activity performed | Pending |
| Capture filter and packet loss information | Pending |
| File size, packet count, and SHA-256 | Pending |
| Evidence references and redaction notes | Pending |

Retain an unmodified original and analyze a working copy. Record a SHA-256 hash after collection so subsequent integrity checks have a baseline. A hash demonstrates file consistency, not the truth or completeness of the captured traffic.

Publish reviewed screenshots only after inspecting metadata, packet details, payloads, and surrounding desktop content. Record redactions without disclosing the removed secrets. Never include credentials, cookies, authentication tokens, private keys, or TLS key logs.

If a sanitized capture is ever needed for sharing, create and validate a separate derivative and obtain explicit approval before publishing it. `.gitignore` rules do not sanitize files or remove previously committed content.
