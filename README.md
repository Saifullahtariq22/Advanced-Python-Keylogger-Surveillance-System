# Advanced Python Keylogger & Surveillance System

An advanced Python-based keylogger and surveillance system developed for cybersecurity education, research, and authorized laboratory environments.

The project demonstrates how surveillance-oriented software can collect different types of endpoint information, store collected data, apply encryption, and transmit files. It is intended to provide practical understanding of the techniques and security implications associated with keylogging and information-stealing software.

> **⚠️ Disclaimer:** This project is intended strictly for authorized cybersecurity research, education, and controlled laboratory environments. Do not deploy or operate it on systems or accounts without explicit authorization.

---

## Features

* Keyboard input monitoring
* System and network information collection
* Clipboard data collection
* Screenshot capture
* Local file-based logging
* Data encryption using Fernet
* Automated file transmission
* Configurable collection intervals
* Basic exception handling and file management

---

## Technologies

* **Python 3**
* `pynput`
* `pywin32`
* `Pillow`
* `Requests`
* `Cryptography`
* `SoundDevice`
* `SciPy`
* Python standard libraries

---

## Project Workflow

```text
        Endpoint Activity
               │
               ▼
      ┌─────────────────┐
      │ Data Collection │
      └────────┬────────┘
               │
       ┌───────┼────────┐
       ▼       ▼        ▼
   Keyboard  System   Clipboard
   Activity  Info     Data
       │       │        │
       └───────┼────────┘
               ▼
        Local Data Files
               │
               ▼
           Encryption
               │
               ▼
        File Transmission
               │
               ▼
            Cleanup
```

---

## Project Structure

```text
Advanced-Python-Keylogger/
│
├── keylogger.py
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── technical-documentation.md
│   ├── architecture.md
│   └── security-analysis.md
│
├── screenshots/
│   └── README.md
│
└── examples/
    └── sample-output.txt
```

---

## Installation

Clone the repository:

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd Advanced-Python-Keylogger
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Configuration

Before running the project in an authorized laboratory environment, review the configuration section of the Python source code.

Configuration may include:

* Output directory
* Collection intervals
* Maximum collection iterations
* Encryption key
* Authorized test email configuration

### Security Warning

Never commit the following to GitHub:

```text
Passwords
Email credentials
Encryption keys
API keys
Authentication tokens
Collected keystrokes
Real clipboard contents
Personal screenshots
Private system information
```

Use environment variables or a local configuration file that is excluded through `.gitignore`.

---

## Components

### Keyboard Monitoring

The keyboard monitoring component demonstrates how keyboard events can be observed and recorded.

### System Information

The system information component gathers information about the operating environment and network configuration.

### Clipboard Collection

The clipboard component demonstrates how applications can access data currently stored in the operating system clipboard.

### Screenshot Capture

The screenshot component demonstrates programmatic screen capture within the test environment.

### Encryption

Collected files can be encrypted using the Fernet symmetric encryption mechanism provided by the `cryptography` library.

### Transmission

The project demonstrates automated transmission of generated files to an authorized destination.

### Cleanup

Temporary files generated during the experiment can be removed after processing.

---

## Security Research Purpose

Keylogging and surveillance capabilities are commonly associated with information-stealing malware.

Studying these techniques in an isolated environment helps cybersecurity students understand:

* How endpoint information can be collected
* How sensitive information can be exposed
* How malware may process collected information
* How encrypted data can be handled
* How suspicious network activity can occur
* How defenders can identify potentially malicious behavior

---

## Ethical and Legal Considerations

This software must only be used:

* On systems you own
* In isolated cybersecurity laboratories
* With explicit authorization
* For educational or security research purposes

Unauthorized monitoring of another person's computer activity or collection of their information may violate privacy and computer misuse laws.

---

## Future Improvements

Potential future improvements include:

* Improved modular architecture
* Configuration through environment variables
* Better logging and exception handling
* Unit testing
* Improved cross-platform compatibility
* Defensive detection rules
* Integration with endpoint security telemetry
* Malware-behavior analysis
* Automated testing in an isolated virtual laboratory

---

## Author

**Saifullah Tariq**

BS Cyber Security
Air University Islamabad

---

## License

See the `LICENSE` file for licensing information.

