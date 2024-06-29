# myTOKEN

`myTOKEN` is a simple Ethereum smart contract written in Solidity that implements a basic ERC20-like token with minting and burning capabilities.

## Features

- Public variables to store details about the token:
  - Token Name
  - Token Abbreviation
  - Total Supply
- A mapping to store balances of addresses.
- A `mint` function to create new tokens.
- A `burn` function to destroy tokens.

## Requirements

1. The contract has public variables to store details about the token:
   - Token Name
   - Token Abbreviation
   - Total Supply

2. The contract has a mapping of addresses to balances:
   ```solidity
   mapping(address => uint) public balances;
   ```

3. The contract has a `mint` function that:
   - Takes an address and a value as parameters.
   - Increases the total supply by the specified value.
   - Increases the balance of the specified address by the same amount.

4. The contract has a `burn` function that:
   - Takes an address and a value as parameters.
   - Decreases the total supply by the specified value.
   - Decreases the balance of the specified address by the same amount.
   - Checks to ensure the balance of the specified address is greater than or equal to the value to be burned.

## Functions

### mint

```solidity
function mint(address _address, uint _value) public {
    total_Supply += _value;
    balances[_address] += _value;
}
```

Increases the total supply and the balance of the specified address by the given value.

### burn

```solidity
function burn(address _address, uint _value) public {
    if(balances[_address] >= _value) {
        total_Supply -= _value;
        balances[_address] -= _value;
    }
}
```

Decreases the total supply and the balance of the specified address by the given value. Ensures that the balance is sufficient before performing the burn.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
