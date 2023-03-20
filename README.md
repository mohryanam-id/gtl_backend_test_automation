# Backend Test Automation Assignment

## Summary ([demo](https://drive.google.com/file/d/1d6QjakGfLzJfPKPSk6XNKQ5cEX6zhAYh/view?usp=share_link)-> need to request access)

- dummyapi to help simulating the endpoint (latest master), It is using OpenAPI specs and Flask, and it's using almost 1 million records.
- Pytest Framework for the testing, and Allure Framework for the reporting.
- Using 3 test cases, intentionally 2 are failed, and 1 is passed, retrieve data by page/size to allow us only checking on chunked files.


## Description

This is Automated API Testing for comparing two CSV files returned by the /getSecuritiesList API, where one file is generated by the latest master version of the application and the other file is generated by the last released version of the application. The purpose of this script is to perform regression testing for the functionality during every release.

## Getting Started

- Install python (<https://realpython.com/courses/installing-python-windows-macos-linux/>)
- Clone this repository to your local machine.
- Run Terminal/Powershell
- Change directory to the repository
- Install Allure Framework (<https://docs.qameta.io/allure/>)
- [Optional] Create virtual environment and Activate it (<https://realpython.com/python-virtual-environments-a-primer/>)
- Install the required packages by running

```bash
pip3 install -r requirements.txt
```

or

```bash
pip install -r requirements.txt
```

- Run the script by executing

```bash
python3 dummyapi/app.py
```

or

```bash
python dummyapi/app.py
```

- check if the dummyapi is ready by open the url http://localhost:7777 on your browser

## Usage

- Open Terminal/Powershell
- Change directory to the repository
- [Mandatory if it's created] Activate virtual environment
- Run pytest

```bash
pytest
```

- Run Allure by executing

```bash
allure serve ./report/allure
```

## 

## Output

The code will output an allure report showing the differences between the two CSV files on the test cases, if any. If there are no differences, the report will indicate that the two files are identical.

## Improvements

Some possible improvements to this code include:

- Adding more error handling to the code to handle potential errors.
- Adding more functionality to the code to log errors and other events.
- Providing more options for configuring the code, such as setting the column names dynamically.
- Adding more tests to cover edge cases and potential errors.
- Refactoring the code.
- Use dockerization
- Use AI to check false-positive and false-negative
- CI/CD integration

## Criteria

- [x] Solution should be scalable(Should support fast changing product features and requirements and large no of future/current test cases).
- [x] Choose efficient design patterns. Elaborate the choice in a README file.

```text
singleton is the design pattern that is used for reading the config file
```

- [x] Use OOP concepts where you see required.
- [x] Choose the techstack with consideration for Maintainability/Usability/Reporting/Readability.

- [x] Solution should adhere to SOLID principles.
- [x] README file should include the steps to run the tests, the brief description of the approach or any alternative considered and any other dependency.
- [x] What improvements would be needed for the solution to be platform/OS independent.

## Notes

- [x] Tested on Windows
- [x] Tested on Macos
- [x] Parallel Execution
