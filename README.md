# DigitalAsset Smart Contract

## Overview

`DigitalAsset` is an ERC20-like token implemented in Solidity. It manages a custom digital asset with functionalities like transferring, minting, burning, and managing allowances. The contract owner, referred to as the admin, has special privileges for minting new tokens.

## Contract Details

### Variables

- `assetName`: Name of the digital asset.
- `assetSymbol`: Symbol of the digital asset.
- `assetDecimals`: Decimal places for the asset.
- `assetTotalSupply`: Total supply of the digital asset.
- `admin`: Address of the contract admin.

### Mappings

- `accountBalances`: Maps addresses to their token balances.
- `spendingAllowances`: Maps addresses to their allowed spending amounts.

### Constructor

Initializes the contract with the asset's name, symbol, decimals, and initial supply. Sets the deployer as the admin and assigns the initial supply to the admin's address.

### Functions

#### `sendAsset(address _receiver, uint256 _amount)`

Transfers tokens to another account.

#### `authorizeSpender(address _spender, uint256 _amount)`

Authorizes another address to spend tokens on the user's behalf.

#### `spendFrom(address _sender, address _receiver, uint256 _amount)`

Allows an authorized spender to transfer tokens from one account to another.

#### `createAsset(address _recipient, uint256 _amount)`

Admin-only function to mint new tokens.

#### `destroyAsset(uint256 _amount)`

Allows users to burn their own tokens.

#### `increaseSpendingAllowance(address _spender, uint256 _addedAmount)`

Increases the allowance for a spender.

#### `decreaseSpendingAllowance(address _spender, uint256 _subtractedAmount)`

Decreases the allowance for a spender.

## Usage

### Deployment

Deploy the `DigitalAsset` contract with the asset name, symbol, decimals, and initial supply.

### Minting Tokens

Admin can mint tokens using `createAsset`.

### Burning Tokens

Users can burn tokens using `destroyAsset`.

### Transferring Tokens

Users can transfer tokens using `sendAsset`.

### Authorizing Spenders

Users can authorize spenders using `authorizeSpender`.

### Spending Tokens

Authorized spenders can transfer tokens on behalf of a user using `spendFrom`.

### Adjusting Allowances

Increase or decrease allowances using `increaseSpendingAllowance` or `decreaseSpendingAllowance`.
