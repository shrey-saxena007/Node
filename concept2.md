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

   



