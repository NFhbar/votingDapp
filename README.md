# votingDapp

Simple voting dapp with blockchain explorer.
Original code by:

[Mahesh Murthy](https://github.com/maheshmurthy/ethereum_voting_dapp)


## Changes
Added a simple blockchain explorer for testrpc

## Install
You need [npm](https://docs.npmjs.com/cli/install), [node](https://nodejs.org/en/download/package-manager/), and [solidity](http://solidity.readthedocs.io/en/develop/installing-solidity.html).

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
```

### Compile Contract
```
> code = fs.readFileSync('Voting.sol').toString()
> solc = require('solc')
> compiledCode = solc.compile(code)
```

### Deploy Contract
```
> abiDefinition = JSON.parse(compiledCode.contracts[':Voting'].interface)
> VotingContract = web3.eth.contract(abiDefinition)
> byteCode = compiledCode.contracts[':Voting'].bytecode
> deployedContract = VotingContract.new(['Mada','Nick','Jay'],{data: byteCode, from: web3.eth.accounts[0], gas: 4700000})
> deployedContract.address
> contractInstance = VotingContract.at(deployedContract.address)
```

### Check your Account
```
> web3.eth.accounts
```
Replace output in [index.js line 6](https://github.com/NFhbar/votingDapp/blob/master/index.js#L6)

### To Run
Execute:
[index.html](https://github.com/NFhbar/votingDapp/blob/master/index.html)

### Terminal
To interact with the contract via terminal, type:
```
> contractInstance.
```
and press TAB to see list of possible commands.
