## Truffle console

Ref: https://trufflesuite.com/docs/truffle/getting-started/interacting-with-your-contracts/
API Ref: https://github.com/trufflesuite/truffle/tree/master/packages/contract

#### Enter to truffle console
```
truffle console
```

#### Create contract
```
truffle(develop)> let instance = await StarNotary.deployed()
truffle(develop)> instance
```

#### Create accounts
```
let accounts = await web3.eth.getAccounts()
```

#### Create Star
```
instance.createStar('Starname 1', 1, {from: accounts[0]})
```

#### LookUptokenIdToStarInfo
```
let starName = await instance.lookUptokenIdToStarInfo(1)
starName
```

#### Call public variables
```
let tokenName = await instance.name.call()
let tokenSymbol = await instance.symbol.call()
tokenName
tokenSymbol
```