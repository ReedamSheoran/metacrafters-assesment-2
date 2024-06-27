# Project Title MyToken Contract

## Description
This is a simple ERC-20 token contract written in Solidity. It allows users to mint and burn tokens, and keeps track of the total supply and individual balances.

## Getting Started
To use this contract, you'll need to have a basic understanding of Solidity and the Ethereum blockchain.

## Installing
This contract is written in Solidity, so you'll need to have a Solidity compiler installed on your machine. You can use Remix, a popular online Solidity IDE, or install a local compiler like solc.

## Executing program
To execute this contract, you'll need to deploy it to a blockchain network like Ethereum or a testnet like Ropsten. You can use a tool like Truffle or Remix to deploy and interact with the contract.

## Help
If you have any questions or need help with this contract, feel free to reach out to the authors.

## Authors
ReedamSheoran (author of the original contract)

## License
This contract is licensed under the MIT License. See the SPDX-License-Identifier at the top of the contract file for more information.

Here is the contract code again for reference:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyToken {

    // public variables here
    string public tokenname = "REEDAM";
    string public tokenabrv = "REE";
    uint public totalsupply = 0;

    // mapping variable here
    mapping (address => uint ) public balances;

    // mint function
    function mint (address R_address, uint R_values) public {
      totalsupply += R_values;
      balances[R_address] += R_values;
    }

    // burn function
    function burn (address R_address, uint R_values) public {
      if (balances[R_address]>= R_values){
      totalsupply -= R_values;
      balances[R_address] -= R_values;
      }
    }
}
```
