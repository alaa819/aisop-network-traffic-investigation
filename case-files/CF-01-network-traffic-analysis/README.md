# CF-01 — Network Traffic Analysis

[Project overview](../../README.md) · [Workflow](diagrams/investigation-flow.md) · [Capture handling](../../captures/README.md)

## Case metadata

| Field | Value |
| --- | --- |
| Case ID | CF-01 |
| Project | AISOP — Phase 6 |
| Investigation type | Planned, authorized lab traffic review |
| Analyst | Pending confirmation |
| Status | Prepared — capture and analysis pending |
| Alert source | Planned training exercise; no alert supplied |
| Severity | Pending assessment |
| Capture date, time, and timezone | Pending |
| Authorized host and scope | Pending confirmation before capture |
| Operating system and Wireshark version | Pending verification |
| Capture interface | Pending selection |
| Capture duration and packet count | Pending |
| Capture filename and SHA-256 | Pending; original retained privately |
| Final disposition | Pending evidence review |

## Objective and scope

Practice selecting an interface, collecting a short authorized capture, identifying protocols and endpoints, examining DNS and TCP behavior, and producing an evidence-backed assessment. This is a documentation scaffold, not a completed investigation or an incident verdict.

The capture must be limited to an approved lab host and activity. Record the capture vantage point, any capture filter, capture start and stop times, timezone, and any dropped-packet indication. Note visibility gaps before drawing conclusions.

## Evidence register

All entries below are **planned placeholders**. No PNG files exist yet; `evidence/.gitkeep` preserves the empty folder. Add images and relative Markdown embeds only after collection and privacy review.

| Step | Planned filename in `evidence/` | Purpose | Status |
| --- | --- | --- | --- |
| 1 | `01-wireshark-interfaces.png` | Interface selection | Pending |
| 2 | `02-live-packet-capture.png` | Capture activity and context | Pending |
| 3 | `03-protocol-identification.png` | Protocols and endpoints | Pending |
| 4 | `04-dns-traffic-filter.png` | DNS exchanges | Pending |
| 5 | `05-tcp-handshake.png` | Connection establishment | Pending |
| 6 | `06-tcp-header-analysis.png` | TCP field inspection | Pending |
| 7 | `07-follow-tcp-stream.png` | One conversation in context | Pending |

## Seven evidence steps

### 1. Select the capture interface

Review available interfaces and identify the one associated with the authorized lab traffic. Record the selection and rationale, including any VPN or virtual adapter that affects visibility.

**Evidence:** `01-wireshark-interfaces.png` · **Observation:** Pending.

### 2. Collect a short live capture

Start capture only after scope approval. Generate a small amount of deliberate lab activity, record what was done and when, then stop and preserve the capture. Record duration, packet count, capture filters, and any packet loss information.

**Evidence:** `02-live-packet-capture.png` · **Observation:** Pending.

### 3. Identify protocols and endpoints

Review the Source, Destination, Protocol, and Info columns. Record only protocols and endpoints actually present, with representative packet numbers and timestamps. Distinguish lab activity from unrelated background activity where the evidence permits.

**Evidence:** `03-protocol-identification.png` · **Observation:** Pending.

### 4. Examine DNS traffic

Apply the display filter `dns`. If available, pair a query and response using transaction details and endpoints; record query type, response code, and returned records. Absence of visible DNS does not establish absence of name resolution: caching or encrypted DNS may limit visibility. Document an unavailable result honestly and plan another authorized sample if needed.

**Evidence:** `04-dns-traffic-filter.png` · **Observation:** Pending.

### 5. Inspect a TCP handshake

Apply `tcp`, select a connection, and isolate its actual stream index using `tcp.stream eq N`, replacing `N` with the observed numeric index. Locate SYN, SYN-ACK, and ACK packets in that same connection and record packet numbers, endpoint ports, and relative sequence behavior. If the capture began after establishment or packets are missing, state that the handshake was not fully observed.

**Evidence:** `05-tcp-handshake.png` · **Observation:** Pending.

### 6. Examine a TCP header

Expand the TCP details for a selected packet. Record ports, flags, sequence and acknowledgment values, window information, and segment length. State whether sequence numbers are relative. Interpret fields in the surrounding stream context; one flag or port alone does not determine whether activity is malicious.

**Evidence:** `06-tcp-header-analysis.png` · **Observation:** Pending.

### 7. Follow a TCP stream

Use Follow TCP Stream for the selected connection. Record the actual stream index, endpoints, direction, and visible content or encryption limitations. TCP reassembly does not decrypt TLS. Avoid claiming application content that is not visible, and review payloads carefully before publishing the screenshot.

**Evidence:** `07-follow-tcp-stream.png` · **Observation:** Pending.

## Findings and indicator register

| Investigation question | Finding | Evidence reference |
| --- | --- | --- |
| Which host and interface were captured? | Pending | Pending |
| Which protocols and endpoints appeared? | Pending | Pending |
| What DNS behavior was visible? | Pending | Pending |
| Was a complete TCP handshake observed? | Pending | Pending |
| What did the TCP headers show? | Pending | Pending |
| What could be established from the stream? | Pending | Pending |
| Were there behaviors needing further investigation? | Pending | Pending |

No IP addresses, domains, packet numbers, counts, or traffic classifications have been assigned. After capture, record indicators with packet references and describe public redactions. An address or recognizable service name alone is insufficient to establish benign or malicious behavior.

## Assessment and limitations

**Assessment:** Pending actual capture and analysis.

**Final disposition:** Pending. The case remains open for evidence collection; no claim of normal traffic or absence of compromise is made.

Document capture duration, vantage point, encryption, caching, missing packets, background traffic, and any other limits that apply. A short capture supports conclusions about the reviewed sample, not the entire host or network.

## Evidence handling and publication

- Preserve the original capture and screenshots privately; record provenance, capture hash, and evidence timestamps.
- Create separate reviewed copies for publication. Record redactions in each caption and retain packet references where possible.
- Inspect addresses, hostnames, account details, browser tabs, payloads, tokens, and desktop identifiers. Do not publish decryption keys or session secrets.
- Keep raw captures out of Git by default. Review the complete staged file list before committing.
- If evidence is absent or inconclusive, report that limitation and leave the corresponding finding pending.

## Completion checklist

- [ ] Confirm authorization, host, interface, and controlled activity.
- [ ] Record environment, capture window, provenance, and SHA-256.
- [ ] Collect seven real screenshots or document unavailable evidence.
- [ ] Add reviewed images with captions and packet references.
- [ ] Replace pending findings with supported observations.
- [ ] Record limitations and an evidence-backed disposition.
- [ ] Review staged content and obtain approval before external publication.
