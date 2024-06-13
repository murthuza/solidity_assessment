# solidity_assessment

# MurthuzaToken Smart Contract

MurthuzaToken is a simple ERC-20-like token implemented in Solidity. This contract provides functionalities to mint and burn tokens while maintaining a record of the total supply and individual balances of tokens.

## Contract Details

- **Token Name:** Murthuza
- **Token Abbreviation:** MS
- **Total Supply:** Initially set to 0

## Public Variables

- `string public tokenName`: The name of the token.
- `string public abbr`: The abbreviation of the token.
- `uint public totalSupply`: The total supply of the token.

## Mapping

- `mapping (address => uint) public balances`: This maps each address to its balance of tokens.

## Functions

### Mint Function

```solidity
function mint(address _address, uint _value) public
```

The mint function increases the total supply of tokens and adds the specified value to the balance of the given address.

**Parameters:**

- `_address`: The address to which the tokens will be minted.
- `_value`: The number of tokens to mint.

### Burn Function

```solidity
function burn(address _address, uint _value) public
```

The burn function decreases the total supply of tokens and subtracts the specified value from the balance of the given address. It checks that the address has enough tokens to burn.

**Parameters:**

- `_address`: The address from which the tokens will be burned.
- `_value`: The number of tokens to burn.

## Requirements

- The balance of the address `_address` must be greater than or equal to the `_value` being burned.

**Error Handling:**

- If the balance is insufficient for burning, the transaction will revert with the message "Funds not sufficient".

## Deployment

To deploy the `MurthuzaToken` contract, use a Solidity-compatible environment such as Remix, Truffle, or Hardhat. Ensure your Solidity compiler version is set to 0.8.18.

## License

This project is licensed under the MIT License.
