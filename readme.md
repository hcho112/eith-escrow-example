# Decentralized Escrow Application

This is an example Escrow DApp (Decentralized Application) built with Hardhat (https://hardhat.org/), created from the Alchemy Ethereum courses. This repository is maintained for archival purposes and includes updated comments for anyone interested in trying it out.

## Project Layout

The project consists of three main directories:

1. **`/app`** - Contains the front-end application built with React.
2. **`/contracts`** - Contains the Solidity smart contracts.
3. **`/tests`** - Contains tests for the Solidity contracts.

## Setup

### Prerequisites

- Node.js (https://nodejs.org/) installed on your machine.
- MetaMask (https://metamask.io/) browser extension installed for managing accounts and interacting with the DApp.

### Installation

1. **Clone the Repository**

   ```
   git clone <repository-url>
   cd <repository-name>
   ```

2. **Install Dependencies**

   Install the dependencies in the top-level directory:

   ```
   npm install
   ```

3. **Compile Contracts**

   Compile the smart contracts using Hardhat:

   ```
   npx hardhat compile
   ```

   The compiled artifacts will be placed in the `/app` folder, making them available to the front-end application. This path configuration can be found in the `hardhat.config.js` file.

4. **Run Hardhat Local Node**

   Start a local Hardhat node:

   ```
   npx hardhat node
   ```

   Leave this terminal window open. The node will provide a list of accounts preloaded with Ether for testing purposes.

5. **Set Up MetaMask**

   To interact with the DApp, set up your browser wallet:

   - Install the MetaMask extension if you haven't already.
   - Connect MetaMask to the local Hardhat network by following this guide: https://www.web3.university/article/how-to-build-a-react-dapp-with-hardhat-and-metamask

6. **Deploy Contracts**

   In a new terminal window, deploy the contracts to the local network:

   ```
   npx hardhat run scripts/deploy.js --network localhost
   ```

   Ensure your `deploy.js` script is correctly set up to deploy your contracts.

## Front-End Setup

1. **Install Front-End Dependencies**

   Navigate to the `/app` directory and install the dependencies:

   ```
   cd app
   npm install
   ```

2. **Run the Front-End Application**

   Start the React application:

   ```
   npm start
   ```

   Open http://localhost:3000 in your browser to view the application.

## Additional Notes

- Ensure that your MetaMask wallet is connected to the same network that Hardhat is running on (usually `localhost:8545`).
- Use the accounts provided by Hardhat for testing transactions within the DApp.
- The application allows you to create and manage escrow contracts on the Ethereum blockchain.

## Resources

- Alchemy Ethereum Development Tutorials: https://www.alchemy.com/overviews/ethereum-development-tutorials
- Hardhat Documentation: https://hardhat.org/getting-started/
- MetaMask Documentation: https://docs.metamask.io/guide/
