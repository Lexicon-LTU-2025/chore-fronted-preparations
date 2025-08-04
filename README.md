# Preparatory Chore: NVM, Vite JS and TypeScript Setup

<details open>
<summary>Table of contents</summary>

- [Node JS](#node-js)

  - [Key features of Node](#key-features-of-node)
  - [NVM Node Version Manager](#nvm---node-version-manager)
  - [Uninstall Node](#uninstall-node)
  - [Install NVM](#install-nvm)

- [NVM (Node Version Manager)](#nvm-node-version-manager)

  - [Installing NVM](#installing-nvm)

- [Vite JS](#vite-js)

  - [About Vite](#about-vite)
  - [Starting a Vite Project](#starting-a-vite-project)

- [TypeScript Introduction](#typescript-introduction)
  - [Why TypeScript?](#why-typescript)
  - [What problems does TypeScript solves?](#what-problems-does-typescript-solves)

</details>

## Node JS

Before we can use Vite, we need to install **Node.js**. Vite relies on Node for tasks like installing dependencies, running the dev server, and building the project for production. But Node itself is also a powerful tool every frontend developer should have.

**Node.js** is an open-source, cross-platform JavaScript runtime environment that allows developers to run JavaScript code outside the browser.

[Node JS Homepage](https://nodejs.org/en)

### Key Features of Node

1. **Server-Side JavaScript:** Run JavaScript on the server.

2. **Node Package Manager ( `npm` )**: Used to install, manage, and share JavaScript libraries. This is key for installing Vite.

3. **Single Page Application (SPA) Support**: Node is commonly used as a backend for SPAs.

4. **Web Servers**: Use frameworks like Express.js to create APIs and servers.

For us, the most important feature is `npm`.

---

### NVM - Node Version Manager

**NVM** is a tool that lets you install and manage multiple Node.js versions. This is useful when switching between projects that require different versions of Node.

⚠️ If you already have Node installed, you must uninstall it before installing NVM.

---

### Uninstall Node

#### Check if Node is already installed:

```bash
node --version
```

If a version shows up, uninstall it:

#### Windows:

- [GeeksForGeeks Guide](https://www.geeksforgeeks.org/how-to-completely-remove-node-js-from-windows/)
- [Codedamn Guide](https://codedamn.com/news/nodejs/how-to-uninstall-node-js)

#### macOS:

- [StackAbuse Guide](https://stackabuse.com/how-to-uninstall-node-js-from-mac-osx/)
- [iMyMac Guide](https://www.imymac.com/powermymac/uninstall-node-mac.html)

[Back to top](#preparatory-exercise-nvm-vite-js-and-typescript-setup)

---

### Install NVM

#### macOS

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

[Official NVM for macOS/Linux](https://github.com/nvm-sh/nvm#installing-and-updating)

#### Windows

[Install NVM for Windows](https://github.com/coreybutler/nvm-windows/releases)

[Installation Guide (XDA)](https://www.xda-developers.com/how-install-nvm-windows/)

After NVM is installed, close and reopen your terminal and run:

```bash
nvm install --lts
nvm use --lts
```

This installs the latest LTS version of Node and sets it as the default.

[Back to top](#preparatory-exercise-nvm-vite-js-and-typescript-setup)

## Vite JS

With NVM and Node installed, you’re ready to set up **Vite**.

[Vite JS Homepage](https://vitejs.dev/)

### About Vite

Vite.js is a build tool for modern web development that focuses on providing a fast development experience. It is particularly well-suited for building web applications using modern JavaScript frameworks like Vue.js, React, and others. Vite.js is designed to leverage the native ES module system and provides a development server with features like hot module replacement (HMR) to enhance the development workflow.

If ES moduels is a new term for you, read more about them here:

[Introduction to ES Modules](https://flaviocopes.com/es-modules/)

[ES modules: A cartoon deep-dive](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)

`vite` is usually directly comapared to webpack which is also a build tool used in frontend development, but I am not going to go through and compare them here. If you are interested there are countless articles on the web about it. But I can say that `Vite` is designed to provide a faster and more streamlined development experience then webpack.

To start a `Vite` project you just have to open up a terminal in the folder where you want to place your project and type in this command:

[Back to top](#preparatory-exercise-nvm-vite-js-and-typescript-setup)

### Starting a Vite Project

1. Open your terminal in the folder where you want your project
2. Run:

```bash
npm create vite@latest
```

3. Follow the prompts:

   - Project name
   - Framework → `Vanilla`
   - Variant → `TypeScript`

Then:

```bash
cd your-project-folder
npm install
npm run dev
```

Your Vite dev server should now be running. Try it put! 🚀

[Back to top](#preparatory-exercise-nvm-vite-js-and-typescript-setup)

## TypeScript Introduction

**TypeScript** is a typed superset of JavaScript created to make large-scale development more robust. Since most of you have experience with **C#**, you’ll notice similarities:

| Concept          | C# Example              | TypeScript Equivalent             |
| ---------------- | ----------------------- | --------------------------------- |
| Type annotations | `int count = 0;`        | `const count: number = 0;`        |
| Interfaces       | `interface IPerson {}`  | `interface IPerson {}`            |
| Enums            | `enum Status { Ready }` | `enum Status { Ready }`           |
| Nullable types   | `string? name = null;`  | `let name: string \| null = null` |

### Why TypeScript?

TypeScript helps solve common problems in JavaScript by providing:

[TypeScript Homepage](https://www.typescriptlang.org/)

### What problems does TypeScript solves?

1. **Static Typing:**

   - **Problem in JavaScript:** JavaScript is a dynamically-typed language, which means variable types are determined at runtime. This lack of static typing can lead to runtime errors and make it harder for developers to catch certain types of bugs during development.
   - **Solution in TypeScript:** TypeScript introduces static typing, allowing developers to define and enforce types for variables, function parameters, and return values. This helps catch type-related errors early in the development process and provides better tooling support for code editors.

2. **Code Maintainability:**

   - **Problem in JavaScript:** In large and complex codebases, understanding and maintaining code can become challenging, especially when dealing with untyped or loosely typed code.
   - **Solution in TypeScript:** With static typing, TypeScript provides better code documentation and readability. Developers can understand the types of variables and functions just by looking at the code, making it easier to maintain and refactor.

3. **Tooling and IDE Support:**

   - **Problem in JavaScript:** JavaScript lacks comprehensive tooling support due to its dynamic nature. IDEs may have limited capabilities in terms of autocompletion, type checking, and refactoring.
   - **Solution in TypeScript:** TypeScript comes with a rich set of tooling features. IDEs can offer intelligent autocompletion, real-time error checking, and enhanced refactoring support because TypeScript provides clear type information.

4. **Enhanced Developer Experience:**

   - **Problem in JavaScript:** Developers often rely on runtime checks and debugging to identify type-related issues in JavaScript, which can be time-consuming.
   - **Solution in TypeScript:** TypeScript allows developers to catch and fix errors at compile-time rather than runtime. This results in a more pleasant development experience with fewer surprises during execution.

5. **Interfaces and Type Annotations:**

   - **Problem in JavaScript:** JavaScript lacks built-in constructs for defining interfaces and complex types explicitly.
   - **Solution in TypeScript:** TypeScript introduces interfaces and type annotations, allowing developers to define custom types, structures, and contracts. This promotes better code organization, documentation, and collaboration.

6. **Code Quality and Readability:**

   - **Problem in JavaScript:** Without type information, it can be challenging to ensure that functions are used correctly, leading to potential bugs.
   - **Solution in TypeScript:** TypeScript helps improve code quality by providing a mechanism for expressing and enforcing contracts between different parts of the code. This can lead to more robust and reliable applications.

[Back to top](#preparatory-exercise-nvm-vite-js-and-typescript-setup)
