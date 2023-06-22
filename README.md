# Creating a Token 
The token is named "META" with the abbreviation "MTA." The project allows for the minting and burning of tokens.

The purpose of the project can vary depending on your specific goals and intentions:

1.Creating a Custom Token: You are creating a custom token called "META" with the symbol "MTA" on the Ethereum blockchain. This token can serve various purposes, such as representing ownership, value, or participation rights within a specific ecosystem or project.

2.Minting and Burning Tokens: The project provides functionality to mint (create) and burn (destroy) tokens. The mint function allows you to increase the total supply of tokens and allocate them to a specific address. The burn function allows for the removal of tokens from a specific address, reducing the total supply accordingly. This capability can be useful for managing token distribution, rewards, or adjusting token supply based on specific rules or requirements.

3.Token Management and Balances: The project includes a mapping variable called "balances," which allows you to track the balance of tokens held by different addresses. The balances are publicly accessible, as defined by the "public" keyword. This feature enables transparency and allows users or external systems to verify token balances.


## Description

This project involves creating a token on the Ethereum blockchain with the name "META" and the symbol "MTA." The purpose of this project is to establish a digital asset that can be used for various purposes within a specific ecosystem or project. The mint function allows for the creation of new tokens, increasing the total supply and allocating them to a specified address. This can be used for token distribution, rewards, or fundraising purposes. On the other hand, the burn function enables the removal of tokens from a specific address, reducing the total supply accordingly. This functionality is valuable for managing token supply based on specific rules or requirements. The project also includes a mapping variable called "balances," which tracks the token balances of different addresses. This provides transparency and allows users or external systems to verify token holdings. Overall, your project empowers you to create, manage, and distribute a custom token on the Ethereum blockchain, opening up possibilities for various applications, such as loyalty programs, decentralized finance (DeFi) platforms, or in-app currencies within a specific ecosystem.

## Getting Started

### Installing

Installing an Ethereum development environment - We can set up an Ethereum development environment using Remix Etheruem IDE
There are no specific modifications needed to the files. However, it's important to ensure that we have the necessary dependencies and development environment set up correctly.

### Executing program

To run the provided smart contract code, we can follow these step-by-step instructions:

1. Set up the Ethereum Development Environment:

Install Remix IDE, a web-based Ethereum development environment, or use another development environment of your choice.
2. Creating  a New Solidity File:

Open the Remix IDE .
Create a new Solidity file and name it "MyToken.sol".
Write the required code into the "MyToken.sol" file.
Compile the Smart Contract:

In the Remix IDE, navigate to the "Solidity Compiler" section.
Select the "MyToken.sol" file.
Click the "Compile" button to compile the smart contract.

3. Deploy the Smart Contract:

In the Remix IDE, navigate to the "Deploy & Run Transactions" section.
Select the "MyToken" contract from the dropdown.
Click the "Deploy" button to deploy the smart contract to the selected network.
Take note of the deployed contract's address for future interactions.

4. Interact with the Smart Contract:

In the Remix IDE, navigate to the "Deployed Contracts" section.
Select the deployed "MyToken" contract from the list.
We will see the contract's public variables (tokenName, tokenAbbrv, totalSupply) and the "balances" mapping.
To interact with the contract, you can use the provided functions:
To mint new tokens, call the "mint" function and provide an address and the amount to mint as parameters.
To burn tokens, call the "burn" function and provide an address and the amount to burn as parameters.
After executing a function, you can check the updated state variables and balances.

Code Block :
```
function mint (address _address, uint _value) public{
    totalSupply += _value;
    balances[_address] += _value;
}
```
```
function burn (address _address, uint _value) public{
    if(balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
    }
```



## Authors
Rahul Purakayastha


## License

This project is licensed under the [Rahul_Purakayastha] License - see the LICENSE.md file for details
