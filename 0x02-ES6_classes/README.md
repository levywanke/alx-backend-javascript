# 0x02. ES6 Classes

## Curriculum


## Resources

Read or watch:
- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Metaprogramming](https://developer.mozilla.org/en-US/docs/Glossary/Metaprogramming)

## Learning Objectives

By the end of this project, you should be able to explain the following without the help of Google:
- How to define a Class
- How to add methods to a class
- Why and how to add a static method to a class
- How to extend a class from another
- Metaprogramming and symbols

## Requirements

- All files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`
- All files should end with a new line
- A `README.md` file, at the root of the folder of the project, is mandatory
- Your code should use the `.js` extension
- Your code will be tested using Jest and the command `npm run test`
- Your code will be verified against lint using ESLint
- Your code needs to pass all the tests and lint. You can verify the entire project by running `npm run full-test`

## Setup

### Install NodeJS 12.11.x

```bash
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```

Verify the installation:

```bash
nodejs -v
# v12.11.1

npm -v
# 6.11.3
```

### Install Jest, Babel, and ESLint

In your project directory, install Jest, Babel, and ESLint using the supplied `package.json` and run `npm install`.

### Configuration Files

Add the following files to your project directory:

#### `package.json`

```json
{
  "name": "es6-classes",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "jest",
    "lint": "eslint .",
    "full-test": "npm run lint && npm run test"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "@babel/cli": "^7.15.7",
    "@babel/core": "^7.15.8",
    "@babel/preset-env": "^7.15.8",
    "babel-jest": "^27.2.5",
    "eslint": "^7.32.0",
    "jest": "^27.2.5"
  }
}
```

#### `babel.config.js`

```js
module.exports = {
  presets: [
    ['@babel/preset-env', { targets: { node: 'current' } }],
  ],
};
```

#### `.eslintrc.js`

```js
module.exports = {
  env: {
    browser: true,
    es6: true,
    node: true,
  },
  extends: [
    'eslint:recommended',
    'plugin:react/recommended',
    'plugin:@typescript-eslint/recommended',
  ],
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: [
    'react',
    '@typescript-eslint',
  ],
  rules: {
    'no-unused-vars': 'off',
    '@typescript-eslint/no-unused-vars': ['error'],
  },
};
```

### Run `npm install`

Don't forget to run `npm install` when you have the `package.json`.

## Tasks

### 0. You used to attend a place like this at some point
**Mandatory**

Implement a class named `ClassRoom`:
- Prototype: `export default class ClassRoom`
- It should accept one attribute named `maxStudentsSize` (Number) and assign it to `_maxStudentsSize`.

```js
// 0-main.js
import ClassRoom from "./0-classroom.js";

const room = new ClassRoom(10);
console.log(room._maxStudentsSize);
```

```bash
$ npm run dev 0-main.js 
# 10
```

**Repository:**
- GitHub repository: `alx-backend-javascript`
- Directory: `0x02-ES6_classes`
- File: `0-classroom.js`

### 1. Let's make some classrooms
**Mandatory**

Import the `ClassRoom` class from `0-classroom.js`. Implement a function named `initializeRooms`. It should return an array of 3 `ClassRoom` objects with sizes 19, 20, and 34 (in this order).

```js
// 1-main.js
import initializeRooms from './1-make_classrooms.js';

console.log(initializeRooms());
```

```bash
$ npm run dev 1-main.js 
# [
#   ClassRoom { _maxStudentsSize: 19 },
#   ClassRoom { _maxStudentsSize: 20 },
#   ClassRoom { _maxStudentsSize: 34 }
# ]
```

**Repository:**
- GitHub repository: `alx-backend-javascript`
- Directory: `0x02-ES6_classes`
- File: `1-make_classrooms.js`

### 2. A Course, Getters, and Setters
**Mandatory**

Implement a class named `HolbertonCourse`:
- Constructor attributes: `name` (String), `length` (Number), `students` (array of Strings)
- Verify the type of attributes during object creation
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter and setter for each attribute.

```js
// 2-main.js
import HolbertonCourse from "./2-hbtn_course.js";

const c1 = new HolbertonCourse("ES6", 1, ["Bob", "Jane"]);
console.log(c1.name);
c1.name = "Python 101";
console.log(c1);

try {
    c1.name = 12;
} 
catch(err) {
    console.log(err);
}

try {
    const c2 = new HolbertonCourse("ES6", "1", ["Bob", "Jane"]);
}
catch(err) {
    console.log(err);
}
```

```bash
$ npm run dev 2-main.js 
# ES6
# HolbertonCourse {
#   _name: 'Python 101',
#   _length: 1,
#   _students: [ 'Bob', 'Jane' ]
# }
# TypeError: Name must be a string
#     ...
# TypeError: Length must be a number
#     ...
```

**Repository:**
- GitHub repository: `alx-backend-javascript`
- Directory: `0x02-ES6_classes`
- File: `2-hbtn_course.js`

### 3. Methods, static methods, computed methods names..... MONEY
**Mandatory**

Implement a class named `Currency`:
- Constructor attributes: `code` (String), `name` (String)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter and setter for each attribute.
- Implement a method named `displayFullCurrency` that will return the attributes in the following format `name (code)`.

```js
// 3-main.js
import Currency from "./3-currency.js";

const dollar = new Currency('$', 'Dollars');
console.log(dollar.displayFullCurrency());
```

```bash
$ npm run dev 3-main.js 
# Dollars ($)
```

**Repository:**
- GitHub repository: `alx-backend-javascript`
- Directory: `0x02-ES6_classes`
- File: `3-currency.js`

### 4. Pricing
**Mandatory**

Import the class `Currency` from `3-currency.js`. Implement a class named `Pricing`:
- Constructor attributes: `amount` (Number), `currency` (Currency)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter and setter for each attribute.
- Implement a method named `displayFullPrice` that returns the attributes in the following format `amount currency_name (currency_code)`.
- Implement a static method named `convertPrice`. It should accept two arguments: `amount` (Number), `conversionRate` (Number). The function should return the amount multiplied by the conversion rate.

```js
// 4-main.js
import Pricing from './4-pricing.js';
import Currency from './3-currency.js';

const p = new Pricing(100, new Currency("EUR", "Euro"));
console.log(p);
console.log(p.displayFullPrice());
```

```bash
$ npm run dev 4-main.js 
# Pricing {
#   _amount: 100,
#   _currency: Currency { _code: 'EUR', _name: 'Euro' }
# }
# 100 Euro (EUR)
```

**Repository:**
- GitHub repository: `alx-backend-javascript`
- Directory: `0x02-