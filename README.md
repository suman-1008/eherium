ExampleToken Smart Contract
This repository contains a simple implementation of a token smart contract named ExampleToken written in Solidity. ExampleToken allows for minting and burning of tokens, as well as tracking balances of token holders.

Smart Contract Details
Public Variables
Token Name: The name of the token is stored in the tokenName variable.
Token Abbreviation: The abbreviation of the token is stored in the tokenAbbrv variable.
Total Supply: The total supply of the token is tracked by the totalSupply variable.
Mapping
Balances: A mapping of addresses to token balances is implemented using the balances mapping.
Functions
Mint Function:

Description: This function mints new tokens and assigns them to a specified address.
Parameters:
_address: The address to which the new tokens will be minted.
_value: The amount of tokens to mint.
Functionality: Increases the total supply by the specified amount and increases the balance of the specified address accordingly.
Burn Function:

Description: This function burns existing tokens from a specified address.
Parameters:
_address: The address from which tokens will be burned.
_value: The amount of tokens to burn.
Functionality: Checks if the address has sufficient balance to burn the specified amount of tokens. If so, it decreases the total supply and the balance of the specified address accordingly.
Usage
To use this smart contract, you can deploy it on an Ethereum-compatible blockchain network. Once deployed, you can interact with it using Ethereum wallet applications or by calling its functions programmatically.

License
This project is licensed under the MIT License - see the LICENSE file for details.
