# MERN Stack Template

This repository contains a comprehensive template for building applications using the MERN stack (MongoDB, Express.js, React, Node.js). It includes a well-structured project setup, essential configurations, and best practices to kickstart your development process. Perfect for developers looking to streamline their workflow and ensure consistency across projects.

# Build
scripts Json file:
```json
  "scripts": {
    "build": "if-env TYPE=server && (cd server && npm install) || (cd client &&  npm install)",
    "build-pnpm": "if-env TYPE=server && (cd server && pnpm install) || (cd client &&  pnpm install) ",
    "server": " node ./server/server.js ",
    "client": " cd client && npm start "
  },
```
## requirements:
- if-env package
in root directory run the following command:
```bash
npm i if-env
```

to modify the build command change the `script` section in package.json in root directory. current one will run this command:
```json
"build": "if-env TYPE=server && (cd server && npm install) || (cd client &&  npm install)",
```
Personally i use `pnpm` for local test enlivenments, so i have added a new command for that too:
```json
"build-pnpm": "if-env TYPE=server && (cd server && pnpm install) || (cd client &&  pnpm install) "
```

# Run Project
running the serve side:

running the client side: