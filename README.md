# reqasrev.sol

This is a program in Solidity that demonstrates the revert, require, and assert functions in the Solidity language. This serves as a demonstration as well as a submission to the assesment to MetaCrafters.
## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has multiple functions. Namely deposit and withdraw. 
deposit adds on to the total sum of the variable amount and withdraw takes away from the total supply.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. 
Save the file with a .sol extension. Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.1;

contract Contract { 
    uint public balance;


    constructor(){
        balance = 0;
    }

    //require functions being used for depositing and withdrawing amounts 
    function deposit(uint amount) public {
        require(amount > 0 , "Deposit amount cannot be lower than 0"); 
        balance += amount;
        assert (amount < 101);
        
    }

    function withdraw(uint amount) public {
        require(amount > 0 , "Withdrawal Amount must be more than 0"); 
        if (balance < amount){
            revert("Insufficient Balance");
        } else { balance -= amount;
          } 
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile reqasrev.sol" button. 

The button name can vary depending on the file name that you designated when creating the file of the code.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the contract with the same name of the file you have just compiled (e.g if your file has the name "HelloWorld.sol" the option to click should be "HelloWorld") from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the deposit, withdraw, and balance functions. 

To add to the total sum all that would need to be done is enter a value from 1 to 100 in the deposit and click deposit. 

To take away from the total amount all that would need to be done is to enter a value in withdraw and click withdraw. 

To see the total amount you have all you would need to click on is balance.


## Authors

Contributors names and contact info
Gavinno Othello C. Angeles
email me at: 201911104@fit.edu.ph


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
