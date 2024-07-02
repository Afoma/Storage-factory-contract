# Storage-factory-contract

The ability of a smart contract to interact with another smart contract is called Composability. I can have multiple smart contracts in one file but it is best practice to have separate files for each smart contract. In the same way that we can create a type of name with the struct keyword, we can also create a type of name with the contract keyword. For example

```
contract Example {
  Example public example;
  
  function store() public{
    example = new Example();
  }
}
```
In the above example, the name of the smart contract is Example and it created a type called `example`, which can be named anything. 
To create a new smart contract, create a type with the smart contract's name and create a variable with it, just like it was done above `Example public example;`, create a function and within it, create a new smart contract with the `new` keyword. 

The format for creating a variable in Solidity is 

`type visibility name;`

## Imports
We write imports to make calling a contract from another contract possible without pasting the entire content of that contract into the contract that is calling it. It is always best practice to default to or use named imports. For example:
`import {StorageFactory"} from "./StorageFactory.sol";`

We only create new instances of a contract in another contract when that contract's instance we are creating already exists, either in another file ( and has already been imported) or in the current file in which it is being called. 

If we intend to create an instance of a smart contract and we intend to make a public variable for it, the format for doing it will be 

` name-of-imported-contract visibility name-of-variable-being-created`

For instance, `SimpleStorage public simpleStorage` means `simpleStorage` is a variable of `SimpleStorage` contract.
`SimpleStorage[] public simpleStorage` means `simpleStorage` is an array of `SimpleStorage` contracts. `address[] public simpleStorage` means `simpleStorage` is an array of adresses.
