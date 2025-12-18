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
