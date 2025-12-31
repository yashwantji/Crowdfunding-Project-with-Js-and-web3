
Prerequisites
Ensure Node.js and npm are installed.
For the web3 part, you may need a local Ethereum node like Hardhat's built-in node or Ganache, but Hardhat handles this.
Running the Client (React Frontend)
Navigate to the client directory:

cd client
Install dependencies (if not already done):

npm install
Start the development server:

npm run dev
This will start the Vite dev server, typically on http://localhost:5173.
Running the Web3 (Smart Contracts)
Open a new terminal and navigate to the web3 directory:

cd web3
Install dependencies:

npm install
Compile the contracts:

npm run build
Start a local Hardhat node (for testing):

npx hardhat node
This runs a local blockchain on http://127.0.0.1:8545.
In another terminal (still in web3 directory), deploy the contracts to the local network:

npx hardhat run scripts/deploy.js --network localhost
(Note: The README uses npm run deploy, but for local development, use the above command. You may need to create a deploy script if it doesn't exist.)
Connecting Frontend to Contracts
The client is configured to connect to the contracts via Thirdweb SDK. Ensure the contract addresses are updated in the client code after deployment.
Open the client in your browser and interact with the dApp.
