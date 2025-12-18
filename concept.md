- NodeJS operates on a single thread but efficiently handles multiple concurrent requests using an event loop.
1. Client Sends a Request: The request can be for data retrieval, file access, or database queries.
2. NodeJS Places the Request in the Event Loop: If the request is non-blocking (e.g., database fetch), it is sent to a worker thread without blocking execution.
3. Asynchronous Operations Continue in Background: While waiting for a response, NodeJS processes other tasks.
4. Callback Execution: Once the operation completes, the callback function executes, and the response is sent back to the client.

---

- NPM stands for Node Package Manager. When we install Node.js, it automatically installs NPM. When we are making any new project, we have to make a command in the terminal, such as

npm init   // init stands for initialization

- It will create a package.json File. It records important metadata about a project, which is required before publishing to NPM, and also defines functional attributes of a project that NPM uses to install dependencies, run scripts, and identify the entry point to our package.

---

## Follow Step-by-Step to send Request to Node.js Server
1. The client sends a request to the Node.js web server to interact with the web application.
2. The request can be either blocking (synchronous) or non-blocking (asynchronous). Node.js receives the request and adds it to the Event Queue. Requests from different users (User 1, 2, 3, etc.) are added to the Event Queue.
3. Requests are picked in (FIFO – First In, First Out) order. If the request is non-blocking, it is processed immediately, and the response is sent back to the client. If the request is a blocking operation, it is passed to the Thread Pool.
4. The Thread Pool has a limited number of threads. If a thread is free, the blocking task is assigned to it.
5. Once the task is completed, the thread returns the result back to the Event Loop, which then sends the response to the client.
6. If all threads are busy, any new blocking requests must wait in a queue until a thread becomes free.
7. This waiting increases the response time for the client. Therefore, it is always better to avoid blocking operations and use non-blocking alternatives whenever possible to maintain performance and scalability.

---

#### Blocking or Synchronous Operation
In a blocking or synchronous operation, tasks are executed one at a time in a specific sequence. The program waits for the current task to complete before moving on to the next one. This means if a task takes time—like reading a file or making a network request—the entire program waits until that task finishes. While this approach is simple and easy to understand, it can slow down performance, especially when handling multiple requests or time-consuming operations

#### Non-Blocking or Asynchronous Operation
In a non-blocking or asynchronous operation, tasks are executed without waiting for the previous one to finish. Instead of pausing the program, long-running operations like file reading or API calls are handled in the background. Once the task is complete, a callback or promise is used to handle the result. This approach allows the program to stay responsive and handle multiple tasks at the same time, making it ideal for high-performance and real-time applications like web servers.

---

- NPM (Node Package Manager) is a package manager for NodeJS modules. It helps developers manage project dependencies, scripts, and third-party libraries. By installing NodeJS on your system, NPM is automatically installed and ready to use.
- so install both node as well as its package manager npm
- some important packages are -: express, mongoos, lodash, axios, react etc


---

### Modules in NodeJS
NodeJS is built around the concept of modules. Modules in NodeJS are reusable pieces of code that can be imported into your application. These can be built-in modules (like fs for file system operations, http for HTTP server, etc.) or external packages installed using NPM.  

Common NodeJS Modules-: 

- HTTP Module: The http module is used to create web servers. It allows you to handle requests and send responses.
- FS (File System) Module: The fs module provides an API to interact with the file system. It can be used to read and write files, check for file existence, etc.
- Path Module: The path module helps in handling and transforming file paths. It makes working with file systems easier and more cross-platform.
- Event Module: The events module allows objects to emit and listen to events, which helps in writing event-driven applications.
- Express Framework: While NodeJS provides basic capabilities, many developers use the Express framework, which simplifies routing, middleware integration, and HTTP request handling.


