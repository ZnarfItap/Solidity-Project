# Solidity-Project

This Solidity program is a simple token contract that demonstrates the functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

The program has two functions
### Mint
The mint function adds tokens to the balance of a specified address and the total supply.
### Burn
The burn function removes tokens from the balance of the specified address and total supply if the balance of the specified address is enough.

## Getting Started

### Installing

* Downlad the create_token.sol
* create_token.sol can be run using the online solidity IDE https://remix.ethereum.org/

### Executing program

* Go to https://remix.ethereum.org/

```javascript

contract MyToken {

    // public variables here
    string public TokenName = "PLENN";
    string public TokenAbbrv = "PLN";
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
        require(balances[_address] >= _value, "Insufficient balance to burn");
        if (balances[_address] >= _value){
        TotalSupply -= _value;
        balances[_address] -= _value;
        }
    }
}

```

* Right click on a blank area in FILE EXPORER(Right Window) and click upload file
* Upload reate_token.sol
* Open on create_token.sol in FILE EXPORER
* Open the Solidity compiler(third icon on the far right)
* Click "Compile and Run script"
* Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. 
* Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.
* Once the contract is deployed, you can interact with it by calling the MyToken function. 
* Click on the "mint" in the left-hand sidebar, put address and amount to mint. 
* Click on the "burn" in the left-hand sidebar, put address and amount to burn. 
* Click on the "balances" in the left-hand sidebar, put address to check total balance. 


## Authors

Francesque Marie T. Pati

patifrancesque@gmail.com
