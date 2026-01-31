# IT23684676
IT3040 - ITPM Assignment 1
🎯 Assignment Overview
This assignment involves testing a Singlish-to-Sinhala translation system and automating the test cases using Playwright. The project evaluates the accuracy and robustness of the translation system across various linguistic scenarios.

📋 Project Structure
text
```
assignment-1/
├── tests/
│   └── test.spec.ts          # All test cases (positive, negative, UI)
├── playwright.config.ts       # Playwright configuration
├── tsconfig.json             # TypeScript configuration
├── package.json              # Dependencies and scripts
├── README.md                 # This file
├── test-results/             # Generated test results and screenshots
│   ├── debug-website.png
│   ├── Pos_Fun_0001-success.png
│   └── ...
└── Book1.xlsx                # Test case documentation (provided)
```
✨ Features
34 Positive Test Cases (Pos_Fun_0001 to Pos_Fun_0034)

11 Negative Test Cases (Neg_Fun_0001 to Neg_Fun_0011)

1 UI Test Case (Neg_UI_0001)

1 Debug Test for website exploration

Flexible comparison logic to handle minor output variations

Comprehensive console logging for test execution details

Automatic screenshot capture for debugging

🚀 Installation
Prerequisites
Node.js (v16 or higher)

npm or yarn

Steps
1. Clone or download the project
```
bash
git clone <your-repository-url>
cd assignment-1
```
2. Install dependencies
```
bash
npm install
```
3. Install Playwright browsers
```
bash
npx playwright install
```

🧪 Test Case Coverage
Sentence Structures
Simple, compound, and complex sentences

Interrogative (questions) and imperative (commands) forms

Positive and negative sentence forms

Daily Language Usage
Common greetings, requests, and responses

Polite vs informal phrasing

Frequently used day-to-day expressions

Word Combinations & Patterns
Multi-word expressions and frequent collocations

Joined vs segmented word variations

Repeated word expressions for emphasis

Grammatical Forms
Tense variations (past, present, future)

Negation patterns

Singular/plural usage and pronoun variations

Request forms with varying politeness

Input Length Variation
Short inputs (≤30 characters)

Medium inputs (31–299 characters)

Long inputs (≥300 characters)

Mixed Language Content
English technical/brand terms embedded in Singlish

Sentences containing places and common English words

English abbreviations and short forms

Punctuation & Formatting
Inputs containing punctuation marks

Currency, time formats, dates, and units of measurement

Multiple spaces, line breaks, and paragraph-style inputs

Informal Language
Slang and colloquial phrasing

🏃‍♂️ Running Tests
Run All Tests
```
bash
npx playwright test
```
Run Specific Test Categories
```
bash
# Run only positive functional tests
npx playwright test --grep "Pos_Fun"

# Run only negative functional tests
npx playwright test --grep "Neg_Fun"

# Run specific test
npx playwright test --grep "Pos_Fun_0001"

# Run tests matching pattern
npx playwright test --grep "000[1-5]"
```
Run with Different Options
```
bash
# Run with UI mode (interactive)
npx playwright test --ui

# Run in headed mode (visible browser)
npx playwright test --headed

# Run with debug mode
npx playwright test --debug

# Run with specific browser
npx playwright test --project=chromium
npx playwright test --project=firefox
npx playwright test --project=webkit
```

Generate Reports
```
bash
# Generate HTML report
npx playwright test --reporter=html

# View the HTML report
npx playwright show-report

# Generate JUnit report
npx playwright test --reporter=junit

# Generate list reporter
npx playwright test --reporter=list
```

📊 Test Results
Test results are stored in:

HTML Report: Automatically generated in ```playwright-report/```

Screenshots: Captured in ```test-results/``` folder

Console Output: Detailed logs in terminal

Viewing Reports
Run tests with HTML reporter:
```
bash
npx playwright test --reporter=html
```
Open the report:
```
bash
npx playwright show-report
```
🔧 Configuration
playwright.config.ts
The configuration includes:

Multiple browser support (Chromium, Firefox, WebKit)

HTML reporter for detailed results

Screenshot and video capture on failure

Test retry logic for CI environments

Custom timeout settings

Test Case Design
Each test case follows this structure:
```
typescript
test('Test_ID - Test Name', async ({ page }) => {
  // 1. Test case data
  // 2. Navigation to website
  // 3. Input field interaction
  // 4. Output verification
  // 5. Assertion with flexible comparison
  // 6. Console logging for traceability
});
```
Flexible Comparison Logic
The test suite includes a smart comparison function that:

Normalizes whitespace

Allows for minor formatting differences

Checks for substring matches

Calculates similarity scores for partial matches

Provides detailed debugging information

🐛 Troubleshooting
Common Issues
"Cannot find input field" error

Run the debug test first: ```npx playwright test --grep "Debug"```

Update selectors in ```findAndTestTranslation``` function based on actual website structure

Tests failing due to timing

Increase wait times in ```findAndTestTranslation``` function

Use ```await page.waitForTimeout(ms)``` for specific delays

Browser installation issues
```
bash
# Reinstall Playwright browsers
npx playwright install --force
```
TypeScript compilation errors
```
bash
# Check TypeScript configuration
npx tsc --noEmit
```
Debugging Tips
Use the debug test to understand website structure

Check screenshots in ```test-results/``` folder

Run tests with ```--debug``` flag for step-by-step execution

Use ```console.log()``` statements in test code for tracing

📝 Test Case Documentation
Excel File Integration
The test cases in Book1.xlsx are implemented in test.spec.ts with:

TC ID: Matches Excel test case IDs

Test case name: Descriptive names from Excel

Input: Singlish text to translate

Expected output: Expected Sinhala translation

Actual output: Captured during test execution

Status: Automatically determined (Pass/Fail)

Test Categories Implemented
✅ Daily language usage

✅ Greeting/request/response

✅ Word combination/phrase pattern

✅ Mixed Singlish + English

✅ Slang/informal language

✅ Typographical error handling

✅ Names/places/common English words

✅ Punctuation/numbers

✅ Formatting (spaces/line breaks/paragraph)

✅ Error handling/input validation

📈 Quality Metrics
Test Coverage
Functional Coverage: 100% of specified test scenarios

Input Variety: Short, medium, and long inputs

Edge Cases: Special characters, mixed language, formatting issues

UI Testing: Real-time conversion feedback

Reliability Features
Automatic retry on failure

Screenshot capture for debugging

Flexible assertion logic

Comprehensive error handling

🏗️ Building Upon This Project
Adding New Test Cases
Add test data following the existing pattern

Use the findAndTestTranslation helper function

Include appropriate console logging

Run the new test individually first

Modifying Selectors
If the website structure changes:

Run the debug test

Update selectors in findAndTestTranslation

Test with a few basic cases first

Extending Functionality
Add data-driven tests from external files

Implement parallel test execution

Add performance testing

Include accessibility testing

📚 References
Playwright Documentation
Playwright Getting Started

Playwright Test

Playwright API

Assignment Resources
Assignment PDF: ```Assignment 1.pdf```

Test Case Template: ```IT23684676.xlsx```

Website Under Test: ```https://www.swifttranslator.com/```