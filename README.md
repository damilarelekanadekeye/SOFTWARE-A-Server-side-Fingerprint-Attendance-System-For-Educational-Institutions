# Server-Side Data Processing for IoT Fingerprint Attendance System

![Project Banner](images/banner.jpg)

A Python-based server-side script for processing encrypted attendance data from an IoT fingerprint system, designed for educational institutions. Integrated with Firebase Realtime Database, it decrypts AES-128 records, generates CSV, HTML, and Excel reports, and enables Heads of Department (HODs) to review attendance post-lecture. This script complements the embedded system, available at [EMBEDDED-An-IoT-Based-Fingerprint-Attendance-System-for-Educational-Institutions](https://github.com/damilarelekanadekeye/EMBEDDED-An-IoT-Based-Fingerprint-Attendance-System-for-Educational-Institutions).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Language-Python-green)](https://www.python.org/)
[![Firebase](https://img.shields.io/badge/Database-Firebase-orange)](https://firebase.google.com/)
[![Pandas](https://img.shields.io/badge/Library-Pandas-blue)](https://pandas.pydata.org/)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Software Requirements](#software-requirements)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Data Processing Workflow](#data-processing-workflow)
- [Screenshots](#screenshots)
- [Related Project](#related-project)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview
This repository hosts a server-side Python script (`process_attendance_decryption.py`) that processes encrypted attendance data from an IoT-based fingerprint system. Designed for educational institutions, it retrieves data from Firebase, decrypts it using AES-128, and generates structured reports (CSV, HTML, Excel) for administrators, such as HODs, to review attendance after lectures. The script ensures security, scalability, and automation, complementing the hardware system developed in the [EMBEDDED-An-IoT-Based-Fingerprint-Attendance-System-for-Educational-Institutions](https://github.com/damilarelekanadekeye/EMBEDDED-An-IoT-Based-Fingerprint-Attendance-System-for-Educational-Institutions) repository.

## Features
- **Secure Decryption**: Decrypts AES-128 (CBC mode) Base64-encoded data with PKCS#7 padding.
- **Real-Time Data Access**: Fetches records from Firebase under `/attendance_records/`.
- **Multi-Format Reports**: Generates CSV files per class/date, styled HTML tables, and formatted Excel spreadsheets.
- **Flexible Data Handling**: Supports both list and dictionary Firebase data structures.
- **Error Management**: Logs decryption failures and skips malformed records.
- **Automation**: Streamlines report generation for HODs, enabling post-lecture attendance reviews.
- **Scalability**: Optimized for large datasets using Pandas.

## Software Requirements
- Python 3.8+
- Libraries: `pyrebase`, `pycryptodome`, `pandas`, `tabulate`, `openpyxl`
- Firebase Realtime Database account
- Visual Studio Code or any Python IDE

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/damilarelekanadekeye/server-side-fingerprint-attendance-system.git
   cd server-side-fingerprint-attendance-system
   ```
2. **Install Dependencies:**
```python
pip install pyrebase pycryptodome pandas tabulate openpyxl
```
