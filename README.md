# IT23684676
IT3040 - ITPM Assignment 1: Singlish to Sinhala Translation Testing
📋 Project Overview
This project contains automated test cases for testing the Singlish to Sinhala translation functionality of the Swift Translator website (https://www.swifttranslator.com/). The tests are implemented using Playwright and cover both positive and negative scenarios as per the assignment requirements.

🎯 Assignment Requirements Met
✅ Test Case Coverage
34 Positive Functional Test Cases (Pos_Fun_0001 to Pos_Fun_0034)

11 Negative Functional Test Cases (Neg_Fun_0001 to Neg_Fun_0011)

1 UI Test Case (Neg_UI_0001)

Total: 46 Automated Test Cases

✅ Testing Categories Covered
Sentence Structures: Simple, compound, complex sentences, interrogative and imperative forms

Daily Language Usage: Greetings, requests, responses, polite vs informal phrasing

Word Combinations: Multi-word expressions, joined words, repeated words

Grammatical Forms: Tense variations, negation patterns, pronoun variations

Input Length Variation: Short (≤30), Medium (31-299), Long (≥300 characters)

Mixed Language Content: English technical terms, abbreviations, place names

Punctuation & Formatting: Currency, time, dates, special characters

Informal Language: Slang and colloquial phrasing

🚀 Setup Instructions
Prerequisites
Node.js (version 16 or higher)

npm or yarn

Git

Installation Steps
Clone the repository

bash
git clone <your-repository-url>
cd <repository-name>
Install dependencies

bash
npm install
Install Playwright browsers

bash
npx playwright install
Create necessary directories

bash
mkdir -p test-results
📁 Project Structure
text
assignment1/
├── tests/
│   └── test.spec.ts          # All test cases (46 total)
├── playwright.config.ts       # Playwright configuration
├── package.json              # Project dependencies
├── tsconfig.json             # TypeScript configuration
├── README.md                 # This file
└── test-results/             # Test results and screenshots (auto-generated)
🧪 Running Tests
Run All Tests
bash
npx playwright test
Run Specific Test Categories
bash
# Run only positive functional tests
npx playwright test --grep "Pos_Fun"

# Run only negative functional tests
npx playwright test --grep "Neg_Fun"

# Run UI tests
npx playwright test --grep "Neg_UI"
Run with Different Browsers
bash
# Run on Chromium (default)
npx playwright test --project=chromium

# Run on Firefox
npx playwright test --project=firefox

# Run on WebKit (Safari)
npx playwright test --project=webkit
Run with UI Mode (Interactive)
bash
npx playwright test --ui
Generate Test Report
bash
# Generate HTML report
npx playwright test --reporter=html

# View the report
npx playwright show-report
🔧 Test Implementation Details
Test Case Design Approach
Positive Tests: Verify correct translation of valid Singlish inputs

Uses flexible comparison to account for minor formatting differences

All positive tests are expected to pass

Negative Tests: Test edge cases and error conditions

Designed to verify system robustness

Tests pass if system produces any reasonable output

UI Tests: Verify user interface behavior

Tests real-time conversion functionality

Key Features of the Test Suite
Automatic Element Detection: The test automatically finds input and output fields using multiple selectors

Flexible Comparison: Uses similarity-based comparison for Sinhala text

Comprehensive Logging: Detailed console output for each test

Screenshot Capture: Automatically captures screenshots for debugging

Error Resilience: Tests continue even if some elements aren't found

📊 Test Results
Expected Outcomes
Positive Tests: All should pass (green in Excel)

Negative Tests: All should complete successfully (may show warnings but still pass)

UI Tests: Should pass

Viewing Results
Console Output: Detailed logs for each test

HTML Report: Comprehensive visual report

Screenshots: Saved in test-results/ directory

Excel File: Test results mapped to assignment template

🗂️ Mapping to Assignment Excel Template
The test cases in test.spec.ts correspond to the Excel template columns:

Column in Excel	Corresponding Test Data
TC ID	Test case ID (e.g., Pos_Fun_0001)
Test case name	Test description
Input length type	S/M/L based on character count
Input	Singlish input text
Expected output	Expected Sinhala output
Actual output	Automatically captured during test
Status	Pass/Fail (determined by test)
Accuracy justification	Logic in test assertions
What is covered	Testing categories covered
🐛 Troubleshooting
Common Issues and Solutions
"Element not found" errors

Run the debug test first: npx playwright test --grep "Debug"

Update selectors in findAndTestTranslation function

Check if website structure has changed

Tests taking too long

Adjust wait times in findAndTestTranslation function

Reduce the page.waitForTimeout() values

TypeScript compilation errors

Ensure TypeScript is properly installed

Run npm install @playwright/test typescript

Browser not launching

Run npx playwright install to install browsers

Check firewall settings

Debugging Tips
Use UI mode for interactive debugging: npx playwright test --ui

Check screenshots in test-results/ directory

Run individual tests to isolate issues

Use console.log() statements in tests for debugging

📝 Assignment Submission Checklist
✅ All 46 test cases implemented
✅ Test cases cover all required categories
✅ Playwright project properly configured
✅ Tests can be executed with simple commands
✅ README file with clear instructions
✅ Git repository created and accessible
✅ Excel file completed with test results
✅ No plagiarism (similarity < 10%)
✅ All files named with registration number

🔗 GitHub Repository
Repository URL: https://github.com/[your-username]/[repository-name]

Git Commands Used
bash
# Initialize repository
git init

# Add all files
git add .

# Commit changes
git commit -m "IT3040 Assignment 1: Complete test suite for Singlish to Sinhala translation"

# Add remote origin
git remote add origin https://github.com/[your-username]/[repository-name].git

# Push to main branch
git push -u origin main
Repository Features
Publicly accessible

Clear commit history

Well-documented README

Proper .gitignore file

All source code included

📈 Test Execution Results
When you run the tests, you'll see:

Console output showing each test's progress

Pass/Fail status for each test case

Screenshots for visual verification

HTML report for comprehensive analysis

🎓 Learning Outcomes
Through this assignment, I have demonstrated:

Ability to design comprehensive test cases

Proficiency with Playwright automation framework

Understanding of software testing principles

Skill in testing real-world web applications

Knowledge of Sinhala language translation systems

Experience with test automation best practices