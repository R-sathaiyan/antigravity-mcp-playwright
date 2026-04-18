🧪 QA Test Manager - Automated Login Test Suite

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Selenium](https://img.shields.io/badge/Selenium-4.18.0-green.svg)
![Pytest](https://img.shields.io/badge/Pytest-8.0.0-yellow.svg)

## 🚀 Overview
This repository contains a comprehensive, automated Quality Assurance testing framework for the [QA Test Manager](https://qa-test-manager.netlify.app/). 

The core application was developed by the senior engineering team at **sirpi**. To ensure the authentication modal is robust, secure, and user-friendly, the sirpi intern team engineered this testing suite from the ground up utilizing the **Antigravity IDE** alongside **Python, Selenium WebDriver, and Pytest**.

## ✨ Key Features
* **Page Object Model (POM):** Clean separation of UI locators and test logic for high maintainability.
* **Comprehensive Coverage:** Validates UI elements, positive workflows, and negative/boundary edge cases.
* **Security Testing:** Automated checks against SQL Injection, Cross-Site Scripting (XSS), and brute-force vulnerabilities.
* **Automated Evidence Collection:** Dynamically captures and saves timestamped screenshots upon any test failure.
* **Headless Execution:** Fully configured for CI/CD pipelines with headless browser support.

## 📂 Project Structure

| File / Folder | Purpose |
| :--- | :--- |
| `pages/login_page.py` | The POM class handling all interactions with the login modal. |
| `utils/helpers.py` | Centralized test data (credentials, payloads) and utility functions. |
| `conftest.py` | Pytest fixtures, browser options, and automated screenshot hooks. |
| `run_tests.py` | A custom CLI runner to execute specific test suites and generate reports. |
| `tests/test_ui_elements.py` | Validates the presence, masking, and styling of all UI components. |
| `tests/test_positive_login.py` | Verifies successful authentication paths and backend responses. |
| `tests/test_negative_login.py` | Tests boundary limits, missing inputs, and security payloads (SQLi/XSS). |

## 🛠️ Setup & Installation

1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/qapilot-automation.git](https://github.com/yourusername/qapilot-automation.git)
   cd qapilot-automation
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🏃‍♂️ Running the Tests

We built a custom runner for easy test execution. You can run the tests with a visible browser, or in headless mode.

**Run the entire suite (visible browser):**
```bash
python run_tests.py
```

**Run in headless mode (for CI/CD):**
```bash
python run_tests.py --headless
```

**Run a specific test suite:**
```bash
python run_tests.py --suite positive
python run_tests.py --suite negative
```

## 📊 Reporting
Upon completion, the framework automatically generates a self-contained HTML test report located in the `/reports` directory, detailing pass/fail ratios and execution times.

## 🤝 Acknowledgments
* **Application Development:** Developed by the senior engineering team at **sirpi**.
* **QA Automation Framework:** Engineered and implemented by the **sirpi intern team** using Python, Selenium, and the Antigravity IDE.
