# Technical Documentation

## 1. Introduction

The Advanced Python Keylogger & Surveillance System is a Python-based cybersecurity research project designed to demonstrate several techniques associated with endpoint information collection.

The project was developed for educational purposes and authorized laboratory experimentation.

---

## 2. Objectives

The primary objectives are:

1. Understand keyboard event monitoring.
2. Study endpoint information collection.
3. Demonstrate clipboard access.
4. Demonstrate programmatic screenshot capture.
5. Understand local data storage.
6. Demonstrate symmetric encryption.
7. Understand automated file transmission.
8. Study the security and privacy implications of surveillance software.

---

## 3. Technologies

| Technology   | Purpose                   |
| ------------ | ------------------------- |
| Python       | Main programming language |
| pynput       | Keyboard event handling   |
| PyWin32      | Windows API interaction   |
| Pillow       | Screenshot functionality  |
| Requests     | HTTP requests             |
| Cryptography | File encryption           |
| SoundDevice  | Audio functionality       |
| SciPy        | Audio file processing     |
| SMTP         | Email/file transmission   |

---

## 4. Main Components

### 4.1 Configuration

The configuration section defines parameters used throughout the program.

Examples include:

* Output location
* Collection duration
* Number of iterations
* Encryption key
* Authorized transmission destination

Sensitive credentials should never be hard-coded into the source code.

---

### 4.2 System Information Collection

The system information component uses Python libraries such as:

```text
socket
platform
getpass
requests
```

It can obtain information such as:

* Hostname
* Private IP address
* Public IP address
* Operating system
* OS version
* Processor
* Machine architecture
* Current username

---

### 4.3 Clipboard Access

The Windows clipboard component accesses clipboard contents through the Windows clipboard API.

This demonstrates why clipboard access can represent a security risk.

Sensitive information such as credentials, tokens, URLs, and copied documents may potentially be exposed when malicious software has access to the clipboard.

---

### 4.4 Screenshot Capture

The screenshot component uses Pillow to capture the current desktop environment and save the resulting image.

This demonstrates how unauthorized software could potentially capture information displayed on a user's screen.

---

### 4.5 Keyboard Monitoring

The keyboard-monitoring component uses the `pynput` library to observe keyboard events.

The events can then be processed and written to a local file.

This functionality is included strictly for controlled cybersecurity experimentation.

---

### 4.6 Encryption

The project uses Fernet symmetric encryption from the Python Cryptography library.

The general process is:

```text
Plaintext File
      │
      ▼
Encryption Key
      │
      ▼
Fernet Encryption
      │
      ▼
Encrypted File
```

The encryption key must be securely stored and must never be committed to a public repository.

---

### 4.7 File Transmission

The project contains functionality for sending generated files through email.

In an authorized laboratory, this can be used to demonstrate how information-stealing software may attempt to transfer collected information outside an endpoint.

Real personal information should never be used during testing.

---

### 4.8 Cleanup

The project can remove temporary files generated during execution.

From a defensive perspective, file deletion can be an important behavior to investigate because malicious software may attempt to remove artifacts after completing an operation.

---

## 5. Error Handling

Potential errors include:

* Missing Python dependencies
* Invalid file paths
* Permission errors
* Network failures
* Clipboard access failures
* Screenshot failures
* Invalid encryption keys
* Email authentication failures
* Missing files during cleanup

The recommended approach is to handle expected exceptions explicitly and provide meaningful error messages.

Example:

```python
try:
    # Operation
    pass
except OSError as error:
    print(f"File operation failed: {error}")
except Exception as error:
    print(f"Unexpected error: {error}")
```

Broad exception handling should be minimized in production-quality code.

---

## 6. Testing Environment

Testing should be performed in an isolated virtual laboratory.

Recommended environment:

```text
Host Machine
     │
     └── Virtual Machine
            │
            ├── Windows
            ├── Test account
            └── Test data
```

The test environment should not contain real credentials or personal information.

---

## 7. Limitations

Current limitations may include:

* Windows-specific functionality
* Dependency on third-party Python packages
* Dependency on local permissions
* Dependency on network connectivity for transmission
* Limited error recovery
* No persistence mechanism
* No command-and-control infrastructure
* No centralized monitoring system

---

## 8. Security Considerations

This project demonstrates capabilities that can be abused by malicious software.

Therefore:

* Use isolated test systems.
* Use dummy credentials and data.
* Do not test against unauthorized systems.
* Do not commit collected information.
* Do not publish credentials.
* Do not distribute the software for unauthorized surveillance.

---

## 9. Conclusion

This project provides practical insight into the technical mechanisms associated with keylogging and endpoint surveillance.

The primary educational value is understanding both the implementation concepts and the associated security risks so that similar behavior can be recognized and investigated from a defensive cybersecurity perspective.
