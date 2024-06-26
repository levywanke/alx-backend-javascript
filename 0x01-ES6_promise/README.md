
# ES6 Promises Curriculum

## Overview
- **JavaScript (ES6)**


## Resources
- [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- [JavaScript Promise: An introduction](https://developers.google.com/web/fundamentals/primers/promises)
- [Await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
- [Async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
- [Throw / Try](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/throw)

## Learning Objectives
- Understand Promises, their usage, and methods (`then`, `resolve`, `catch`)
- Use the `await` operator and `async` functions
- Handle errors with Throw / Try

## Requirements
- Ubuntu 18.04 LTS with NodeJS 12.11.x
- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`
- Code in `.js` extension, tested with Jest (`npm run test`), linted with ESLint
- Export all functions

## Setup
### NodeJS Installation
```sh
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
nodejs -v
# v12.11.1
npm -v
# 6.11.3
```

### Install Jest, Babel, and ESLint
```sh
npm install
```

## Tasks Summary
1. **Basic Promise**: Return a Promise using `getResponseFromAPI()`.
2. **Conditional Promise**: Return a promise that resolves/rejects based on a boolean input.
3. **Promise Handlers**: Append handlers to a promise to return specific values or log messages.
4. **Multiple Promises**: Handle multiple promises and log results.
5. **Resolved Promise**: Return a resolved promise with user data.
6. **Rejected Promise**: Return a rejected promise with an error message.
7. **Promise All Settled**: Handle multiple promises and return their status and results.
8. **First Resolved Promise**: Return the result of the first resolved promise.
9. **Error Handling**: Handle errors in a division function.
10. **Guardrails**: Create a queue to handle function results and errors, ensuring processing messages are logged.