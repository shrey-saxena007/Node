### Creating First Application 

1. Step 1: Initialize a NodeJS Project
     mkdir my-node-app
     cd my-node-app
     npm init -y
2. Step 2: Install Required Modules
3. Step 3: Create an index.js File
        import http from "http";
        import fs from "fs";
        import path from "path";
        import { fileURLToPath } from "url";
        
        const __filename = fileURLToPath(import.meta.url);
        const __dirname = path.dirname(__filename);
        
        const server = http.createServer((req, res) => {
            const filePath = path.join(__dirname, "message.txt");
        
            fs.readFile(filePath, "utf8", (err, data) => {
                if (err) {
                    res.writeHead(500, { "Content-Type": "text/plain" });
                    res.end("Error reading file");
                } else {
                    res.writeHead(200, { "Content-Type": "text/plain" });
                    res.end(data);
                }
            });
        });
        
        server.listen(3000, () => {
            console.log("Server is running on port 3000");
        });

4. type node index.js to run the file

---

NodeJS REPL (Read-Eval-Print Loop) is an interactive shell that allows you to execute JavaScript code line-by-line and see immediate results. This tool is extremely useful for quick testing, debugging, and learning, providing a sandbox where you can experiment with JavaScript code in a NodeJS environment.

---

### Types of Modules:
- Core Modules: Core modules are built-in modules provided by NodeJS. They offer essential functionalities such as file system operations (fs), HTTP server (http), and utilities (util). Core modules can be accessed using the require() function without specifying a path. So the modues are-: fs(File System), http and https, events, path, util, os(operating system), crypto(cryptography)
``const fs = require('fs');`
- Third-Party Modules: Third-party modules are created by the NodeJS community or external developers and are hosted on package registries like npm (Node Package Manager). Developers can install third-party modules using npm and include them in their applications using require().
npm install package-name
const package = require('package-name');
- Custom Modules: Custom modules are user-defined modules created by developers to encapsulate reusable code. Developers can create custom modules by defining functions, objects, or classes in separate files and exporting them using the module.exports or exports object.



