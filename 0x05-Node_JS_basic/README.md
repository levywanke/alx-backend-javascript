
- **package.json**  
Click to show/hide file contents.

- **babel.config.js**  
Click to show/hide file contents.

- **.eslintrc.js**  
Click to show/hide file contents.

**Note:** Don't forget to run `$ npm install` when you have the `package.json` file.

## Tasks
### 0. Executing basic JavaScript with Node.js
Create a function `displayMessage` in `0-console.js` that prints a string argument to STDOUT.

### 1. Using Process stdin
Create a program `1-stdin.js` that prompts for the user's name and displays it, handling input from the command line.

### 2. Reading a file synchronously with Node.js
Create a function `countStudents` in `2-read_file.js` that reads a database file synchronously and logs the number of students by field.

### 3. Reading a file asynchronously with Node.js
Create a function `countStudents` in `3-read_file_async.js` that reads a database file asynchronously and logs the number of students by field.

### 4. Create a small HTTP server using Node's HTTP module
Create an HTTP server in `4-http.js` that listens on port 1245 and displays "Hello Holberton School!" for any endpoint.

### 5. Create a more complex HTTP server using Node's HTTP module
Create an HTTP server in `5-http.js` that listens on port 1245, and displays different content depending on the URL path (`/` or `/students`).

### 6. Create a small HTTP server using Express
Create an HTTP server in `6-http_express.js` using Express that listens on port 1245 and displays "Hello Holberton School!" for the root endpoint.

### 7. Create a more complex HTTP server using Express
Create an HTTP server in `7-http_express.js` using Express that listens on port 1245 and handles routes `/` and `/students`.

### 8. Organize a complex HTTP server using Express
Organize your server into separate files and directories in the `full_server` folder, using ES6 modules with Babel, and creating routes and controllers.

## Tips
- **Asynchronous Callbacks:** Use them to avoid blocking the main thread in Node.js.
- **Testing:** Validate your integration by adding tests.