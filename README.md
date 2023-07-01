# express-setup-with-ts

How I setup my nodejs with express projects to work with typescript

➜ Generate the `package.json` file using

```cmd
npm init -y
```

➜ Generate the `tsconfig.json` file using

```cmd
tsc --init
```

➜ Install two packages I usually use them

```cmd
npm install concurrently nodemon
```

➜ Create a `src` & `build` folders

➜ Open the `tsconfig.json` file and uncomment the following:

```json
    "rootDir": "./src" /* Specify the root folder within your source files. */,
    "outDir": "./build" /* Specify an output folder for all emitted files. */,
```

➜ Open the `package.json` file and add the following inside the `"scripts"` tag:

```json
"scripts": {
    "start:build": "tsc -w",
    "start:run" : "nodemon build/index.js",
    "start": "concurrently npm:start:*"
}

```
