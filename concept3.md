This is important article -: [Event Loop](https://www.geeksforgeeks.org/javascript/what-is-an-event-loop-in-javascript/)  
This is important article -: [Promises](https://www.geeksforgeeks.org/javascript/javascript-promise-chaining/)  

---

NodeJS provides a set of global objects that are available in every module. These are built-in objects that can be used directly in the application without using import statements. Let’s take a look at some of the most commonly used NodeJS global objects
1. global-: The global object in NodeJS is equivalent to the window object in browsers. Any variable or function added to global becomes globally accessible across the application
2. console-: The console object is used for printing messages to standard output (stdout) or error output (stderr). It provides methods like console.log(), console.error(), and console.warn() for logging messages and debugging.
3. process-: The process object in NodeJS provides information about the currently running NodeJS process. It allows you to interact with the system, get details about the process, and control how the process runs. In simple terms, it helps you manage things like environment settings, command-line arguments, and how the application behaves during execution.
4. The Buffer class is used to deal with binary data in NodeJS. It provides a way to handle raw binary data directly in memory, allowing you to manipulate binary files or network streams.
5. __dirname and __filename-: These are global variables that represent the directory name (__dirname) and the filename (__filename) of the current module (file).
6. setTimeout and setInterval-: These functions are used to schedule the execution of code. setTimeout() runs a function after a specified delay, while setInterval() runs a function repeatedly at fixed intervals.
7. Url-: URL is used to handle URL-related operations, and URLSearchParams helps with manipulating URL query parameters.
8. TextEncoder and TextDecoder-: These classes are used for encoding and decoding text in various encodings, such as UTF-8. They are useful for working with string data that needs to be converted to binary or vice versa.

---

If you're building a NodeJS application and want to automatically restart the server whenever you make changes to your code, Nodemon is a great tool for that. It saves you time by eliminating the need to manually restart the server each time you update your code.

---

See this article for session tracking-: [Session Tracking](https://www.geeksforgeeks.org/node-js/how-to-use-session-variable-with-node-js/)







