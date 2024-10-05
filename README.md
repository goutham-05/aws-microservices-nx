# AWS Microservices with Nx

## Overview

This a monorepo project built using Yarn workspaces and Nx. It includes multiple services like `order-service` and `user-service`, utilizing Serverless Framework to deploy AWS Lambda functions and API Gateway endpoints. This project also integrates continuous integration (CI) and continuous deployment (CD) pipelines using GitHub Actions. Automated testing is implemented with Jest, and code coverage reports are generated. The project is written in TypeScript.

## Table of Contents

- [AWS Microservices with Nx](#aws-microservices-with-nx)
  - [Overview](#overview)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Project Structure](#project-structure)
  - [Installation](#installation)
- [aws-microservices-nx](#aws-microservices-nx)

## Features

- Monorepo managed with Yarn workspaces
- Services built with TypeScript and Serverless Framework
- Continuous integration and deployment with GitHub Actions
- Automated testing with Jest
- Code coverage reports

## Project Structure

aws-microservices-nx/
├── services/
│ ├── order-service/
│ │ ├── src/
│ │ │ └── handlers/
│ │ │ └── getOrder.ts
│ │ ├── project.json
│ │ ├── tsconfig.json
│ │ └── jest.config.js
│ ├── user-service/
│ │ ├── src/
│ │ │ └── handlers/
│ │ │ └── getUser.ts
│ │ ├── project.json
│ │ ├── tsconfig.json
│ │ └── jest.config.js
├── .github/
│ ├── workflows/
│ │ ├── build.yml
│ │ ├── test.yml
│ │ └── deploy.yml
├── nx.json
├── package.json
└── yarn.lock

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/goutham-05/aws-microservices-nx
   cd aws-microservices-nx

   ```

2. **Install dependencies:**:

   ```bash
   yarn install

   ```

Running Locally
To run the services locally, use the following commands:

Start the development server:

```bash
   yarn dev

```

Access the API:

Order Service: http://localhost:4001/dev/order/{id}
User Service: http://localhost:4000/dev/user/{id}

Testing
To run the tests, use:

```bash
yarn test

```

Code Coverage
To generate code coverage reports, use:

```bash
yarn test --coverage

```

Building
To build the project, use:

```bash
yarn build

```

Deploying
To deploy the services, use:

```bash
yarn deploy

```

GitHub Actions Workflows
Build Workflow
The build workflow triggers on pushes and pull requests to the develop branch. It builds the affected projects using Nx.

Test Workflow
The test workflow triggers on pushes and pull requests to the develop branch. It runs tests and generates code coverage reports for the affected projects using Jest.

Deploy Workflow
The deploy workflow triggers on pushes to the develop branch. It deploys the affected projects using the Serverless Framework.

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Create a new Pull Request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Feel free to modify this template according to your project's specifics and needs.

```bash
This `README.md` file includes all sections and detailed information to help users understand and work with your project effectively.

```

# aws-microservices-nx
