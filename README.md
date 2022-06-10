# Solidity template

Quickly get up and running with a powerful Solidity project in no time.

## ✨ Tech stack used

- Hardhat - Tooling for compiling, deploying and testing smart contracts.
- Ethers - Library with Ethereum and Wallet implementations.
- Waffle and Chai - For testing the smart contracts comprehensively.
- Solhint and Prettier - For linting and formatting of the code.
- Hardhat Gas reporter - For reporting gas usage of the smart contracts during testing.
- Typechain - For generating type definitions for the smart contracts.
- Slither - For static analysis of the smart contracts for optimizations and possible vulnerabilities.

## 👇 Pre-requisites

Ensure that you have the following tools ready and installed to use this:

- Git
- Node.js

Setup the environmental variables if you haven't yet.

You can setup the `.env` variables based on the `.env.example` file as provided. Setup the file using
`cp .env.example .env` and fill in the values.

## 🛠 Usage

Quickly get started by installing the dependencies.

```sh
npm install -D
# OR
yarn
```

**NOTE** Any contracts written should use the `0.8.0` or a specific minor-version pragma in order to retain
backwards compatibility with all the versions of the compiler with same minor release.

### Build the project

You can build the project using the following commands.

If you're not using this as a library:

```sh
yarn run build
```

If you are using this as a library:

**NOTE** This runs the build command, and transpiles typescript typechain output to javascript.

```sh
yarn run build:lib
```

### Linting and formatting

Linting and formatting is provided by the solhint and prettier packages respectively.

You can lint/format the whole project as so:

```sh
# Linting
yarn run lint

# Formatting
yarn run format
```

### Testing

The project ships with a simple test suite. You can add your own as you work on more contracts. The gas reporter runs along with tests if enabled.

Run the tests as so:

```sh
yarn run test
```

### Analyzing the contracts

The project utilizes [Slither](https://github.com/crytic/slither) for performing static analysis of the smart contracts.

To use this, you need to install it first. Ensure you have Python3 on your system, then run:

```sh
pip install slither-analyzer
```

If you're good to go, run the following command to analyze the smart contracts:

```sh
yarn run analyze
```

### Clean up project

A script has been provided to clean up artifacts, cache, typechain output and ABIs copied.

```sh
yarn run clean
```

### Tasks

Hardhat scripts and tasks are present in their respective folders.

You can run any hardhat scripts using:

```sh
npx hardhat run scripts/path/to/script
```

Replace `/path/to/script` with the actual path to script file.

The tasks can be run using the same manner.

```sh
npx hardhat <task-name>
```

Where `task-name` is the unique identifier for a task. They're defined when creating a task, such as
`accounts` is one of the tasks present.

You can create your own scripts & tasks in the same manner by referring to the hardhat documentation on them.

## Contributing

Contributions, issues and feature requests are welcome. After cloning & setting up project locally, you
can just submit a PR to this repo and it will be deployed once it's accepted.

⚠️ It’s good to have descriptive commit messages, or PR titles so that other contributors can understand about your
commit or the PR Created. Read [conventional commits](https://www.conventionalcommits.org/en/v1.0.0-beta.3/)
before making the commit message.

## Show your support

We love people's support in growing and improving. Be sure to leave a ⭐️ if you like the project and
also be sure to contribute, if you're interested!

<div align="center">Made by Sunrit Jana with ❤</div>
