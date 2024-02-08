# RandomP2P ERC1155 Trading Contract

This Solidity smart contract enables random peer-to-peer (P2P) trading of ERC1155 tokens with other participating traders. Designed for flexibility and simplicity, the contract allows participants to exchange their tokens in a random match-up process. Conceptualized for a trading card game and inspired by the random trading system in Pokemon Sword and Shield.

## Features

- **Random Trading Mechanism**: Trades are executed between random participants, ensuring a dynamic trading environment.
- **ERC1155 Support**: Fully compatible with ERC1155 tokens, facilitating the trade of a wide range of digital assets.
- **Trade Price Setting**: Owners can set the price for each trade, allowing for economic adjustments based on market conditions.
- **Trade Gate Control**: The contract owner can open or close the trading gate, providing control over the trading process.

## How It Works

1. **Initiate Trade**: A user initiates a trade by calling the `trade` function with the ID of the token they wish to trade.
2. **Trade Matching**: If another trade is waiting, the contract will automatically match the trades and swap the tokens between the two participants.
3. **Trade Completion**: Once a match is made, the trade is completed, and both parties receive their new tokens.

## Functions

- `trade(uint256 id)`: Initiate a trade with a specific token ID.
- `cancelTrade()`: Cancel a waiting trade (if applicable).
- `tradeReady()`: Check if a trade is ready to be matched.
- `setRNDM(address rndmAddr)`: Set the address of the Random Token (RNDM) contract.
- `setCards(address cardAddr)`: Set the address of the ERC1155 token (card) contract.
- `setPrice(uint256 price)`: Set the trade price.
- `setGate(uint256 status)`: Open or close the trading gate.

## Setup and Deployment

1. **Deploy Contract**: Deploy the `RandomP2P` contract to your preferred blockchain network compatible with Solidity ^0.8.13.
2. **Configure Contract**: Set the appropriate addresses for the Random Token and ERC1155 token contracts using `setRNDM` and `setCards`.
3. **Adjust Settings**: Optionally, adjust the trade price and gate status using `setPrice` and `setGate`.

## Security and Ownership

- **Ownable Contract**: Incorporates ownership functionality, allowing only the owner to change critical settings.
- **Safe Transfers**: Utilizes the `Address` library for safe calls and value transfers, minimizing risks.

## Disclaimer

This contract is provided "as is", without warranty of any kind. Use at your own risk. Always ensure thorough testing before deployment.

## License

SPDX-License-Identifier: MIT

