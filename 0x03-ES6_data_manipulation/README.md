# ES6 Data Manipulation

## Project Overview
This project covers various aspects of ES6 data manipulation in JavaScript, focusing on using `map`, `filter`, and `reduce` functions on arrays, as well as working with typed arrays and data structures like `Set`, `Map`, and `WeakMap`.

### Learning Objectives
By the end of this project, you should be able to:
- Use `map`, `filter`, and `reduce` on arrays.
- Understand and use typed arrays.
- Work with `Set`, `Map`, and `WeakMap` data structures.

### Requirements
- All files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x.
- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`.
- All files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- Your code should use the `.js` extension.
- Your code will be tested using Jest with `npm run test`.
- Your code will be verified against lint using ESLint.
- Your code needs to pass all tests and lint checks with `npm run full-test`.
- All functions must be exported.

### Setup
**Install NodeJS 12.11.x:**
```sh
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
nodejs -v
npm -v
```

**Install Jest, Babel, and ESLint:**
In your project directory, install the necessary packages:
```sh
npm install
```

### Configuration Files
Ensure the following configuration files are present in your project directory:
- `package.json`
- `babel.config.js`
- `.eslintrc.js`

### Tasks

#### 0. Basic list of objects
Create a function named `getListStudents` that returns an array of objects with attributes `id`, `firstName`, and `location`.

```javascript
import getListStudents from "./0-get_list_students.js";
console.log(getListStudents());
```

#### 1. More mapping
Create a function `getListStudentIds` that returns an array of ids from a list of objects.

```javascript
import getListStudentIds from "./1-get_list_student_ids.js";
import getListStudents from "./0-get_list_students.js";
console.log(getListStudentIds("hello"));
console.log(getListStudentIds(getListStudents()));
```

#### 2. Filter
Create a function `getStudentsByLocation` that returns an array of objects located in a specific city.

```javascript
import getListStudents from "./0-get_list_students.js";
import getStudentsByLocation from "./2-get_students_by_loc.js";
console.log(getStudentsByLocation(getListStudents(), 'San Francisco'));
```

#### 3. Reduce
Create a function `getStudentIdsSum` that returns the sum of all student ids.

```javascript
import getListStudents from "./0-get_list_students.js";
import getStudentIdsSum from "./3-get_ids_sum.js";
console.log(getStudentIdsSum(getListStudents()));
```

#### 4. Combine
Create a function `updateStudentGradeByCity` that returns an array of students for a specific city with their new grade.

```javascript
import getListStudents from "./0-get_list_students.js";
import updateStudentGradeByCity from "./4-update_grade_by_city.js";
console.log(updateStudentGradeByCity(getListStudents(), "San Francisco", [{ studentId: 5, grade: 97 }, { studentId: 1, grade: 86 }]));
```

#### 5. Typed Arrays
Create a function named `createInt8TypedArray` that returns a new `ArrayBuffer` with an `Int8` value at a specific position.

```javascript
import createInt8TypedArray from "./5-typed_arrays.js";
console.log(createInt8TypedArray(10, 2, 89));
```

#### 6. Set Data Structure
Create a function named `setFromArray` that returns a `Set` from an array.

```javascript
import setFromArray from "./6-set.js";
console.log(setFromArray([12, 32, 15, 78, 98, 15]));
```

#### 7. More Set Data Structure
Create a function named `hasValuesFromArray` that returns a boolean if all elements in the array exist within the set.

```javascript
import hasValuesFromArray from "./7-has_array_values.js";
console.log(hasValuesFromArray(new Set([1, 2, 3, 4, 5]), [1]));
```

#### 8. Clean Set
Create a function named `cleanSet` that returns a string of all set values starting with a specific string.

```javascript
import cleanSet from "./8-clean_set.js";
console.log(cleanSet(new Set(['bonjovi', 'bonaparte', 'bonappetit', 'banana']), 'bon'));
```

#### 9. Map Data Structure
Create a function named `groceriesList` that returns a map of groceries.

```javascript
import groceriesList from "./9-groceries_list.js";
console.log(groceriesList());
```

#### 10. More Map Data Structure
Create a function named `updateUniqueItems` that returns an updated map for all items with initial quantity at 1.

import updateUniqueItems from "./10-update_uniq_items.js";
import groceriesList from "./9-groceries_list.js";
const map = groceriesList();
updateUniqueItems(map);
console.log(map);