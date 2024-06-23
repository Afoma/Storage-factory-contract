# Storage-factory-contract

The ability of a smart contract to interact with another smart contract is called Composability. I can have multiple smart contracts in one file but it is best practice to have separate files for each smart contract. In the same way that we can create a type of name with the struct keyword, we can also create a type of name with the contract keyword. For example

```
contract Example {
  function store() public{
    Example public example;
    example = new Example();
  }
}
```
In the above example, the name of the smart contract is Example and it created a type called `example`, which can be named anything. 
