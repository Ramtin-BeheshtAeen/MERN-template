# MERN Stack Template

This repository contains a comprehensive template for building applications using the MERN stack (MongoDB, Express.js, React, Node.js). It includes a well-structured project setup, essential configurations, and best practices to kickstart your development process. Perfect for developers looking to streamline their workflow and ensure consistency across projects.

# requirements:
- if-env package

# Build
first clone this project to the new projects folder using the following commad:
```bash
git clone [address of this project]
```
then copy all the files from `MERN_template` folder to the current directory and delete the `MERN_template` folder:
```bash
cp -r MERN-template/* .
```
if you want to copy it to other location, replace the dot with that specific location.
and finially delete the `MERN_template` folder
```bash
rm rf MERN-template/
```
install `if-env package`:
in root directory run the following command:
```bash
npm i if-env
```
build server and client side(this will install all requierd node modules):
if you are using pnpm use:
```bash
npm run build-pnpm
```
otherweise run this comand:
```bash
npm run build
```


## explanations:
`scripts` section of `package.json` file:
```json
  "scripts": {
    "build": "if-env TYPE=server && (cd server && npm install) || (cd client &&  npm install)",
    "build-pnpm": "if-env TYPE=server && (cd server && pnpm install) || (cd client &&  pnpm install) ",
    "server": " node ./server/server.js ",
    "client": " cd client && npm run dev "
  },
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
## running the serve side:
```bash
npm run server
```
modify this script, for your optimal result:
```json
"server": " node ./server/server.js ",
```

## running the client side:
```bash
npm run client
```
because Vite template has been used, this script will be used:
```json
"client": " cd client && npm run dev "
```

otherwise, replace it with:
```json
"client": " cd client && npm start "
```
