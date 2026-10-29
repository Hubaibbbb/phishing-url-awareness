# Phishing URL Awareness Checker

## 1. Project Overview

The Phishing URL Awareness Checker is a simple Python-based cybersecurity mini project. It checks a URL's text for selected warning signs that may be associated with phishing.

The program does not open websites or visit any URLs. It only inspects the text entered by the user.

## 2. Features

- Detects the `@` symbol in a URL.
- Flags unusually long URLs (over 100 characters).
- Detects IP addresses used as hostnames.
- Flags hostnames containing five or more segments.
- Detects punycode-style hostnames containing `xn--`.
- Flags URLs using HTTP.
- Displays a warning summary when warning signs are found.
- Allows users to check multiple URLs until they choose to quit.
- Handles empty input and URLs without an identifiable hostname.

## 3. Technologies Used

- Python 3.14.10
- Regular expressions (`re`)
- URL parsing (`urllib.parse`)
- Visual Studio Code

All modules used are included in Python's standard library. No additional packages are required.

## 4. Project Structure

```text
phishing-url-awareness/
├── phishing_checker.py
├── README.md
├── requirements.txt
├── tests/
│   └── test_samples.md
└── screenshots/
    ├── sample_run.png
    └── test_results.png
```

## 5. How to Run

1. Install Python.
2. Open the project folder in Visual Studio Code.
3. Open the integrated terminal.
4. Run the following command on Windows PowerShell:

```powershell
& "$env:LOCALAPPDATA\Programs\Python\Python314\python.exe" phishing_checker.py
```

5. Enter a sample URL when prompted.
6. Type `q` to exit the program.

## 6. Example Output

Example input:

```text
http://192.0.2.10/account
```

Example output:

```text
Result:
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

REVIEW CAREFULLY: Check the warning signs above.
Never enter passwords from unexpected links.
```

## 7. Testing

Five sample URL test cases are documented in `tests/test_samples.md`.

The test cases cover:
- A normal example URL.
- An IP address with HTTP.
- A URL containing an `@` symbol.
- A hostname with many segments.
- A punycode-style hostname.

Actual results and PASS/FAIL status should be recorded after checking each test in the terminal.

## 8. Screenshots

- `screenshots/sample_run.png` — Example program execution.
- `screenshots/test_results.png` — Test case documentation.

## 9. Improvements Implemented

1. Multiple URL checking: Users can inspect multiple URLs in one run without restarting the program.
2. Review warning: The program displays a clear review message when selected warning signs are detected.
3. Input handling: The program handles empty input and cases where a hostname cannot be identified.

## 10. Limitations

- The program uses basic text-based checks and does not use machine learning.
- It does not check website reputation, domain registration, or live threat intelligence.
- A suspicious-looking URL is not automatically confirmed as phishing.
- A URL with no detected warning signs is not guaranteed to be safe.
- HTTPS alone does not guarantee that a website is trustworthy.

## 11. Ethical Use

This project is intended for cybersecurity education and phishing awareness. Use sample URLs for testing. The program does not open or visit the URLs entered.

## 12. Author

Name: Sheikh Mohammad Hubaib  
Project: EWB Edutech Cybersecurity Mini Project  
Project Title: Phishing URL Awareness Checker