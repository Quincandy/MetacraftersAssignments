# ATHENA TOKEN

This Solidity program is a simple "ATHENA TOKEN" program that creates a token called ATHENA. The purpose is to apply and demonstrate my understanding of the solidity beginner course on metacrafters.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions;one to mint the token and one to burn the token. There is a also a mapping of address to amount of the token the address has in it.

## Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ATHENA Token.sol). Copy and paste the following code into the file:

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
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile ATHENA Token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "ATHENA Token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Click on the "ATHENATOKEN" contract in the left-hand sidebar, and then click on the mint and burn function to key in amount of token to mint or burn. Finally, click on the "transact" button to execute the functions.

## Authors
Quincandy
https://twitter.com/metacraftersio


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
