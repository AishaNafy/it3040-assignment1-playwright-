# IT3040 – Assignment 1  
# Chat Sinhala Transliteration Accuracy Testing using Playwright

This repository contains the complete automation project developed for **IT3040 – ITPM Semester 1, Assignment 1 (IT23321236)**.  

The objective of this project is to evaluate the transliteration accuracy of the Chat Sinhala Transliteration system by automatically executing negative test scenarios against the live application.

Target Application:

https://www.pixelssuite.com/chat-translator

---

# Project Overview

This automation framework:

- Reads test cases from an Excel spreadsheet
- Launches the browser using Playwright
- Enters Singlish chat inputs
- Captures generated Sinhala output
- Compares actual output against expected output
- Automatically updates the Excel file with:
  - Actual output
  - PASS / FAIL status

The framework supports:

- Dynamic Excel header detection
- Retry mechanisms
- UI synchronization
- Automatic error handling
- Incremental result saving

---

# Technology Stack

- Python 3.11+
- Playwright
- OpenPyXL
- Google Chrome / Chromium

---

# Project Structure

```text
.
├── test_automation.py
├── Assignment 1 - Test cases.xlsx
├── repository link.txt
├── README.md
└── .gitignore
```

---

# Prerequisites

Before running this project, ensure the following are installed:

# Python

Download and install Python:

https://www.python.org/downloads/

Recommended version:

Python 3.11 or later

Verify installation:

```bash
python --version
```

---

# Git

Download:

https://git-scm.com/downloads

Verify:

```bash
git --version
```

---

# Clone Repository

Clone the public repository:

```bash
git clone https://github.com/AishaNafy/it3040-assignment1-playwright-
```

Navigate to project folder:

```bash
cd <YOUR_PROJECT_FOLDER>
```

---

# Installation

# Step 1: Upgrade pip

```bash
pip install --upgrade pip
```

# Step 2: Install dependencies

```bash
pip install -r requirements.txt
```

# Step 3: Install Playwright browsers

```bash
playwright install
```

---

# Required Python Packages

The following dependencies are used:

```txt
playwright
openpyxl
```

---

# Test Data Preparation

Open:

Assignment 1 - Test cases.xlsx

Populate only the following columns:

- TC ID
- Input length type
- Input
- Expected output

Do NOT manually edit:

- Actual output
- Status

These fields are automatically updated during execution.

---

# Running the Automation

Execute:

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx"
```

---

# Advanced Execution Options

# Keep browser open

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --keep-open
```

# Slow motion execution

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --slow-mo-ms 200
```

# Headless mode

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --headless
```

# Save after every test

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --save-every 1
```

---

# Default Configuration

| Parameter | Default Value |
|----------|---------------|
| wait-ms | 5000 |
| retries | 8 |
| retry-wait-ms | 1000 |
| type-delay-ms | 30 |
| timeout-ms | 60000 |

---

# Output

After execution, the Excel file is automatically updated with:

# Actual Output

Sinhala output returned by the application.

# Status

Possible values:

- PASS
- FAIL
- COLLECTED
- UI Error

---

# Error Handling

The framework handles:

# UI element detection failures

Automatically retries until timeout.

# Network delays

Configurable wait and retry strategy.

# Dynamic UI overlays

Automatically dismisses popup dialogs.

# Excel formatting issues

Supports merged cells and dynamic column resolution.

---

# Example Execution Output

```text
Starting Frontend-Only test with 50 rows...

Frontend loaded successfully.

Testing [Row 2]: umbata hariyada?
-> FAIL

Testing [Row 3]: oyala kohomada?
-> PASS

Testing [Row 4]: mata poddak kiyanna
-> FAIL

Test completed.
Results saved successfully.
```

---

# Assignment Compliance

This repository includes:

✔ Full Playwright automation project  
✔ Scripts and configuration files  
✔ Public Git repository  
✔ Execution instructions  
✔ Excel-based automated result generation  

Compliant with IT3040 Assignment 1 submission requirements.

---

# Author

Student Name: Nafy F A 

Registration Number: IT233321236

Module: IT3040 – Information Technology Project Management  

---

# Academic Integrity

This project was developed individually for academic assessment purposes. Unauthorized copying or distribution is prohibited.
