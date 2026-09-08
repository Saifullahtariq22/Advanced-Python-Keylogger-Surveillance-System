# System Architecture

## 1. Overview

The project consists of several functional components that work together to demonstrate endpoint information collection and processing.

## 2. High-Level Architecture

```text
┌──────────────────────────────┐
│       Windows Endpoint       │
│                              │
│  ┌────────────────────────┐  │
│  │ Keyboard Monitoring    │  │
│  └───────────┬────────────┘  │
│              │               │
│  ┌───────────▼────────────┐  │
│  │ System Information     │  │
│  └───────────┬────────────┘  │
│              │               │
│  ┌───────────▼────────────┐  │
│  │ Clipboard Collection   │  │
│  └───────────┬────────────┘  │
│              │               │
│  ┌───────────▼────────────┐  │
│  │ Screenshot Capture     │  │
│  └───────────┬────────────┘  │
│              │               │
│              ▼               │
│       Local Data Files       │
│              │               │
│              ▼               │
│           Encryption         │
│              │               │
│              ▼               │
│        Transmission          │
│              │               │
│              ▼               │
│           Cleanup            │
└──────────────────────────────┘
```

---

## 3. Data Flow

### Stage 1 — Collection

Different components demonstrate collection of endpoint information.

```text
Keyboard
Clipboard
System Information
Screenshot
     │
     ▼
Data Collection Layer
```

### Stage 2 — Storage

The collected test data is temporarily stored in local files.

```text
Collection Layer
      ↓
Local Files
```

### Stage 3 — Encryption

Selected files can be encrypted using Fernet symmetric encryption.

```text
Local File
    ↓
Fernet
    ↓
Encrypted File
```

### Stage 4 — Transmission

The project demonstrates transmission of generated files to an authorized destination.

```text
Encrypted Data
      ↓
Transmission Mechanism
      ↓
Authorized Test Destination
```

### Stage 5 — Cleanup

Temporary files may be removed after the experiment.

```text
Temporary Files
      ↓
Cleanup
      ↓
Removed Artifacts
```

---

## 4. Component Relationships

| Component          | Responsibility                         |
| ------------------ | -------------------------------------- |
| Keyboard Monitor   | Demonstrates keyboard-event collection |
| System Collector   | Collects system/network information    |
| Clipboard Module   | Demonstrates clipboard access          |
| Screenshot Module  | Captures test-environment screen       |
| Storage Layer      | Stores generated files                 |
| Encryption Layer   | Encrypts selected files                |
| Transmission Layer | Demonstrates file transfer             |
| Cleanup Layer      | Removes temporary artifacts            |

---

## 5. Security Perspective

From a defensive perspective, each stage can produce observable behavior.

```text
Collection
    ↓
Process Activity
    ↓
File Activity
    ↓
Encryption Activity
    ↓
Network Activity
    ↓
Potential Security Alert
```

These behaviors can be useful when studying endpoint monitoring and malware detection.
