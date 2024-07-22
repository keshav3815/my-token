# Create a Token 
A basic smart contract to manage a cryptocurrency token called "My_Token", allowing users to mint and burn tokens while keeping track of balances.
# Description 
This code is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract enables users to mint and burn tokens, with functionalities to adjust the total supply and individual balances accordingly. This code serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.
# Getting started
## Executing code 
To run this code, you can use Remix, an online Solidity IDE. To get started , go to Remix website at https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.18+commit.87f61d96.js Once you go on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g.,My_token.sol). Copy and paste the following code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

 contract MyToken {
    string public tokenName = "meta";
    string public tokenshiba = "sibh";
    uint public totalSupply = 0;
    
    //mapping variable here 
    mapping (address => uint ) public balances;
    //mint function 
    
    function mint(address _address, uint _value) public 
    {
        totalSupply += _value;
        balances [_address] += _value;
    }
    //burn function 
    function burn (address _address, uint _value) public 
    {
        if (balances [_address] >= _value)
        {
          totalSupply -= _value;
          balances [_address] -= _value;
        }
    }
 }
```
To compile this code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile My_Token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Our_Token" contract from the dropdown menu, and then click on the "Deploy" button. Now there you can check tokenName, tokenshiba and total_supply by clicking on them.

To mint Tokens, scroll above and go to the account section, copy the account address and paste it under the _address section and add the amount you want to add under _value section then just click on transact and you can check the added amount by calling again total_supply function.

To destroy some tokens, go to the burn_Func, expand it and paste the same address to the _address section and put the amount to be burn to _value section then just click on transact and by calling again total_supply you can check the updated amount.
# Author 
Keshav Singh 

keshavsingh3815@gmail.com
