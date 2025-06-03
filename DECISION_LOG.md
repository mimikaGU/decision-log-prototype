# This file contains concept decisions for GAD automation framework

# Table of Contents

1. [Decision log - for all agreement and statements ](#decision-log-for-sake-of-readability)
2. [Integration of code style tools in framework](#integration-of-code-style-tools-in-framework)
3. [Use of design patterns like POM, AAA, and composition in automated tests](#use-of-design-patterns-like-pom-aaa-and-composition-in-automated-tests)

# Decisions

## Decision log - for all agreement and statements <a id="decision-log-for-sake-of-readability"></a>

**ID**: 001  
**Status**: Pending  
**Date**: ----/01/--  
**Context**:
We need solid statement and together agreement on whole big decisions in our Project repositoy - for sake of 
cooperation including coding standards. In here also is a place where we can keep Client's agreements

- single place for decisions concenring code and its development
- single place for decisions about way of coding (test automation e2e, smoke etc.)
- 

**Proposed solution**

- A few volunteers will keep updated the .md file responsible for storeage the ideas, needs, agreements
- During the separate pull request it will be maintatin accoringly to team decisions
- On daily meetings new ideas, proposals can be delivered/ discussed

**Pros**: One place and solid foundations for one way of proceeding

**Cons**: Somebody has to keep an eye on decision-log and maintain accordingly

**Decision**: _______

**Creator**: Milosz Mika


## Integration of code style tools in framework <a id="integration-of-code-style-tools-in-framework"></a>

**ID**: 002
**Status**: Decided  
**Date**: ----/01/--  
**Context**:
We need static code analysis tools for:

- unified code standard in the framework
- better code readability
- easy code formatting actions

**Proposed solution**

- ESLint for linting coding rules for TypeScript files
- Prettier for formatting files
- Husky for running linting scripts

**Pros**: Tools automate formatting and code style maintenance activities
**Cons**: New tools add more complexity to the solution and require maintenance
**Decision**: Use Prettier, ESLint, and Husky to provide high code standard across the framework
**Creator**: Code Owner


## Use of design patterns like POM, AAA, and composition in automated tests <a id="use-of-design-patterns-like-pom-aaa-and-composition-in-automated-tests"></a>

**ID**: 003
**Status**: Decided  
**Date**: ----/01/--  
**Context**: As our automated test suite grows, we face challenges in maintaining test code readability, reusability, and scalability. We are considering adopting design patterns to improve the overall test structure and maintainability.
**Proposed solution**: Implement the Page Object Model (POM) for UI tests, Arrange-Act-Assert (AAA) pattern for tests, and Composition for creating modular and flexible test components.
**Pros**:
- **Page Object Model (POM)**:
    - Enhanced test organization - POM allows us to structure UI test code by creating separate classes for each web page, resulting in a more organized and readable test suite.
    - Improved test maintenance - Changes to the UI can be localized within the page class, reducing the impact on test code and speeding up maintenance efforts.
    - Reusability - POM promotes reusing page methods across different tests, leading to a more efficient test development process.
- **Arrange-Act-Assert (AAA)**:
    - Clear test structure - AAA separates test code into three distinct sections, making it easier to understand the test's setup, action, and verification steps.
    - Better error localization - With AAA, it is simpler to pinpoint the cause of test failures, aiding in quicker issue resolution.
    - Facilitates testing best practices - AAA aligns with the principles of testing, encouraging developers to write more reliable and robust tests.
- **Composition**:
    - Modular test components - Using composition allows us to build test scenarios by assembling smaller, reusable building blocks, enhancing test maintainability.
    - Flexible test design - By composing test components, we can easily create different test combinations and scenarios, promoting test coverage and adaptability.

**Cons**:
- **Page Object Model (POM)**:
    - Initial setup overhead - Implementing POM may require additional effort in creating page classes and refactoring existing test code.
    - Potential overhead for small projects - In smaller projects with limited UI testing, POM may introduce unnecessary complexity.
- **Arrange-Act-Assert (AAA)**:
    - Learning curve - Developers unfamiliar with AAA might require some time to adapt to the new testing pattern.
- **Composition**:
    - Complexity management - While composition promotes modularity, if not properly managed, it can lead to an overly complex test structure.
    - Abstraction balance - Overuse of composition might obscure the underlying test logic, making it harder to understand the test flow.
**Decision**: Decided. Assertions in tests nad we will adopt the Page Object Model (POM) for UI tests, Arrange-Act-Assert (AAA) pattern for tests.
**Creator**: Code Owner

