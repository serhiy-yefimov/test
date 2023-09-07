### 1. Install typescript

`npm i typescript`

### 2. Create a TypeScript Configuration File (Optional)

You can create a `tsconfig.json` file in your project's root directory to configure TypeScript settings. This file specifies compiler options, file inclusion/exclusion patterns, and more. If you don't create a `tsconfig.json` file, TypeScript will use default settings.

You can generate a basic `tsconfig.json` file using:  
`tsc --init`

#### Configure Compilation Options

Here are a few common options you might want to set:

- `"outDir"`: Specifies the output directory for compiled JavaScript files.
- `"rootDir"`: Specifies the root directory of your TypeScript source files.
- `"target"`: Specifies the ECMAScript target version.
- `"module"`: Specifies the module system to use (e.g., "commonjs", "es6").
- `"strict"`: Enforces strict type checking.
- `"include"`: Specifies which files to include in compilation (can use glob patterns).
- `"exclude"`: Specifies which files to exclude from compilation (can use glob patterns).

  Here's an example of a `tsconfig.json` file:

  ```
  {
  "compilerOptions": {
    "outDir": "./dist",
    "rootDir": "./src",
    "target": "ES2020",
    "module": "ESNext",
    "strict": true
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules"]
  }
  ```

### 3. Compile TypeScript to JavaScript

Use the TypeScript compiler (`tsc`) to compile your TypeScript code into JavaScript:
`tsc index.ts`

If you have a `tsconfig.json` file with the appropriate settings, TypeScript will automatically compile the `.ts` files in the `src` folder and output the compiled JavaScript files into the `dist` folder.

If you don't have a `tsconfig.json` file, you can directly compile `index.ts` using the command:
`tsc src/index.ts --outDir dist`
