# Tokenmaster

# How It Works

The application operates on a Web 3.0 framework, integrating Solidity smart contracts with a React frontend to create a decentralized event ticketing system. Here's how it works:

![Diagram](https://github.com/developerisnow/tickets_booking_web3_simple/blob/main/_docs/img/sequence_main.png?raw=true)

![Diagram](https://github.com/developerisnow/tickets_booking_web3_simple/blob/main/_docs/img/activity.png?raw=true)


1. Users connect their MetaMask wallet to the application through their browser.
2. Once connected, they can browse events listed on the React-based frontend.
3. When selecting an event , the frontend interacts with the smart contract to display available seats and event details.
4. The user chooses a seat and initiates a purchase by sending the appropriate amount of ETH.

The smart contract's mint function is called, which checks for the validity of the seat ID, ensures the seat is not already taken, and verifies the transaction's value against the ticket's cost.
If all conditions are met, the smart contract mints an NFT ticket, which represents proof of purchase and ownership, and transfers it to the user's wallet.
The frontend confirms the purchase and updates the user interface to display the newly minted NFT ticket.

In the case that the seats are sold out or another error occurs during the transaction, the frontend will show an appropriate message to the user, such as 'Sold Out' or a transaction error notification.

The sequence diagram provided above illustrates this process, showing the interaction between the user, the frontend, the smart contract, and the blockchain. It is a step-by-step visual representation of the app's functionality from the user's perspective.

### Contract
![Diagram](https://github.com/developerisnow/tickets_booking_web3_simple/blob/main/_docs/img/sequence_contract.png?raw=true)


## Technology Stack & Tools

- Solidity (Writing Smart Contracts & Tests)
- Javascript (React & Testing)
- [Hardhat](https://hardhat.org/) (Development Framework)
- [Ethers.js](https://docs.ethers.io/v5/) (Blockchain Interaction)
- [React.js](https://reactjs.org/) (Frontend Framework)
- [MetaMask](https://metamask.io/)

## Requirements For Initial Setup
- Install [NodeJS](https://nodejs.org/en/). Recommended to use the LTS version.
- Install [MetaMask](https://metamask.io/) on your browser.

## Setting Up
### 1. Clone/Download the Repository

### 2. Install Dependencies:
`$ npm install`

### 3. Run tests
`$ npx hardhat test`

### 4. Start Hardhat node
`$ npx hardhat node`

### 5. Run deployment script
In a separate terminal execute:
`$ npx hardhat run ./scripts/deploy.js --network localhost`

### 6. Start frontend
`$ npm run start`