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





### Note: for migratation to Rinkeby

```
Starting migrations...
======================
> Network name:    'rinkeby'
> Network id:      4
> Block gas limit: 29970705


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0xd9d69fd853cf4f23272afa380c94474330431ea43d0dce47e8d49b055eed01ac
   > Blocks: 0            Seconds: 14
   > contract address:    0x0c8B78cE1E87ABd588c8c5dFAF979601094083c9
   > account:             0x69d378367AB777d4d8Ac0803dc4420265444587e
   > balance:             0.09754064
   > gas used:            245936
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00245936 ETH

   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00245936 ETH


2_deploy_contracts.js
=====================

   Deploying 'StarNotary'
   ----------------------
   > transaction hash:    0x984497a2c01a5f72a63dd858f480918e7bad6b2dac9bd620912cb1360a50d785
   > Blocks: 2            Seconds: 18
   > contract address:    0x2BD2eE20C213a5d941A9228B30Ec384f873cC5Ee
   > account:             0x69d378367AB777d4d8Ac0803dc4420265444587e
   > balance:             0.07405063
   > gas used:            2349001
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.02349001 ETH

   > Saving artifacts
   -------------------------------------
   > Total cost:          0.02349001 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.02594937 ETH


```