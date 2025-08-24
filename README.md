Cucumber SDET Project

This project is a robust, ready-to-use Mobile Test Automation Framework designed to streamline and enhance testing processes for both Android and iOS devices. Built with the Behavior-Driven Development (BDD) approach, it uses the Cucumber framework to allow for test scenarios to be written in a business-readable language (Gherkin), improving collaboration and communication across the team.

Key Features

  Cross-Platform Automation: Supports test automation on both Android and iOS mobile platforms.
  BDD Approach: Uses Cucumber and Gherkin syntax for writing clear and human-readable test scenarios.
  Extensive Reporting: Integrates with various reporting tools to generate comprehensive and insightful test reports, including Cucumber HTML Report, Extent HTML/PDF Report, and Timeline Report.
  Flexible Execution: Allows for local testing and remote execution through platforms like Sauce Labs, offering scalability and flexibility.
  Maven Integration: The project is configured with Maven, enabling easy test execution from the command line with configurable runtime parameters.
  Page Object Model (POM): The framework follows the POM design pattern for maintaining clean, reusable, and maintainable code.

Prerequisites

To get started with this project, ensure you have the following installed:

  Java 11 or higher
  Maven
  An IDE (e.g., IntelliJ IDEA)
  Node.js (required for Appium)
  Appium (install with `npm i --location=global appium`)
  Appium Drivers for the platforms you wish to test (e.g., `appium driver install uiautomator2` for Android).

Getting Started

Follow these steps to set up and run the tests:

1.  Clone the repository:

    ```
    git clone https://github.com/theviks/Cucumber_SDET_Project.git
    ```

2.  Navigate to the project directory:

    ```
    cd Cucumber_SDET_Project
    ```

3.  Install dependencies and build the project:

    ```
    mvn clean install
    ```

Running Tests

Tests can be executed from the command line using Maven. The framework is highly configurable via command-line parameters.

Running all tests

```
mvn clean install
```

Running selected tests using tags

Use the `-Dcucumber.filter.tags` parameter to filter tests based on Cucumber tags.

  Run all tests with the `@Regression` tag:

    ```
    mvn clean install -Dcucumber.filter.tags="@Regression"
    ```

    Run a combination of tags:

    ```
    mvn clean install -Dcucumber.filter.tags="@Smoke and @Login"
    ```

    Exclude specific tags:

    ```
    mvn clean install -Dcucumber.filter.tags="not @Ignore"
    ```

Reports

After test execution, various reports are generated in the `testReports` directory. These reports provide detailed information about the test run, including pass/fail status, execution time, and screenshots of failures.

  `testReports/CucumberReport.html`
  `testReports/ExtentReport.html`
  `testReports/ExtentReport.pdf`
