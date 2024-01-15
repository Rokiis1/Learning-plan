# Software Testing Life Cycle

- [Requirement Analysis](#requirement-analysis)
- [Test Planning](#test-planning)
- [Defect Reporting and Tracking](#defect-reporting-and-tracking)
- [Test Closure](#test-closure)

**Explanation:**

The Software Testing Life Cycle is a structured approach that encompasses various phases from the inception of a software project to its completion and release. It ensures that the software meets its intended requirements, is free of defects, and aligns with quality standards.

**Key Concepts:**

- **Requirement Analysis**: This initial phase involves understanding and documenting all project requirements, including functional and non-functional aspects. It sets the foundation for the entire testing process.

- **Test Planning**: Test planning is crucial for outlining the scope of testing, identifying necessary resources, creating schedules, defining deliverables, and estimating efforts. It helps in organizing and managing the testing process effectively.

- **Test Case Design**: In this phase, test cases are designed based on the identified requirements. Test scenarios and cases are created to cover various aspects of the software's functionality, ensuring comprehensive testing.

- **Test Execution**: Test execution involves setting up the testing environment, running test cases, and documenting the results. Testers execute the test cases as per the test plan and report any defects they encounter.

- **Defect Reporting and Tracking**: During test execution, defects or issues are identified and reported to the development team. A defect tracking system is used to manage and monitor the status of these reported defects until they are resolved.

- **Test Closure**: Test closure marks the end of the testing phase. It involves evaluating whether all functionalities have been tested, no new defects are found, testing schedules are met, and there are no project risks related to testing.

## Requirement Analysis

**Explanation:**

Requirement Analysis is the first phase in the Software Testing Life Cycle (STLC). In this phase, testers analyze the requirements from a testing perspective. This involves understanding the system, identifying testable requirements, and determining the testing strategies to be used.

**Key Concepts:**

- Understanding the system: Testers need to understand the functionality, architecture, and performance requirements of the system.

- Identifying testable requirements: Not all requirements are testable. Testers need to identify which requirements can be validated through testing.

- Determining testing strategies: Based on the requirements, testers decide the testing strategies like unit testing, integration testing, system testing, etc.

**Syntax:**

Typically a Requirement Traceability Matrix (RTM) which maps each requirement to its corresponding test cases to ensure all requirements are covered by testing.

Understanding the system: The system is an online shopping platform where users can browse products, add them to a cart, and make a purchase. The system needs to handle user authentication, product management, cart management, and payment processing.

*Identifying testable requirements:*

Users should be able to register and log in.
Users should be able to browse products.
Users should be able to add products to a cart.
Users should be able to make a purchase and receive a confirmation.

*Determining testing strategies:*

Unit testing: Test individual components like user registration, login, product browsing, cart management, and payment processing.
Integration testing: Test the interaction between different components, like adding a product to the cart after browsing, and making a purchase after adding to the cart.
System testing: Test the entire system as a whole to ensure all components work together as expected.

*Requirement Traceability Matrix (RTM):*

![Alt text](../assets/images/stlc/rtmTable.png)

## Test Planning

- [Purpose and Content of a Test Plan](#purpose-and-content-of-a-test-plan)
- [Tester's Contribution to Iteration and Release Planning](#testers-contribution-to-iteration-and-release-planning)
- [Entry Criteria and Exit Criteria](#entry-criteria-and-exit-criteria)
- [Estimation Techniques](#estimation-techniques)
- [Test Case Prioritization](#test-case-prioritization)

### Purpose and Content of a Test Plan

**Explanation:**

A test plan is a detailed document that outlines the test strategy, testing objectives, resources (manpower, software, hardware) required for testing, test schedule, test estimation and test deliverables. The purpose of a test plan is to provide clear instructions on how the testing activity should be performed.

**Key Concepts:**

- Test Strategy: Describes the overall approach to testing.

- Test Objectives: Describes what the goals of testing are.

- Resources: Describes what resources are needed for testing.

- Test Schedule: Describes when testing activities will take place.

- Test Estimation: Describes how long testing activities are expected to take.

- Test Deliverables: Describes what the outputs of testing activities will be.

### Tester's Contribution to Iteration and Release Planning

**Explanation:**

A test plan is a detailed document that outlines the test strategy, testing objectives, resources (manpower, software, hardware) required for testing, test schedule, test estimation and test deliverables. The purpose of a test plan is to provide clear instructions on how the testing activity should be performed.

**Key Concepts:**

- Test Strategy: Describes the overall approach to testing.

- Test Objectives: Describes what the goals of testing are.

- Resources: Describes what resources are needed for testing.

- Test Schedule: Describes when testing activities will take place.

- Test Estimation: Describes how long testing activities are expected to take.

- Test Deliverables: Describes what the outputs of testing activities will be.

### Entry Criteria and Exit Criteria

**Explanation:**

Entry criteria are the conditions that must be met before testing can begin. Exit criteria are the conditions that must be met before testing can be considered complete.

**Key Concepts:**

- Entry Criteria: Conditions that must be met before testing can begin.

- Exit Criteria: Conditions that must be met before testing can be considered complete.

### Estimation Techniques

**Explanation:**

Estimation techniques are used to estimate the time and effort required for testing. Common techniques include use case point method, function point method, and test point analysis.

**Key Concepts:**

- Use Case Point Method: An estimation technique based on the complexity and size of use cases.

- Function Point Method: An estimation technique based on the functionality provided by the software.

- Test Point Analysis: An estimation technique based on the number of test cases and their complexity.

### Test Case Prioritization

**Explanation:**

Test case prioritization involves ordering the test cases in a way that the most important or high-risk ones are executed first.

**Key Concepts:**

- Risk-Based Prioritization: Test cases are prioritized based on the risk associated with the functionality they are testing.

- Business Value-Based Prioritization: Test cases are prioritized based on the business value of the functionality they are testing.

## Defect Reporting and Tracking

- [Test Case Report](#test-case-report)
   - [Test Case vs Test Case Report](#test-case-vs-test-case-report)
- [Test Summary Report](#test-summary-report)
- [Defect Report (Bug Report)](#defect-report-bug-report)

### Test Case Report

**Explanation:**

A Test Case Report, also known as a Test Execution Report, provides an overview of the status and results of executed test cases.

**Example:**

- [Test Case Report](./assets/manualTesting/testCaseReport.md)

## Test Case vs Test Case Report

1. **Test Case:**

- **Purpose:** A test case is a detailed document that outlines the specific steps to be followed, the conditions to be met, and the expected outcomes to verify a particular aspect of a software application.

- **Content:** Test cases include information such as test case ID, test steps, input data, expected results, preconditions, and postconditions. They are used by testers to execute tests systematically.

- **Focus:** Test cases are focused on the specific actions to be taken during testing and the expected results, helping testers ensure that the software functions correctly.

2. **Test Case Report (or Test Execution Report):**

- **Purpose**: A Test Case Report, often referred to as a Test Execution Report, provides an overview of the status and results of executed test cases for a specific testing phase or cycle.

- **Content**: Test Case Reports typically include project details, test phase information, test execution dates, the total number of test cases executed, the number of test cases passed and failed, details about the test environment, an overall summary of the testing effort (example overall status, comments), and a list of individual test cases with their execution statuses and any specific comments.

- **Focus**: Test Case Reports focus on summarizing the outcomes of testing efforts and providing stakeholders with a high-level view of the testing progress and results. They help project managers, stakeholders, and team members assess the quality and readiness of the software.

### Tasks: Test Case Report

- [Task: Test Case Report](../QA/tasks/TestCaseReports.md)

## Defect Report (Bug Report)

**Explanation:**

Defect Reports are separate documents used to document and track issues or defects identified during testing. You do not typically write Defect Reports (Bug Reports) within individual test cases.

- Defect Reports document issues found during testing, which may result from executing test cases. These reports are used to communicate the problems to developers or the relevant team responsible for fixing the defects.

**Example:**

- [Example: Defect Report (Bug Report)](./assets/manualTesting/bugReport.md)

### Tasks: Bug Report

- [Task: Defect Report (Bug Report)](../QA/tasks/bugReport.md)

## Test Summary Report

**Explanation:**

A Test Summary Report is a comprehensive document that provides a consolidated overview of the testing activities conducted during a specific phase of a software development life cycle. It serves as a formal record of the testing process, presenting key findings, outcomes, and metrics to stakeholders involved in the project. The primary purpose of the Test Summary Report is to communicate the quality and readiness of the software being tested.

**Key Concepts:**

1. **Consolidation of Testing Information:**
   - The Test Summary Report consolidates information from various testing activities, including test case execution, defect tracking, and other relevant testing processes.

2. **Communication Tool:**
   - It serves as a communication tool between different stakeholders, such as project managers, developers, quality assurance teams, and business analysts, providing them with a snapshot of the testing results.

3. **Project Overview:**
   - The report typically includes details about the project, such as the project name, test phase, and dates of testing. This contextual information helps readers understand the scope of the report.

4. **Test Execution Details:**
   - It provides details about the execution of test cases, including the total number of test cases, the number of test cases passed, and the number of test cases failed. This information indicates the level of test coverage and the overall success of the testing effort.

5. **Defect Summary:**
   - A Test Summary Report includes a summary of defects found during testing, highlighting their severity levels and current status. This section aids in assessing the impact of identified issues on the software.

6. **Test Environment Information:**
   - Details about the test environment, including the operating systems, browsers, and other relevant configurations, are often included. This information helps in understanding the conditions under which the testing was conducted.

7. **Overall Test Status:**
   - The report concludes with an overall test status, indicating whether the testing goals were achieved. The status is typically expressed as Pass or Fail, providing a clear indication of the software's readiness for the next phase.

8. **Recommendations and Next Steps:**
   - In some cases, the Test Summary Report may include recommendations for improvements or actions to be taken based on the testing outcomes. This guides future development and testing efforts.

9. **Approval and Sign-off:**
   - The report may include a section for approval and sign-off by relevant stakeholders, indicating their acceptance of the testing results and readiness to proceed with the next phase of the project.

**Example:**

- [Test Summary Report](./assets/examples/softwareTestingLifeCycle/testSummaryReport.md)

### Tasks: Test Summary Report

- [Task: Test Summary Report](../QA/tasks/testSummaryReport.md)