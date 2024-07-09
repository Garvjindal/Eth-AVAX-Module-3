# MyToken Smart Contract

This smart contract implements a basic ERC-20 token with minting and burning functionalities. The token contract is implemented in Solidity and is compatible with the Ethereum blockchain.

## Features

- **Token Name:** Configurable token name
- **Token Symbol:** Configurable token symbol
- **Decimals:** Configurable decimal places
- **Total Supply:** Initial supply set during contract deployment
- **Ownership:** Owner has exclusive rights to mint new tokens
- **Transfer:** Allows transferring tokens between addresses
- **Minting:** Owner can mint new tokens
- **Burning:** Any user can burn their tokens

## Functions

### `constructor`
The constructor initializes the contract with the specified parameters:
- `_name`: The name of the token
- `_symbol`: The symbol of the token
- `_decimals`: The number of decimal places
- `_initialSupply`: The initial supply of the token

### `transfer`
Allows the transfer of tokens from the sender's address to another address.
- `_to`: The recipient address
- `_value`: The amount of tokens to transfer

### `mint`
Allows the owner to mint new tokens.
- `_to`: The address to receive the minted tokens
- `_value`: The amount of tokens to mint

### `burn`
Allows any user to burn their tokens.
- `_value`: The amount of tokens to burn

## Events

### `Transfer`
Triggered when tokens are transferred from one address to another.
- `from`: The sender address
- `to`: The recipient address
- `value`: The amount of tokens transferred

### `Mint`
Triggered when new tokens are minted.
- `to`: The recipient address
- `value`: The amount of tokens minted

### `Burn`
Triggered when tokens are burned.
- `from`: The address from which the tokens are burned
- `value`: The amount of tokens burned

## Usage

To deploy and interact with this contract, you will need a Solidity development environment such as Remix, Truffle, or Hardhat. Here is a basic example of how to deploy the contract:

1. Open Remix IDE or your preferred Solidity development environment.
2. Copy and paste the smart contract code into a new file.
3. Compile the contract.
4. Deploy the contract with the desired parameters (name, symbol, decimals, initial supply).
5. Interact with the contract using the provided functions (transfer, mint, burn).


