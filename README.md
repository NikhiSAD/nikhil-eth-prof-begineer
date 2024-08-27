# My Ethereum Token Smart Contract

MY  Ethereum token smart contract is designed to create and manage a custom cryptocurrency token. This token represents a digital asset that can be minted (created) and burned (destroyed) based on predefined rules. The primary purpose of this project is to provide a simple yet functional token management system with the following features: Token Details,Balance Management,Minting,Burning.This smart contract serves as a basic template for creating and managing a cryptocurrency token on the Ethereum blockchain.

## Description

My Ethereum Token smart contract is a basic implementation of an ERC-20 like token on the Ethereum blockchain, written in Solidity. It provides the essential functionalities required to manage a cryptocurrency token. The smart contract is a straightforward implementation of a token management system. It includes basic functionality to mint and burn tokens, ensuring that tokens can only be burned if the balance is sufficient. This simplicity makes it a great starting point for understanding how cryptocurrencies can be managed on the Ethereum blockchain.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Mytoken.sol). Copy and paste the following code into the file:

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


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" and then click on the "Compile Mytoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Mytoken" contract from the dropdown menu, and then click on the "Deploy" button.

Under Deployed Contracts, expand the deployed MyToken contract. You can now interact with the contract functions:
tokenName: Click to view the token name.
tokenAbbrv: Click to view the token abbreviation.
totalSupply: Click to view the total supply of tokens.
balances: Enter an address to view its token balance.
mint: Enter an address and a value, then click the button to mint new tokens.
burn: Enter an address and a value, then click the button to burn tokens.

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
