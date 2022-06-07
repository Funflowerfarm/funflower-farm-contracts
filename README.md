# Funflower Farm Contracts

This repo includes the contracts used in [Funflower farm](https://funflowerfarm.com/) along with a suite of tests.

## Prerequisites

- truffle
- solc (brew install solidity)
- nodejs
- docker-compose

## Testing

1. Open docker (if not already running)
2. Start ganache - `docker-compose up eth`
3. `truffle test`

## Contract Addresses

FFFTOKEN_CONTRACT=[0xecb21349dcfcb48b9bd51b70a7618e5fa00d2041](https://polygonscan.com/token/0xecb21349dcfcb48b9bd51b70a7618e5fa00d2041) in mainnet
BANK_CONTRACT=[0x835186f64fac54fe62687a8f32900a06bac49c7b](https://polygonscan.com/address/0x835186f64fac54fe62687a8f32900a06bac49c7b) in mainnet
PROXY_BANK_CONTRACT=[0xebbbe833f528ed5206c52326a2c92665cacaa5a9](https://polygonscan.com/address/0xebbbe833f528ed5206c52326a2c92665cacaa5a9) in mainnet

          
## Architecture

Funflower farm  uses an off-chain architecture to allow players to store data off-chain without the need to transact on the Blockchain after every action.

**Behaviour**
_Contracts that hold the behaviour of the game in the blockchain_

- `Bank.sol` - Withdraw, Deposit, collect Fees and handle sessions

**Data Storage**
_Contracts that hold the core data in the game_

- `FFFToken.sol` - FFF ERC20 token


