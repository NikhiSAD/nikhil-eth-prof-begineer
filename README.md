# My Ethereum Token Smart Contract

The My Ethereum Token smart contract allows you to create and manage a custom cryptocurrency token on the Ethereum blockchain. This ERC-20-like token is designed to support essential token management features such as minting (creating new tokens) and burning (destroying existing tokens). The contract serves as a foundational template for understanding and working with Ethereum-based tokens.

Features

Token Details: View and manage the token’s name, abbreviation, and total supply.

Balance Management: Track and manage token balances for various addresses.

Minting: Create new tokens and allocate them to specified addresses.

Burning: Destroy tokens from specified addresses, with checks to ensure sufficient balance.

## Description

The My Ethereum Token smart contract is a basic implementation of a cryptocurrency token on the Ethereum blockchain, using Solidity. It offers fundamental functionalities required for token management, including:

Minting: Increase the total supply of tokens and credit a specified address.

Burning: Decrease the total supply of tokens and debit a specified address, provided there is a sufficient balance.

This simple implementation is an excellent starting point for those looking to understand token management on Ethereum.

## Getting Started

### Executing program

Prerequisites

Remix IDE: An online Solidity integrated development environment.


Execution Instructions

Access Remix IDE: Go to Remix.


Create a New File:

Click the "+" icon in the left-hand sidebar to create a new file.

Save the file with a .sol extension (e.g., MyToken.sol).

Insert the Code: Copy and paste the following Solidity code into your new file:

    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;

    contract MyToken {

    // public variables here
    string public tokenName = "Thappar UNIVERSITY";
    string public tokenAbbrv = "TU";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
    }


Compile the Contract:

Click on the "Solidity Compiler" tab in the left-hand sidebar.

Ensure the compiler version is set to 0.8.18.

Click "Compile MyToken.sol".


Deploy the Contract:

Navigate to the "Deploy & Run Transactions" tab in the left-hand sidebar.

Select "MyToken" from the contract dropdown menu.

Click "Deploy".


Interact with the Deployed Contract:

Under "Deployed Contracts", expand the deployed MyToken contract.

You can interact with the contract using the following functions:

tokenName: Click to view the token name.

tokenAbbrv: Click to view the token abbreviation.

totalSupply: Click to view the total supply of tokens.

balances: Enter an address to view its token balance.

mint: Enter an address and a value, then click to mint new tokens.

burn: Enter an address and a value, then click to burn tokens.


## Authors

Nikhil Mankotia

nikhilmankotia02@gmail.com


## License

This project is licensed under the [Nikhil Mankotia] License - 
MIT License

Copyright (c) 2024 Nikhil Mankotia

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
