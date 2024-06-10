Project Title : In this project we need to create a token in which we are taking some public variables which stores (Token Name, Token Abbrv., Total Supply). 
The primary objective of the MyToken contract is to provide a simple and comprehensible implementation of token creation and management on the Ethereum network. 
It serves as an educational tool for developers learning about blockchain and smart contracts, and as a foundational template for more complex token systems. 
The MyToken smart contract offers a straightforward implementation of a custom token on the Ethereum blockchain. 
It allows users to mint and burn tokens while tracking the total supply and individual balances. 
It is designed to offer a simple yet effective way to manage a token with basic functionalities.

Description : we need to perform different function in token to demonstrate the code.
Mint Tokens: This function allows the creation of new tokens. 
Burn Tokens: This function enables the destruction of existing tokens. 
Total Supply: This feature keeps track of the overall number of tokens in circulation. Balances: This feature maintains records of individual token holders' balances. 

Getting Started: This is a simple ERC-20 token contract implemented in Solidity. The contract allows for the creation and destruction of tokens, as well as storing information about the token.

Requirements:
1. The contract has public variables that store the details about the coin:
   - `tokenName`: A string representing the name of the token.
   - `abbrv`: A string representing the abbreviation of the token.
   - `totalSupply`: An unsigned integer representing the total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `balances`: A mapping that associates addresses with their corresponding token balances.

3. The contract has a `mint` function that increases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `_address`: The address to which the tokens will be minted.
     - `_value`: The amount of tokens to be minted.
   - Actions:
     - Increase the `totalSupply` by `_value`.
     - Increase the balance of the `_address` by `_value`.

4. The contract has a `burn` function that decreases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `_address`: The address from which the tokens will be burned.
     - `_value`: The amount of tokens to be burned.
   - Actions:
     - Check if the balance of the `_address` is greater than or equal to `_value`.
     - If true, decrease the `totalSupply` by `_value`.
     - Decrease the balance of the `_address` by `_value`.

Usage:
1. Deploy the `MyToken` contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

   - `mint`: Creates new tokens and assigns them to a specified address.
     - Parameters:
       - `_address`: The address to which the tokens will be minted.
       - `_value`: The amount of tokens to be minted.

   - `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
     - Parameters:
       - `_address`: The address from which the tokens will be burned.
       - `_value`: The amount of tokens to be burned.
