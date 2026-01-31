# it23219052-IT3040
ITPM - ASSIGNMENT 1



# SwiftTranslator Test Automation Suite

This repository contains an automated test suite for the **SwiftTranslator Singlish → Sinhala** web application, built using **Playwright** and **JavaScript**.

The tests validate functional accuracy, error handling, and UI behavior of the real-time translation feature.

---

## 📌 Project Overview

This automation suite verifies the correctness and reliability of the SwiftTranslator system by covering:

* ✅ **24 Positive Functional Test Cases**
* ❌ **10 Negative Functional Test Cases**
* 🖥️ **1 UI Real-Time Translation Test**

The tests ensure accurate Singlish-to-Sinhala conversion under normal, edge-case, and user-interaction scenarios.

---

## 🛠️ Technologies Used

* **Node.js**
* **Playwright Test Framework**
* **JavaScript**
* **Chromium Browser**

---

## 📋 Prerequisites

Before running the tests, ensure you have:

* **Node.js** version 16 or higher
* **npm** (included with Node.js)

Verify installation:

```bash
node --version
npm --version
```

---

## 📦 Installation

### Step 1: Clone or Download the Project

```bash
git clone <repository-url>
cd <project-directory>
```

Or extract the ZIP file into a local directory.

---

### Step 2: Install Dependencies

```bash
npm install
```

---

### Step 3: Install Playwright Browsers

```bash
npx playwright install chromium
```

---

## 📁 Project Structure

```
.
├── swift-translator-tests.spec.js   # Main Playwright test suite
├── playwright.config.js             # Playwright configuration
├── package.json                     # Project dependencies & scripts
├── test-results/                    # Test reports & artifacts
└── README.md                        # Project documentation
```

---

## ▶️ Running the Tests

### Run All Tests

```bash
npm test
```

---

### Run Tests in Headed Mode (Visible Browser)

```bash
npx playwright test --headed
```

---

### Run Tests Using Playwright UI Mode

```bash
npx playwright test --ui
```

---

### Run Tests in Debug Mode

```bash
npx playwright test --debug
```

---

### View HTML Test Report

```bash
npx playwright show-report
```

---

## 🧪 Test Coverage

### ✅ Positive Functional Tests (24 Scenarios)

These tests validate correct translations for:

* Simple, compound, and multi-word sentences
* Questions, commands, and polite requests
* Past, present, and future tense usage
* Negation patterns
* Greetings and daily expressions
* Slang and informal language
* Mixed Singlish + English content
* Numbers, currency, and time formats
* Multi-line and repeated-word inputs

---

### ❌ Negative Functional Tests (10 Scenarios)

These tests check robustness against:

* Misspelled words
* Missing or extra spaces
* Random characters
* Special symbols
* Informal slang with errors
* Mixed English words with incorrect formatting
* Abbreviations inside sentences

---

### 🖥️ UI Functionality Test (1 Scenario)

* Verifies **real-time translation updates while typing**
* Confirms partial output appears dynamically
* Validates final translated output after full input

---

## 🧱 Test Data Design

Each test case includes:

* **Test Case ID** (e.g., `Pos_Fun_001`)
* **Test Name**
* **Input Text (Singlish)**
* **Expected Output (Sinhala)**
* **Category** (Daily usage, slang, formatting, etc.)
* **Grammar Focus**
* **Input Length** (S / M / L)

---

## ⚙️ Configuration Details

Configuration is centralized in the test file:

* Base URL: `https://www.swifttranslator.com/`
* Controlled timeouts for:

  * Page load
  * Input clearing
  * Translation wait
  * Delay between tests
* Stable selectors used for input and output detection
* Sequential execution to avoid UI conflicts

---

## 🧠 Design Approach

* **Page Object Model (POM)** used via `TranslatorPage` class
* Reusable helper methods:

  * Navigation
  * Input handling
  * Output detection
  * Translation execution
* Dynamic waiting for translation output instead of static delays

---

## 🐞 Troubleshooting

### Tests Failing?

* Ensure stable internet connection
* Website UI or selectors may have changed
* Increase timeout values if translations are slow

---

### Playwright Issues?

```bash
npx playwright install --force chromium
```

---

### npm Issues?

```bash
npm cache clean --force
npm install
```

---

## 📊 Test Results & Reports

After execution, results are stored in:

```
test-results/
├── html-report/
├── screenshots/
├── videos/
└── test-results.json
```

Screenshots and videos are captured **only on failures**.

---

## 📘 Notes

* Tests run sequentially for stability
* 2-second delay between tests to avoid UI overlap
* Real browser interaction (no mocks)
* Designed for educational and QA validation purposes

---

## 📜 License

This project is created **for educational use** as part of an academic assignment.

---

## ✍️ Author

BSc (Hons) in Information Technology – Year 3 Student



