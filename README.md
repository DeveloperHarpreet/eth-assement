# MyToken Smart Contract

This project implements a basic ERC20-like token on the Ethereum blockchain. The smart contract allows for minting and burning of tokens, and keeps track of balances associated with addresses.

## Contract Overview

The `MyToken` smart contract includes the following functionalities:

1. **Public Variables**: Stores details about the coin:
   - `Token Name`
   - `Token Abbreviation`
   - `Total Supply`

2. **Mapping**: Maps addresses to their respective balances.

3. **Mint Function**: Increases the total supply and the balance of the specified address.

4. **Burn Function**: Decreases the total supply and the balance of the specified address, with checks to ensure sufficient balance.

## Contract Details

### Public Variables

- `string public name` - Stores the name of the token.
- `string public symbol` - Stores the abbreviation (symbol) of the token.
- `uint public totalSupply` - Stores the total supply of the token.

### Mapping

- `mapping(address => uint) public balances` - Maps addresses to their respective balances.

### Mint Function

```solidity
function mint(address _to, uint _amount) public {
    totalSupply += _amount;
    balances[_to] += _amount;
}

This project is licensed under the MIT License.
