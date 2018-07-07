# Solidity Golf Challenge [ConsenSys India '18]

A repository hosting the submissions to the Solidity Golf Challenge for ConsenSys India '18.

## Participating

Submit a keccak256 hash (or any other 32 bytes long hash with a hashing algorithm to be later specified by you) of the bytecode of your smart contract or the source code string of the smart contract submission to the registry contract at https://rinkeby.etherscan.io/address/0x1744fc0e24cba7356d19c62d9630cadfae1ea31b#code on the Rinkeby network. At the end of the contest you can specify wether each specific hash was for the golf challenge or for the gas challenge.

As an alternative, you can send a PR of with a file titled <your_name>_golf.sol or <your_name>_gas_challenge.sol depending on which challenge you are entering for (you can participate in both), please note this will make your submission public and hence give advantage to other players.

## Contract Specification

The contract is an "allowance" contract. It is supposed to:

* Allow deposits only by the account that deployed it.
* Have a public function  to disburse `X`% of its balance to an address `A`.
* `A` must be set by the deployer and not at compile time.
* At deploy time `X = 5` and after that `X = <block height at last execution> % 100`.
* The disbursement function must only be callable once every 105 blocks. Otherwise it should revert the transaction.

## Rules

* All source code files that don't compile (i.e. throws an error, as opposed to a warning, at compile time) with `solc` v0.4.24 will be disqualified.
* The contest will run until Saturday, July 7th, 1200 UTC at which time the winners will be chosen.
* Assembly blocks are **not** permitted. Every submission should be written in vanilla Solidity.
* Usage of external libraries is not permitted. All code should be written by the contestant.
* When submitting the contract please comment in the PR what's the name of each of the functions.

* For the Solidity Golf challenge the source code file with the least amount of characters will be pronounced the winner.
* For the Solidity Gas Optimization challenge the source code file that has the smaller execution cost will be pronounced the winner.

The testing execution path for both challenges will be revealed after the winners are chosen.

## Any doubts?

Just reach out to me through any channel (issues in this repo are fine! :D)
