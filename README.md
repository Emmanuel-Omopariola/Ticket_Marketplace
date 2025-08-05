# Ticket Market Place

A decentralized ticket marketplace inspired by TokenMaster, built on blockchain technology to eliminate ticket fraud, scalping, and provide transparent, secure ticket trading for events.

## Overview

This project creates a decentralized ticket marketplace that revolutionizes event ticketing by leveraging blockchain technology. Inspired by TokenMaster, the platform ensures authentic ticket ownership, prevents counterfeiting, and enables secure peer-to-peer ticket transfers while maintaining event organizer control and revenue distribution.

## Key Features

- **NFT-Based Tickets**: Each ticket is a unique NFT ensuring authenticity and ownership
- **Anti-Scalping Mechanisms**: Smart contract controls to prevent ticket hoarding
- **Transparent Pricing**: All ticket prices and fees are visible on-chain
- **Secure Transfers**: Blockchain-verified ticket ownership and transfers
- **Event Management**: Tools for event organizers to create and manage events
- **Resale Controls**: Configurable resale rules set by event organizers

## Technology Stack & Tools

- **Solidity** (Writing Smart Contracts & Tests)
- **Javascript** (React & Testing)
- **[Hardhat](https://hardhat.org/)** (Development Framework)
- **[Ethers.js](https://docs.ethers.io/v5/)** (Blockchain Interaction)
- **[React.js](https://reactjs.org/)** (Frontend Framework)
- **[MetaMask](https://metamask.io/)**

## Requirements For Initial Setup

- Install **[NodeJS](https://nodejs.org/en/)**. Recommended to use the LTS version.
- Install **[MetaMask](https://metamask.io/)** on your browser.

## Setting Up

### 1. Clone/Download the Repository

```bash
git clone https://github.com/yourusername/ticket-marketplace.git
cd ticket-marketplace
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Run tests

```bash
npx hardhat test
```

### 4. Start Hardhat node

```bash
npx hardhat node
```

### 5. Run deployment script

In a separate terminal execute:

```bash
npx hardhat run ./scripts/deploy.js --network localhost
```

### 6. Start frontend

```bash
npm run start
```

Visit `http://localhost:3000` to interact with the ticket marketplace.

## Usage

### Contract Interaction Example

```javascript
import { ethers } from 'ethers';

const provider = new ethers.providers.Web3Provider(window.ethereum);
const signer = provider.getSigner();

const contractAddress = "0x...";
const contract = new ethers.Contract(contractAddress, ABI, signer);

// Purchase a ticket
const ticketPrice = ethers.utils.parseEther("0.1");
const result = await contract.purchaseTicket(eventId, seatNumber, { value: ticketPrice });

// List ticket for resale
await contract.listTicketForResale(ticketId, resalePrice);
```

## Testing

### Run All Tests

```bash
npx hardhat test
```

### Run Coverage Report

```bash
npx hardhat coverage
```

## Deployment

### Deploy to Testnet

```bash
npx hardhat run scripts/deploy.js --network goerli
```

### Verify Contracts

```bash
npx hardhat verify --network goerli DEPLOYED_CONTRACT_ADDRESS
```

## Contributing

We welcome contributions from the community!

### Development Process

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


### **emmaculate_eth**

