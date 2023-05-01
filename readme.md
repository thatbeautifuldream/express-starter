# Express Starter Kit

> A boilerplate for building web applications with [Express](http://expressjs.com/). ⚠️ This project is in active development and is not yet ready for production use. This template will be updated as the project matures and my learnings about various industry practices. This project is an active fork of the implemetations by [Sanket Singh](https://github.com/singhsanket143)'s [repository](https://github.com/singhsanket143/Base-Node-Project-Template).

[![image](https://user-images.githubusercontent.com/28717686/235532155-6878d8f4-ec14-4c9d-84a7-aa9fa0afaadf.png)](https://github.com/thatbeautifuldream/express-starter)

## Features

- **No configuration.** Start developing instantly.
- **No lock-in.** Easily migrate to other tools and frameworks.
- **No boilerplate.** Start with a blank canvas with just bare minimum code to setup the server.
- **No bloat.** Only the bare minimum dependencies to get you started.
- **No black box.** Understand every line of code and customize it to your needs.
- **No legacy.** Uses the latest version of Express and Node.js.

## Getting Started

### Prerequisites

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en/)
- [VS Code](https://code.visualstudio.com/)
- [Yarn](https://yarnpkg.com/en/) (optional)
- [Pnpm](https://pnpm.js.org/) (optional)

### Installation

- Clone the repository

```bash
git clone <repository-url>
```

- Delete the existing git repository

```bash
rm -rf .git
```

- Initialize a new git repository

```bash
git init
```

- Install dependencies using npm or your favorite package manager

```bash
npm install
```

- Setup environment variables in the .env file at `src/.env` path with contents as follows

```bash
PORT=5000
```

- Initialise the project with sequelize, which may create a config, migrations, models and seeders folder

```bash
npx sequelize-cli init
```

- Start the development server

```bash
npm run dev
```

## Project Structure and Conventions

> This is a base node js project template, which anyone can use as it has been prepared, by keeping some of the most important code principles and project management recommendations. Feel free to change anything.

- `src` -> Inside the src folder all the actual source code regarding the project will reside, this will not include any kind of tests. (You might want to make separate tests folder)

Lets take a look inside the `src` folder

- `config` -> In this folder anything and everything regarding any configurations or setup of a library or module will be done. For example: setting up `dotenv` so that we can use the environment variables anywhere in a cleaner fashion, this is done in the `server-config.js`. One more example can be to setup you logging library that can help you to prepare meaningful logs, so configuration for this library should also be done here.

- `routes` -> In the routes folder, we register a route and the corresponding middleware and controllers to it.

- `middlewares` -> they are just going to intercept the incoming requests where we can write our validators, authenticators etc.

- `controllers` -> they are kind of the last middlewares as post them you call you business layer to execute the budiness logic. In controllers we just receive the incoming requests and data and then pass it to the business layer, and once business layer returns an output, we structure the API response in controllers and send the output.

- `repositories` -> this folder contains all the logic using which we interact the DB by writing queries, all the raw queries or ORM queries will go here.

- `services` -> contains the buiness logic and interacts with repositories for data from the database

- `utils` -> contains helper methods, error classes etc.

- `index.js` -> this is the entry point of the application, where we start the server and register all the routes and middlewares.

- `rest.http` -> this is a file which contains all the API endpoints and their request and response bodies, this file can be used to test the APIs using the REST client extension in VS Code.

## Package Dependencies

- [Express](https://expressjs.com/) - Fast, unopinionated, minimalist web framework for Node.js
- [Sequelize](https://sequelize.org/) - Sequelize is a promise-based Node.js ORM for Postgres, MySQL, MariaDB, SQLite and Microsoft SQL Server.
- [Sequelize CLI](https://www.npmjs.com/package/sequelize-cli) - The Sequelize Command Line Interface (CLI)
- [Morgan](https://www.npmjs.com/package/morgan) - HTTP request logger middleware for node.js
- [Dotenv](https://www.npmjs.com/package/dotenv) - Dotenv is a zero-dependency module that loads environment variables from a .env file into process.env
- [Nodemon](https://www.npmjs.com/package/nodemon) - Nodemon is a tool that helps develop node.js based applications by automatically restarting the node application when file changes in the directory are detected.
- [Prettier](https://prettier.io/) - Prettier is an opinionated code formatter.
- [ESLint](https://eslint.org/) - ESLint is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs.
- [Jest](https://jestjs.io/) - Jest is a delightful JavaScript Testing Framework with a focus on simplicity.
- [HTTP Status Codes](https://www.npmjs.com/package/http-status-codes) - Constants enumerating the HTTP status codes.
- [Winston](https://www.npmjs.com/package/winston) - A logger for just about everything.
