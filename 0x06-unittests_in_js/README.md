# 0x06. Unittests in JS

## Table of Contents
- [Description](#description)
- [Curriculum](#curriculum)
- [Resources](#resources)
- [Learning Objectives](#learning-objectives)
- [Requirements](#requirements)
- [Tasks](#tasks)

## Description
This project covers the fundamentals of unit testing in JavaScript using tools like Mocha, Chai, and Sinon. It emphasizes writing effective test suites, handling edge cases, and testing asynchronous functions. The project also introduces integration testing with ExpressJS.

## Curriculum

### Short Specializations
### Topics Covered:
- Unit Tests
- Back-end Development
- JavaScript (ES6)
- NodeJS
- ExpressJS
- Mocha
- Chai
- Sinon

## Resources
- [Mocha documentation](https://mochajs.org/)
- [Chai documentation](https://www.chaijs.com/)
- [Sinon documentation](https://sinonjs.org/)
- [Express documentation](https://expressjs.com/)
- [Request library](https://github.com/request/request)
- [How to Test NodeJS Apps using Mocha, Chai, and SinonJS](https://www.digitalocean.com/community/tutorials/how-to-test-node-js-apps-using-mocha-chai-and-sinon)

## Learning Objectives
By the end of this project, you will be able to:
- Use Mocha to write test suites.
- Utilize different assertion libraries (Node's assert or Chai).
- Present long test suites effectively.
- Use spies and stubs for testing.
- Implement hooks for test setup and teardown.
- Write unit tests for asynchronous functions.
- Write integration tests with a small Node.js server.

## Requirements
- Your code will be executed on Ubuntu 18.04 using Node 12.x.x.
- Editors allowed: `vi`, `vim`, `emacs`, `Visual Studio Code`.
- All files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- Code should use the `.js` extension.
- All tests must pass without warnings or errors when running `npm run test *.test.js`.

## Tasks

### 0. Basic test with Mocha and Node assertion library
- **Objective:** Install Mocha and set up a script to quickly run tests.
- **Files:** `package.json`, `0-calcul.js`, `0-calcul.test.js`

### 1. Combining descriptions
- **Objective:** Extend the function from the previous task to support different operations.
- **Files:** `1-calcul.js`, `1-calcul.test.js`

### 2. Basic test using Chai assertion library
- **Objective:** Rewrite the previous test suite using Chai's `expect` style.
- **Files:** `2-calcul_chai.js`, `2-calcul_chai.test.js`

### 3. Spies
- **Objective:** Use Sinon spies to validate the use of functions in your code.
- **Files:** `utils.js`, `3-payment.js`, `3-payment.test.js`

### 4. Stubs
- **Objective:** Use Sinon stubs to replace function implementations for testing.
- **Files:** `4-payment.js`, `4-payment.test.js`

### 5. Hooks
- **Objective:** Implement hooks for setting up and tearing down test environments.
- **Files:** `5-payment.js`, `5-payment.test.js`

### 6. Async tests with done
- **Objective:** Write tests for asynchronous functions using the `done` callback.
- **Files:** `6-payment_token.js`, `6-payment_token.test.js`

### 7. Skip
- **Objective:** Skip failing tests without removing them from the test suite.
- **Files:** `7-skip.test.js`

### 8. Basic Integration testing
- **Objective:** Set up integration testing for a simple Express server.
- **Files:** `8-api/package.json`, `8-api/api.js`, `8-api/api.test.js`

### 9. Regex integration testing
- **Objective:** Implement regex validation in route parameters for an Express server.
- **Files:** `9-api/api.js`, `9-api/api.test.js`

### 10. Deep equality & Post integration testing
- **Objective:** Test deep equality of objects and implement POST request handling.
- **Files:** `10-api/api.js`, `10-api/api.test.js`