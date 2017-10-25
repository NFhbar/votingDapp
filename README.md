# votingDapp

Simple voting dapp with blockchain explorer.
Original code by:

[Mahesh Murthy](https://github.com/maheshmurthy/ethereum_voting_dapp)


## Changes
Added a simple blockchain explorer for testrpc

## Install
You need [npm](https://docs.npmjs.com/cli/install) and [node](https://nodejs.org/en/download/package-manager/).

### Testrpc
In terminal:

```
npm install ethereumjs-testrpc web3@0.20.1
$ node_modules/.bin/testrpc
```

### Web3
Open new terminal
cd into project folder
```
$ node
> Web3 = require('web3')
> web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));




