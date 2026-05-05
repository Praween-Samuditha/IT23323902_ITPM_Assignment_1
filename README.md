# IT23323902 - ITPM Assignment 1
## Transliteration Accuracy Testing - IT3040

---

## Project Overview

This repository contains the automated testing project for evaluating the accuracy of the Chat Sinhala transliteration function available at [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator).

The project identifies **50 test cases** where the system fails to correctly convert chat-style Singlish into Sinhala, covering all 24 Singlish input types specified in the assignment.

---

## Repository Contents

| File | Description |
|------|-------------|
| `test_automation.py` | Playwright automation script that runs all test cases |
| `IT23323902.xlsx` | Excel file containing all 50 test cases with results |
| `IT23323902_Git repository link.txt` | Text file containing this repository link |
| `README.md` | Project documentation and setup instructions |

---

## Prerequisites

Before running the tests, make sure you have the following installed:

- **Python 3.11 or 3.12**
- **Google Chrome** (recommended) or Chromium

---

## Installation

### Step 1 — Clone the repository

```bash
git clone https://github.com/Praween-Samuditha/IT23323902_ITPM_Assignment_1.git
cd IT23323902_ITPM_Assignment_1
```

### Step 2 — Install required dependencies

```bash
pip install playwright openpyxl
```

### Step 3 — Install Playwright browsers

```bash
python -m playwright install
```

---

## Running the Tests

From the project directory, run the following command:

```bash
python test_automation.py --excel "IT23323902.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 10000 --type-delay-ms 100 --slow-mo-ms 300 --save-every 1 --keep-open
```

### Command Parameters Explained

| Parameter | Value | Description |
|-----------|-------|-------------|
| `--excel` | `IT23323902.xlsx` | Path to the Excel test cases file |
| `--url` | `https://www.pixelssuite.com/chat-translator` | URL of the application under test |
| `--wait-ms` | `10000` | Wait time in milliseconds after each transliteration |
| `--type-delay-ms` | `100` | Delay between keystrokes in milliseconds |
| `--slow-mo-ms` | `300` | Slow motion delay for browser actions |
| `--save-every` | `1` | Save results to Excel after every test case |
| `--keep-open` | - | Keep browser open after tests complete |

---

## Test Results

After running the script:

1. Open `IT23323902.xlsx`
2. Check column **E (Actual output)** — filled automatically by the script
3. Check column **F (Status)** — shows **PASS** or **FAIL** for each test case

---

## Test Case Structure

The Excel file contains the following columns:

| Column | Header | Description |
|--------|--------|-------------|
| A | TC ID | Test case identifier (Neg_0001 to Neg_0050) |
| B | Input length type | S (≤30 chars), M (31-299 chars), L (300-450 chars) |
| C | Input | Singlish input text |
| D | Expected output | Correct Sinhala transliteration |
| E | Actual output | Auto-filled by Playwright script |
| F | Status | Auto-filled: PASS or FAIL |
| G | Singlish input types covered | Which of the 24 types this test covers |
| H | Evidence or rationale | Explanation of why this input type applies |

---

## Singlish Input Types Covered

All 24 input types are covered with at least 2 test cases each:

1. Question forms
2. Command forms
3. Greetings
4. Requests
5. Responses
6. Repeated Words
7. Inputs with Punctuation Marks
8. Romanization / Spelling Variants
9. Isolated English Word Insertions in Singlish
10. Multi-Word English Phrases in Singlish
11. English Digital Terms in Singlish
12. Platform/App Names in Singlish
13. English Abbreviations/Acronyms in Singlish
14. English Clipped Forms in Singlish
15. Place Names Embedded in Singlish
16. Person Names Embedded in Singlish
17. Inputs with Numbers and Numeric Suffixes
18. Inputs with Currency
19. Inputs with Time Formats
20. Inputs with Dates
21. Inputs with Unit of Measurements
22. Inputs with Slang and Casual Phrasing
23. Online Identifiers in Singlish
24. Inputs Containing Emojis

---

## Notes

- Make sure the Excel file is **closed** before running the script
- Ensure a stable internet connection during test execution
- The application under test must be accessible at the provided URL
- Test execution takes approximately **10-15 minutes** for all 50 test cases

---

## Author

**Praween Samuditha**  
Registration Number: IT23323902  
Module: IT3040 - IT Project Management  
Academic Year: Year 3, Semester 1
