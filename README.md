# TESTNFT - Simple NFT Collection

A simple ERC-721 NFT smart contract built for testing and learning purposes on Ethereum Sepolia testnet.

## Overview

**TESTNFT** is a basic NFT collection smart contract that demonstrates fundamental NFT functionalities including minting with price limits, supply constraints, and ownership management.

## Contract Details

- **Contract Name:** TESTNFT
- **Symbol:** TNFT
- **Network:** Sepolia Testnet
- **Contract Address:** [`0x64002B3c9E6D4C4074AcdBBD85BBB888cf8f8780`](https://sepolia.etherscan.io/address/0x64002B3c9E6D4C4074AcdBBD85BBB888cf8f8780)
- **Solidity Version:** ^0.8.20

## Features

- **Maximum Supply:** 100 NFTs
- **Mint Price:** 0.001 ETH per NFT
- **Batch Minting:** Support for minting multiple NFTs in a single transaction
- **Supply Tracking:** Real-time tracking of minted and remaining NFTs
- **Owner Controls:** Owner-only functions for URI updates and fund withdrawal
- **Standard Compliant:** Implements ERC-721 standard using OpenZeppelin contracts

### Public Functions

#### `mint(uint256 quantity)`
Mints NFTs to the caller's address.
- **Parameters:** 
  - `quantity` - Number of NFTs to mint
- **Payment Required:** 0.001 ETH × quantity
- **Requirements:**
  - Quantity must be greater than 0
  - Total minted cannot exceed MAX_SUPPLY (100)
  - Sufficient ETH must be sent

#### `getMintedCount()`
Returns the total number of NFTs minted.
- **Returns:** `uint256` - Total minted count

#### `getRemainingSupply()`
Returns the number of NFTs still available to mint.
- **Returns:** `uint256` - Remaining supply

#### View Constants
- `MAX_SUPPLY` - Returns 100
- `MINT_PRICE` - Returns 0.001 ether
- `totalMinted` - Current minted count

### Owner-Only Functions

#### `setBaseURI(string memory newBaseURI)`
Updates the base URI for token metadata.
- **Parameters:**
  - `newBaseURI` - New base URI string

#### `withdraw()`
Withdraws all ETH from the contract to the owner's address.

## Resources

- [OpenZeppelin Contracts](https://docs.openzeppelin.com/contracts/)
- [ERC-721 Standard](https://eips.ethereum.org/EIPS/eip-721)
- [Remix IDE Documentation](https://remix-ide.readthedocs.io/)
- [Sepolia Testnet](https://sepolia.dev/)
