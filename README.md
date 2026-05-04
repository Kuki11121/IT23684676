# IT23684676
This repository contains the Playwright test automation project for evaluating a Singlish-to-Sinhala chat translator. The script reads 50 chat-style Singlish test cases from an Excel file, inputs them into the web application, and automatically records the actual Sinhala output and the test status (Pass/Fail) back into the Excel sheet.

Prerequisites
Before running the script, make sure you have the following installed on your machine:

Python 3.11 or 3.12
Google Chrome (Recommended)
Setup & Installation
Download and extract the project folder.

Open your Command Prompt (CMD) or terminal and navigate to the extracted folder.

Update pip (optional but good practice): pip install -U pip

Install the required Python dependencies: pip install playwright openpyxl

Install the Playwright browsers: playwright install

How to Run the Tests
Open your Command Prompt inside the project directory and run the following command.

python IT23684676.py --excel "IT23684676.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open

Project Structure
IT23684676.py : The main Python script that runs the Playwright automation.
IT23684676.xlsx : The Excel file containing the 50 test scenarios. The script will write the actual results directly into this file.
README.md : Setup and execution instructions.
