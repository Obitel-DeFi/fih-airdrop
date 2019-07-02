# Smart Contract Box

[![Build Status](https://travis-ci.org/bc1tech/fih-airdrop.svg?branch=master)](https://travis-ci.org/bc1tech/fih-airdrop) 
[![Coverage Status](https://coveralls.io/repos/github/bc1tech/fih-airdrop/badge.svg)](https://coveralls.io/github/bc1tech/fih-airdrop)
[![MIT licensed](https://img.shields.io/github/license/bc1tech/fih-airdrop.svg)](https://github.com/bc1tech/fih-airdrop/blob/master/LICENSE)


Smart Contracts and scripts to manage FIH token AirDrop issued by FidelityHouse International SA.

Code created using [Open Zeppelin (openzeppelin-solidity)](https://github.com/OpenZeppelin/openzeppelin-solidity) and [Truffle Framework](https://github.com/trufflesuite/truffle).

## Development

### Install dependencies

```bash
npm install
```

## Usage

Open the Truffle console

```bash
npm run console
```

### Compile

```bash
npm run compile
```

### Test 

```bash
npm run test 
```

### Code Coverage

```bash
npm run coverage
```

## Linter

Use Solhint

```bash
npm run lint:sol
```

Use ESLint

```bash
npm run lint:js
```

Use ESLint and fix

```bash
npm run lint:fix
```

## Flattener

This allow to flatten the code into a single file

Edit `scripts/flat.sh` to add your contracts

```bash
npm run flat
```

## Analysis

Note: it is better to analyze the flattened code to have a bigger overview on the entire codebase. So run the flattener first.

### Describe

The `describe` command shows a summary of the contracts and methods in the files provided

```bash
surya describe dist/AirDrop.dist.sol
```

### Dependencies

The `dependencies` command outputs the c3-linearization of a given contract's inheirtance graph. Contracts will be listed starting with most-derived, ie. if the same function is defined in more than one contract, the solidity compiler will use the definition in whichever contract is listed first.

```bash
surya dependencies AirDrop dist/AirDrop.dist.sol
```
### Generate Report

Edit `scripts/analyze.sh` to add your contracts 

```bash
npm run analyze
```

The `inheritance` command outputs a DOT-formatted graph of the inheritance tree.

The `graph` command outputs a DOT-formatted graph of the control flow.

The `mdreport` command creates a markdown description report with tables comprising information about the system's files, contracts and their functions.


## License

Code released under the [MIT License](https://github.com/bc1tech/fih-airdrop/blob/master/LICENSE).