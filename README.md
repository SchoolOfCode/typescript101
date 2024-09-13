
# Working with TypeScript

Follow these steps in order 



- Click the Fork button at the top-right corner of the repository page to create a copy under your GitHub account.
- Clone your fork to your local machine using git clone URL_OF_YOUR_FORK and start working on your changes.

## TypeScript Setup Guide

This guide will walk you through setting up a TypeScript project, configuring TypeScript, and compiling a simple TypeScript file.

## Steps

### 1. Install TypeScript

First, install TypeScript globally using npm:

```bash
npm install -g typescript

```


### 2. Create a TypeScript File

Create a file named `index.ts` with the following content:

```typescript
let message: string = "Hello, TypeScript!";
console.log(message);

```

### 3. Initialize TypeScript Configuration

Generate a `tsconfig.json` file in your project directory by running in Bash:

```bash
tsc --init
```

### 4. Configure `tsconfig.json`
Open the `tsconfig.json` file and update it with the following configuration:  

Tips:

(1)  Search for the keys and if they are commented out, get rid of the comment (activate it)

(2) Create an include property outside of compilerOptions

```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "outDir": "./dist"
  },
  "include": ["index.ts"]
}

```

### 5.  Compile TypeScript

Compile the TypeScript file to JavaScript by running:

``` bash
tsc
```

### 6. Run the Compiled Code

Execute the compiled JavaScript file located in the `dist` folder with:

```bash
node dist/index.js
```

