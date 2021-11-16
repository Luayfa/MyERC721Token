![Build Status](https://travis-ci.org/0xcert/ethereum-erc721.svg?branch=master)&nbsp;[![codecov](https://codecov.io/gh/0xcert/ethereum-erc721/branch/master/graph/badge.svg?token=F0tgRHyWSM)](https://codecov.io/gh/0xcert/ethereum-erc721)&nbsp;[![NPM Version](https://badge.fury.io/js/@0xcert%2Fethereum-erc721.svg)](https://www.npmjs.com/package/@0xcert/ethereum-erc721)&nbsp;[![Dependencies Status](https://david-dm.org/0xcert/ethereum-erc721.svg)](https://david-dm.org/0xcert/ethereum-erc721)&nbsp;[![Bug Bounty](https://img.shields.io/badge/bounty-open-2930e8.svg)](https://github.com/0xcert/ethereum-erc721/blob/master/BUG_BOUNTY.md)

# ERC-721 Token — 

This is the complete implementation of the [ERC-721](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-721.md) non-fungible token standard for the Ethereum and Wanchain blockchains. It is also compatible with other EVM compatible chains like Binance Smart Chain (BSC), Avalanche (AVAX) etc. This is an open-source project, complete with [Hardhat](https://hardhat.org/) testing.


## Structure

All contracts and tests are in the [src](src/) folder. There are multiple implementations and you can select between:

- [`nf-token.sol`](src/contracts/tokens/nf-token.sol): This is the base ERC-721 token implementation (with support for ERC-165).
- [`nf-token-metadata.sol`](src/contracts/tokens/nf-token-metadata.sol): This implements optional ERC-721 metadata features for the token contract. It implements a token name, a symbol and a distinct URI pointing to a publicly exposed ERC-721 JSON metadata file.
- [`nf-token-enumerable.sol`](src/contracts/tokens/nf-token-enumerable.sol): This implements optional ERC-721 support for enumeration. It is useful if you want to know the total supply of tokens, to query a token by index, etc.

Other files in the [tokens](src/contracts/tokens) and [utils](src/contracts/utils) directories named `erc*.sol` are interfaces and define the respective standards.

Mock contracts showing basic contract usage are available in the [mocks](src/contracts/mocks) folder.

There are also test mocks that can be seen [here](src/tests/mocks). These are specifically made to test different edge cases and behaviours and should NOT be used as a reference for implementation.

## Requirements

* NodeJS 12+ is supported
* Windows, Linux or macOS

## Installation

### npm

*This is the recommended installation method if you want to use this package in your JavaScript project.*

This project is [released as an npm module](https://www.npmjs.com/package/@0xcert/ethereum-erc721). You must install it using the `npm` command:

```
$ npm install @0xcert/ethereum-erc721@2.0.0
```

### Source

*This is the recommended installation method if you want to improve the `0xcert/ethereum-erc721` project.*

Clone this repository and install the required `npm` dependencies:

```
$ git clone git@github.com:0xcert/ethereum-erc721.git
$ cd ethereum-erc721
$ npm install
```

Make sure that everything has been set up correctly:

```
$ npm run test
```

## Usage

### npm

To interact with this package's contracts within JavaScript code, you simply need to require this package's `.json` files:

```js
const contract = require("@0xcert/ethereum-erc721/build/nf-token-enumerable.json");
console.log(contract);
```

## Validation

You can check the validity of the smart contract, the correctness of the implementation and the supported functions of the respective smart contract using the online validator at https://erc721validator.org/.

## Playground

### Ethereum - Ropsten testnet

We already deployed some contracts to the [Ropsten](https://ropsten.etherscan.io/) network. You can play with them RIGHT NOW. No need to install the software. In this test version of the contract, anybody can `mint` or `burn` tokens, so don't use it for anything important.

| Contract                                                     | Token address | Transaction hash |
| ------------------------------------------------------------ | ------------- | ---------------- |
| [`nf-token.sol`](src/contracts/tokens/nf-token.sol)          | [0xd8bbf8ceb445de814fb47547436b3cfeecadd4ec](https://ropsten.etherscan.io/address/0xd8bbf8ceb445de814fb47547436b3cfeecadd4ec)          | [0xaac94c9ce15f5e437bd452eb1847a1d03a923730824743e1f37b471db0f16f0c](https://ropsten.etherscan.io/tx/0xaac94c9ce15f5e437bd452eb1847a1d03a923730824743e1f37b471db0f16f0c)             |
| [`nf-token-metadata.sol`](src/contracts/tokens/nf-token-metadata.sol) | [0x5c007a1d8051dfda60b3692008b9e10731b67fde](https://ropsten.etherscan.io/address/0x5c007a1d8051dfda60b3692008b9e10731b67fde)          | [0x1e702503aff40ea44aa4d77801464fd90a018b7b9bad670500a6e2b3cc281d3f](https://ropsten.etherscan.io/tx/0x1e702503aff40ea44aa4d77801464fd90a018b7b9bad670500a6e2b3cc281d3f)             |
| [`nf-token-enumerable.sol`](src/contracts/tokens/nf-token-enumerable.sol) | [0x130dc43898eb2a52c9d11043a581ce4414487ed0](https://ropsten.etherscan.io/address/0x130dc43898eb2a52c9d11043a581ce4414487ed0)          | [0x8df4c9b73d43c2b255a4038eec960ca12dae9ba62709894f0d85dc90d3938280](https://ropsten.etherscan.io/tx/0x8df4c9b73d43c2b255a4038eec960ca12dae9ba62709894f0d85dc90d3938280)             |

### Wanchain - testnet

Already deployed some contracts to [testnet](http://testnet.wanscan.org/) network. No need to install software. In this test version of the contract, anybody can `mint` or `burn` tokens, so don't use it for anything important.

| Contract                                                     | Token address | Transaction hash |
| ------------------------------------------------------------ | ------------- | ---------------- |
| [`nf-token.sol`](src/contracts/tokens/nf-token.sol)          | [0x6D0eb4304026116b2A7bff3f46E9D2f320df47D9](http://testnet.wanscan.org/address/0x6D0eb4304026116b2A7bff3f46E9D2f320df47D9)          | [0x9ba7a172a50fc70433e29cfdc4fba51c37d84c8a6766686a9cfb975125196c3d](http://testnet.wanscan.org/tx/0x9ba7a172a50fc70433e29cfdc4fba51c37d84c8a6766686a9cfb975125196c3d)             |
| [`nf-token-metadata.sol`](src/contracts/tokens/nf-token-metadata.sol) | [0xF0a3852BbFC67ba9936E661fE092C93804bf1c81](http://testnet.wanscan.org/address/0xF0a3852BbFC67ba9936E661fE092C93804bf1c81)          | [0x338ca779405d39c0e0f403b01679b22603c745828211b5b2ea319affbc3e181b](http://testnet.wanscan.org/tx/0x338ca779405d39c0e0f403b01679b22603c745828211b5b2ea319affbc3e181b)             |
| [`nf-token-enumerable.sol`](src/contracts/tokens/nf-token-enumerable.sol) | [0x539d2CcBDc3Fc5D709b9d0f77CaE6a82e2fec1F3](http://testnet.wanscan.org/address/0x539d2CcBDc3Fc5D709b9d0f77CaE6a82e2fec1F3)          | [0x755886c9a9a53189550be162410b2ae2de6fc62f6791bf38599a078daf265580](http://testnet.wanscan.org/tx/0x755886c9a9a53189550be162410b2ae2de6fc62f6791bf38599a078daf265580)             |

