### assert

- assert-: same as asserion we do in unit testing, It is a module which provides various functions
- Parameters: This function accepts the following parameters as mentioned above and described below:
    1. value: This parameter holds the expression that needs to be evaluated. It is of any type.
    2. message: This parameter holds the error message of string or error type. It is an optional parameter.
- eturn Value: This function returns assertion error of object type

### buffer
In Node, Buffer is used to store and manage binary data. Pure JavaScript is great with Unicode-encoded strings, but it does not handle binary data very well. It is not problematic when we perform an operation on data at the browser level but at the time of dealing with TCP stream and performing a read-write operation on the file system is required to deal with pure binary data.

Buffer in Node is a built-in object used to perform operations on raw binary data. The buffer class allows us to handle the binary data directly.

### query string
The Query String module used to provides utilities for parsing and formatting URL query strings. It can be used to convert query string into JSON object and vice-versa. 
Query strings in Node.js are a common way to pass data to a server via a URL. A query string is the part of a URL that comes after a "?" symbol and contains key-value pairs separated by &. These strings are used in HTTP requests to send additional parameters to the server.


### timers

- Scheduling Timers: It is used to call a function after a set period of time.
1. setImmediate()
2. setInterval()
3. setTimeout()
   
- Canceling Timers: It is used to cancel the scheduled timer.
1. clearImmediate()
2. clearInterval()
3. clearTimeout()

### url
The ‘url’ module provides utilities for URL resolution and parsing. The getters and setters implement the properties of URL objects on the class prototype, and the URL class is available on the global object.

There are many classes in this module each having many methods

---

Read these docs only if interested-:
- [How V8 Engine works in NodeJS](https://www.geeksforgeeks.org/node-js/explain-v8-engine-in-node-js/)
- [Create VIrtual Machines in NodeJS](https://www.geeksforgeeks.org/node-js/nodejs-vm-module/)
