# Functional tests
Tests are conducted on the Kovan test network, February 2 - 6, 2018, @Bruce Li

<br>

# Gifto.sol

### Contract owner can:

* Start Sale period when deploy the contract
* Pause/unpause Sales during Sale period
* Turn on tradable
* Set purchasing price, ICO percent, maximum buying amount
* Add/remove a new investor to/from the investor list
* Transfer an investor's tokens to others
* Withdraw ether in the contract

### Investor can:

* Buy Gifto tokens with ETH
* Transfer their own tokens to others
* Set allowance for his own account to withdraw a specific amount of tokens and transfer to spender's account
* Withdraw tokens from another investor's account under his allowance

### Stranger can:

* Check balance of any account
* Check ETH deposit of any investor
* Check allowance of any account

<br>

## Periods
* Sales starts when the contract being deployed
* Pause/unpause sales are totally controled manually by the contract owner

<br>

## Accounts

* Contract owner [0x00812974cb8afa7fFA5081922C0f46B5a82cEA28](https://kovan.etherscan.io/address/0x00812974cb8afa7fFA5081922C0f46B5a82cEA28)

* Investor [0x0089E6eb5786e7dB31f3e2521313a502fA9596d3](https://kovan.etherscan.io/address/0x0089E6eb5786e7dB31f3e2521313a502fA9596d3)

* Stranger - Non-investor [0x006b942E2Eb0981AB083F7c680c3E43Ca5Fd7bDb](https://kovan.etherscan.io/address/0x006b942E2Eb0981AB083F7c680c3E43Ca5Fd7bDb)

<br>

## Expected behaviour tests

### Contract owner
 - [x] Contract created and deployed[0x75e9a2](https://kovan.etherscan.io/tx/0x75e9a21c1bfa45fff74332e3d30d782b370c254f6a2c713c92c02b2b07956325) 
 - [x] Pause Sales during Sale period [0x88b5ad](https://kovan.etherscan.io/tx/0x88b5ad5145a84744c70269a0fe06680bbba044b1de28390c3b4564448dfb1975)
 - [x] Unpause sales during sale period [0xc5d3c6](https://kovan.etherscan.io/tx/0xc5d3c604ff9d9d77a7f154b5d583f0fb0d6e6d91323b23a46ea4fafcac56845d)
 - [x] Start tradable period [0xc81211](https://kovan.etherscan.io/tx/0xc81211612c8b5614e875be14c8a02ab48601ca86501b00f46e50f7ac9191cc6e)
 - [x] Set perchase price [0xb93487](https://kovan.etherscan.io/tx/0xb934875bf608b85a6f2a62eea3bcdb3e09f48dff2968e9e27573591a8df3f57f)
 - [x] Set ICO percentage [0x6843f3](https://kovan.etherscan.io/tx/0x6843f39765dc2bb37c6fb7bb64dd83564cd9c73f4b4ff853ade6899e2e2a6f0f) 
 - [x] Set maximum buying amount [0x580e8d](https://kovan.etherscan.io/tx/0x580e8d2ebb8dfff62ff22fd77f715727882a9dcbcd8737aa0d036e95ffb3bf98)
 - [x] Add investor [0x0ea900](https://kovan.etherscan.io/tx/0x0ea90040b32bd6f500e0f467e9a1972754edce1b103ddd2433edcc1f76793633)
 - [x] Remove investor [0x60c3cc](https://kovan.etherscan.io/tx/0x60c3cc9a287e72a57950e0e499a17edeb4ada67d010cf39af4d9ce1db5fb55b3)


### Investor
 - [x] Buy Gifto tokens [0x88dc1d](https://kovan.etherscan.io/tx/0x88dc1d0890512f8d825cd4634b6277c98beffa2dee32a352491d809421120d20)
 - [x] Transfer their tokens to some one else [0x2a2935](https://kovan.etherscan.io/tx/0x2a293534127fe212a137dfaf063ab17c174b78c9d43edd2c9001d7865c5296f0)
 - [x] Approve allowance [0x88f15c](https://kovan.etherscan.io/tx/0x88f15cf4ba931888a4c2a713e67ccb231b6d0876fe26319dbafaa629ffe84657)
 - [x] Withdraw tokens from another investor's account under his allowance [0xd68b59](https://kovan.etherscan.io/tx/0xd68b5995129002c6804e2c1114ca0566cfcb7b89a913d035977cbe395f3ac05c)
 
### Stranger
 - [x] Check balance of any account
 - [x] Check ETH deposit of any investor
 - [x] Check allowance of any account

<br>

## Unexpected behaviour tests (reverted)

### Contract owner
 - [×] Turn on sales when it is already on.[0x06a246](https://kovan.etherscan.io/tx/0x06a246d6e7cecc2d9223dea578472431b0ffec77f9c8c6d3810f14aa23b67d5c)
 Suggest to verify the variable status before turn it on. Or you just lose your gas if it is already on.
 - [×] Turn off sales when it is already off.[0x06a246](https://kovan.etherscan.io/tx/0x06a246d6e7cecc2d9223dea578472431b0ffec77f9c8c6d3810f14aa23b67d5c)
 Suggest to verify the variable status before turn it off. Or you just lose your gas if it is already off.
 - [x]

### Investor
*

### Stranger
*

<br>

# MultiSigWallet.sol
