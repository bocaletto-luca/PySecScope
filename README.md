# PySecScope
#### Author: Bocaletto Luca

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge&logo=gnu)](LICENSE) [![Language: Python](https://img.shields.io/badge/Language-Python-blue?style=for-the-badge&logo=python)](https://www.python.org/) [![Linux-Compatible](https://img.shields.io/badge/Linux-Compatible-blue?style=for-the-badge&logo=linux)](https://www.kernel.org/) [![Status: Complete](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)](https://github.com/bocaletto-luca/Directory-Monitor)

PySecScope is a comprehensive Linux enumeration tool with a Tkinter-based graphical user interface. Inspired by LinEnum, this tool gathers system, user, network, and service information, along with detailed security checks, and generates reports in multiple formats (Text, JSON, CSV).

This repository contains two versions of the tool:
- **main_eng.py**: The English version.
- **main_ita.py**: The Italian version.

## Features

- **Modular Scan Modules**:  
  Gather details on system information, user information, network configuration, running services, container status, and more.
  
- **Extended Modules (Thorough Mode)**:  
  Additional modules to retrieve SUID/SGID files, file capabilities, cron jobs, sudoers configuration, log files, installed packages, firewall rules, and more.

- **Multi-Format Reporting**:  
  Generate reports in Text, JSON, or CSV formats including a summary detailing the total scan time.

- **Real-Time Progress Feedback**:  
  A responsive GUI showing a progress bar, status updates, and allowing the user to cancel the scan.

- **GUI Menu Options**:  
  Includes a menu bar with "File" (Exit) and "Help" (About) options.

- **Configuration via INI File**:  
  Default settings (export directory, thorough mode, report format) can be customized via a `pysecscope.ini` file.

- **Logging**:  
  Comprehensive logging is implemented using the Python `logging` module; logs are saved in `pysecscope.log`.

- **Privilege Check**:  
  The tool checks for root privileges and warns the user if not running as root (since some modules require elevated permissions).

## Requirements

- **Python 3.x**  
- Standard Python libraries are used (no external dependencies are required).

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/bocaletto-luca/PySecScope.git
   cd PySecScope
   ```

2. (Optional) Create and adjust the `pysecscope.ini` file to set your default preferences. For example:
   ```ini
   [Settings]
   export_directory =
   thorough = False
   report_format = Text
   ```

## Usage

To run the English version of PySecScope:
```bash
python3 main_eng.py
```

To run the Italian version of PySecScope:
```bash
python3 main_ita.py
```

**Note:** It is recommended to run the tool as root to ensure that all modules can function correctly.

## How It Works

PySecScope performs a comprehensive enumeration of your system:
- It collects basic information (system, user, network, service details) using shell commands.
- In "Thorough Mode," it employs additional checks (e.g., SUID/SGID, file capabilities, log files, cron jobs).
- The results are displayed in a real-time updating GUI and can be exported in your preferred report format.
- A progress bar and status label provide continuous feedback during the scan.
- The tool also supports cancellation of the scan if needed.

## License

PySecScope is released under the GNU General Public License (GPL). See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests. Please ensure your code follows the existing style and includes appropriate tests/documentation.

## About

PySecScope is inspired by LinEnum and designed for authorized security testing and system enumeration. Use responsibly and only in environments where you have explicit permission.

---

Happy scanning!

---
