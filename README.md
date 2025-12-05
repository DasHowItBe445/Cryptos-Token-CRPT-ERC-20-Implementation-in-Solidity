# Cryptos-Token-CRPT-ERC-20-Implementation-in-Solidity

This project contains a simple and transparent implementation of an ERC-20 token written in Solidity.
The token is named Cryptos (CRPT) and follows the essential ERC-20 standards, including balance tracking, approvals, and token transfers.

About the Project:

This contract demonstrates the core mechanics behind ERC-20 tokens-

- Managing a total supply

- Tracking user balances

- Secure token transfers

- allowance / approve mechanism for delegated transfers

- Emitting Transfer and Approval events

The purpose of this project is to understand how ERC-20 tokens function internally and gain hands-on experience in smart contract development.


Tech Stack:

1] Solidity ^0.8.x

2] Ethereum / EVM

3] Remix IDE / Hardhat / Foundry (any environment can be used)

4] Metamask 


Contract Features:

✔ totalSupply

The total number of CRPT tokens minted at deployment.

✔ balanceOf()

Returns the token balance of any address.

✔ transfer()

Allows users to send CRPT tokens directly to another address.

✔ approve()

Authorizes another address to spend tokens on behalf of the owner.

✔ allowance()

Checks how many tokens a spender is allowed to use.

✔ transferFrom()

Enables delegated transfers using the allowance system.


How to Run:

Using Remix

1] Open https://remix.ethereum.org/

2] Create a new .sol file and paste the contract

3] Compile using Solidity 0.8.x

4] Deploy using Injected Provider or Remix VM

5] Interact with the contract functions


Future Enhancements:

- Add token minting and burning functions

- Add OpenZeppelin security standards

- Build a frontend to interact with the token

- Deploy CRPT token to a public testnet
