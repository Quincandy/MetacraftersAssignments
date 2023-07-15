# ATHENA TOKEN

This Solidity program is a simple "ATHENA TOKEN" program that creates a token called ATHENA. The purpose is to apply and demonstrate my understanding of the Solidity beginner course on Metacrafters.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions: one to mint the token and one to burn the token. Additionally, there is a mapping of addresses to the amount of the token held by each address.

## Getting Started
Prerequisites
To run this program, you need to have access to Remix, an online Solidity IDE. If you don't have it already, you can access it at https://remix.ethereum.org/.

Execution
To run the program, follow these steps:

Open Remix in your web browser.
Create a new file by clicking on the "+" icon in the left-hand sidebar.
Save the file with a .sol extension (e.g., ATHENA Token.sol).
Copy and paste the code provided below into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract ATHENATOKEN {

    // public variables here
    string public TokenName = "ATHENA";
    string public TokenAbbrv = "AEN";
    uint public TotalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        TotalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
     function burn(address _address, uint _value) public {
         if (balances[_address] >= _value) {
            TotalSupply -= _value;
            balances[_address] -= _value;
            }
    }

}
In Remix, navigate to the "Solidity Compiler" tab in the left-hand sidebar.
Make sure the "Compiler" option is set to "0.8.18" (or another compatible version).
Click the "Compile ATHENA Token.sol" button to compile the code.
Once the code is compiled without any errors, you can deploy the contract:

Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
Select the "ATHENA Token" contract from the dropdown menu.
Click the "Deploy" button to deploy the contract.
After deploying the contract, you can interact with it by calling the mint and burn functions:

Click on the "ATHENATOKEN" contract in the left-hand sidebar.
Click on the mint or burn function, depending on your desired action.
Enter the amount of tokens to mint or burn.
Finally, click on the "transact" button to execute the function.

## Authors
Quincandy
https://twitter.com/metacraftersio


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
