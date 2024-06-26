# MyToken

MyToken is a simple ERC-20 token contract implemented in Solidity. It includes basic functionality for minting and burning tokens.

## Contract Details

- **Token Name:** MyToken
- **Token Symbol:** MTK
- **Total Supply:** The total number of tokens in circulation.

## Features

1. **Public Variables:** 
    - `name` - Stores the name of the token.
    - `symbol` - Stores the abbreviated name of the token.
    - `totalSupply` - Stores the total supply of the token.

2. **Balances Mapping:**
    - A mapping from addresses to their respective balances. This keeps track of the balance of each address.

3. **Mint Function:**
    - The `mint` function increases the total supply of tokens and the balance of the specified address.
    - Parameters:
      - `_to` - The address to which the tokens will be minted.
      - `_value` - The amount of tokens to be minted.

4. **Burn Function:**
    - The `burn` function decreases the total supply of tokens and the balance of the specified address.
    - Parameters:
      - `_from` - The address from which the tokens will be burned.
      - `_value` - The amount of tokens to be burned.
    - The function includes a check to ensure that the address has a sufficient balance to burn the specified amount of tokens.

## Usage

### Minting Tokens

To mint tokens, call the `mint` function with the recipient's address and the amount of tokens to mint.

```solidity
mint(address _to, uint256 _value)

```

### Burning Tokens
-To burn tokens, call the burn function with the address from which the tokens will be burned and the amount of tokens to burn. The address must have a sufficient balance to burn the specified amount of tokens.
```solidity
burn(address _from, uint256 _value)


```

## Example Usage
// Deploy the contract
MyToken token = new MyToken();

// Mint 100 tokens to address 0x123...
token.mint(0x123..., 100);

// Burn 50 tokens from address 0x123...
token.burn(0x123..., 50);



## License

This project is licensed under the MIT License.
