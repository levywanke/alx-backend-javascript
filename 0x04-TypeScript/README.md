# 0x04. TypeScript


## Resources
- [TypeScript in 5 minutes](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
- [TypeScript documentation](https://www.typescriptlang.org/docs/)

## Learning Objectives
By the end of this project, you should be able to explain the following concepts without needing to refer to Google:
- Basic types in TypeScript
- Interfaces, Classes, and functions
- Working with the DOM and TypeScript
- Generic types
- Using namespaces
- Merging declarations
- Using an ambient namespace to import an external library
- Basic nominal typing with TypeScript

## Requirements
- Allowed editors: vi, vim, emacs, Visual Studio Code
- All files should end with a new line
- Files will be transpiled on Ubuntu 18.04
- TypeScript scripts will be checked with Jest (version 24.9.*)
- A README.md file, at the root of the project folder, is mandatory
- Use the `.ts` extension when possible
- The TypeScript compiler should not show any warnings or errors when compiling your code

## Configuration Files
Use the provided configuration files for the following tasks:
- `package.json`
- `.eslintrc.js`
- `tsconfig.json`
- `webpack.config.js`

## Tasks

### Task 0: Creating an Interface for a Student
- **Directory:** `task_0`
- **Files:** `task_0/js/main.ts`, `task_0/package.json`, `task_0/.eslintrc.js`, `task_0/tsconfig.json`, `task_0/webpack.config.js`
- **Requirements:**
  - Copy provided configuration files into `task_0` directory
  - Write an interface named `Student` with the following properties:
    - `firstName`: string
    - `lastName`: string
    - `age`: number
    - `location`: string
  - Create two student objects and an array `studentsList` containing these objects
  - Use Vanilla JavaScript to render a table, appending a new row for each student in the array with their first name and location

### Task 1: Let's Build a Teacher Interface
- **Directory:** `task_1`
- **Files:** `task_1/js/main.ts`, `task_1/webpack.config.js`, `task_1/tsconfig.json`, `task_1/package.json`
- **Requirements:**
  - Create a directory `task_1` and copy the configuration files
  - Write an interface named `Teacher` with the following properties:
    - `firstName`: string (modifiable only during initialization)
    - `lastName`: string (modifiable only during initialization)
    - `fullTimeEmployee`: boolean
    - `yearsOfExperience`: number (optional)
    - `location`: string
    - Additional attributes can be added dynamically

### Task 2: Extending the Teacher Interface
- **Directory:** `task_1`
- **Files:** `task_1/js/main.ts`
- **Requirements:**
  - Write an interface `Directors` that extends `Teacher`
  - Add a property `numberOfReports`: number

### Task 3: Printing Teachers
- **Directory:** `task_1`
- **Files:** `task_1/js/main.ts`
- **Requirements:**
  - Write a function `printTeacher` that accepts `firstName` and `lastName`, and returns the first letter of `firstName` and the full `lastName`
  - Write an interface `printTeacherFunction`

### Task 4: Writing a Class
- **Directory:** `task_1`
- **Files:** `task_1/js/main.ts`
- **Requirements:**
  - Write a class `StudentClass` with the following:
    - Constructor accepting `firstName` and `lastName`
    - Method `workOnHomework` returning "Currently working"
    - Method `displayName` returning the `firstName`
  - Describe the constructor and class using interfaces

### Task 5: Advanced Types Part 1
- **Directory:** `task_2`
- **Files:** `task_2/js/main.ts`, `task_2/webpack.config.js`, `task_2/tsconfig.json`, `task_2/package.json`
- **Requirements:**
  - Create interfaces `DirectorInterface` and `TeacherInterface` with specific methods
  - Implement these interfaces in `Director` and `Teacher` classes
  - Write a function `createEmployee` that returns either a `Director` or a `Teacher` based on salary

### Task 6: Creating Functions Specific to Employees
- **Directory:** `task_2`
- **Files:** `task_2/js/main.ts`
- **Requirements:**
  - Write a type predicate function `isDirector`
  - Write a function `executeWork` that calls `workDirectorTasks` or `workTeacherTasks` based on the employee type

### Task 7: String Literal Types
- **Directory:** `task_2`
- **Files:** `task_2/js/main.ts`
- **Requirements:**
  - Write a string literal type `Subjects` allowing only `Math` or `History`
  - Write a function `teachClass` that returns the appropriate teaching string based on the subject

### Task 8: Ambient Namespaces
- **Directory:** `task_3`
- **Files:** `task_3/js/main.ts`, `task_3/js/interface.ts`, `task_3/js/crud.d.ts`, `task_3/webpack.config.js`, `task_3/tsconfig.json`
- **Requirements:**
  - Create types and interfaces in `interface.ts`
  - Write type declarations for `crud.js` functions in `crud.d.ts`
  - Use these types in `main.ts` to demonstrate CRUD operations

### Task 9: Namespace & Declaration Merging
- **Directory:** `task_4`
- **Files:** `task_4/package.json`, `task_4/tsconfig.json`, `task_4/js/subjects/Cpp.ts`, `task_4/js/subjects/Java.ts`, `task_4/js/subjects/React.ts`, `task_4/js/subjects/Subject.ts`, `task_4/js/subjects/Teacher.ts`
- **Requirements:**
  - Create and merge declarations in the `Subjects` namespace
  - Implement classes `Cpp`, `Java`, `React` extending `Subject` with specific methods

### Task 10: Update `main.ts`
- **Directory:** `task_4`
- **Files:** `task_4/js/main.ts`
- **Requirements:**
  - Export constants and log results for different subjects and teacher methods

### Task 11: Brand Convention & Nominal Typing
- **Directory:** `task_5`
- **Files:** `task_5/js/main.ts`, `task_5/package.json`, `task_5/webpack.config.js`, `task_5/tsconfig.json`
- **Requirements:**
  - Create interfaces `MajorCredits` and `MinorCredits`
  - Write functions `sumMajorCredits` and `sumMinorCredits` to sum credits of subjects
