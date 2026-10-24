# Capture Handling

[CF-01 case report](../README.md)

Seven user-supplied screenshots have been added to the evidence folder. The original raw capture has not been supplied to this repository or independently reviewed. No raw capture is published.

| Field | Evidence / status |
|---|---|
| Collection source | User-supplied Wireshark screenshots from a home-lab exercise |
| Local IPv4 endpoint | `192.168.1.60` |
| Interface | Wi-Fi, shown in capture window titles |
| Tool version | Wireshark 4.6.0, shown in welcome screenshot |
| Operating system/version | Not verified from supplied images |
| Capture start/stop, date, timezone, duration | Not established by supplied screenshots |
| Controlled activity | Not established; do not assume earlier suggested commands were run |
| Capture filter | Not established; `dns`, `tcp`, and `tcp.stream eq 13` are display filters |
| Packet count | 260 in visible status bars |
| Dropped packets | Status bars report 0 (0.0%); this does not establish complete session visibility |
| Original capture filename, size, SHA-256 | Not verified; no original capture supplied |
| Screenshot handling | Seven originals copied unchanged; local paths and network identifiers remain visible |

Keep the original capture privately outside the repository and record its actual filename, collection times, and SHA-256 when available. Hashing a screenshot does not substitute for hashing the original capture. Preserve original evidence and analyze working copies.

Raw captures and session secrets are excluded by the root `.gitignore`. Review staged files before committing: ignore rules do not sanitize files or remove previously tracked data. Any future public derivative should be separately reviewed for credentials, tokens, payloads, and identifying information.
