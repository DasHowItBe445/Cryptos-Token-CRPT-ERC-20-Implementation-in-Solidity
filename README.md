# Cryptos ERC20 Token & ICO Smart Contract

A complete ERC20 token implementation with an Initial Coin Offering (ICO) built using Solidity.
This project demonstrates how a cryptocurrency token can be created, distributed via an ICO, and safely traded after a defined lock-in period.

Project Overview:

This project consists of two smart contracts:

1] Cryptos – A basic ERC20-compliant token contract

2] CryptosICO – An ICO (Initial Coin Offering) contract that manages token sales, investment rules, and trading restrictions

The goal of this project is to learn and implement ERC20 tokens from scratch, understand allowances and transfers, and design a time-based ICO lifecycle.


Tech Stack:

1] Solidity ^0.8.x

2] Ethereum / EVM

3] Remix IDE / Hardhat / Foundry (any environment can be used)

4] Metamask 


Smart Contract Architecture:

1] Cryptos (ERC20 Token Contract)

This contract implements the core ERC20 functionality.

Token Details-

- Token Name: Cryptos

- Symbol: CRPT

- Decimals: 0 (kept simple for learning)

- Total Supply: 1,000,000 tokens

- Founder: Deployer of the contract

Key Features-

- Token balance tracking using mappings

- Token transfers between accounts

- Allowance mechanism (approve + transferFrom)

- Emits standard ERC20 events (Transfer, Approval)

Core Functions-

transfer() – Transfers tokens from sender to receiver

approve() – Allows a spender to use tokens on behalf of the owner

transferFrom() – Enables delegated token transfers

balanceOf() – Returns token balance of an address

2] CryptosICO (ICO Contract)

This contract extends the ERC20 token and manages the token sale lifecycle.

ICO Workflow:

The ICO goes through four states:
| State         | Description                             |
| ------------- | --------------------------------------- |
| `beforeStart` | ICO has not started                     |
| `running`     | ICO is active and accepting investments |
| `afterEnd`    | ICO is finished                         |
| `halted`      | ICO paused by admin                     |


Investment Rules:

- Token Price: 0.001 ETH per token

- Hard Cap: 300 ETH

- Minimum Investment: 0.01 ETH

- Maximum Investment: 5 ETH

- ICO Duration: 30 days

- Token Trading Start: 1 day after ICO ends


Trading Lock Mechanism:

Token transfers are disabled during the ICO.
Trading is enabled only after tokenTradeStart.

This prevents:

- Premature trading

- Market manipulation during token sale

Investing in the ICO:

Investors can buy tokens by-

- Calling invest()

- Sending ETH directly to the contract (via receive())

Tokens are-

- Calculated based on ETH sent

- Transferred from the founder’s balance

- ETH is forwarded to the deposit address

Token Burn Mechanism:

After the ICO ends-

- Remaining unsold tokens held by the founder can be burned

- This helps control token supply

```
function burn() public returns(bool)
```

Admin Controls:

Only the admin (contract deployer) can-

- Halt the ICO

- Change deposit address

This ensures controlled execution of critical operations.

Security Considerations:

1. Uses Solidity 0.8.x (built-in overflow protection)

2. Time-based state validation for ICO phases

3. Investment limits enforced

4. Trading locked until ICO completion

⚠️ This project is for learning and demonstration purposes and has not been audited for production use.

Learning Outcomes:

Through this project, you’ll understand-

- ERC20 token mechanics

- Allowances and delegated transfers

- ICO state machines

- Token sale economics

- Solidity inheritance and overrides

- Time-based access control

Future Improvements:

- Add SafeMath (educational)

- Add pausable token transfers

- Add whitelist for investors

- Add refund mechanism

- Integrate with frontend (Web3 / ethers.js)
