# Donation
Quick Start Guide to Clone and Set Up the Donation DApp

Step 1: Clone the Project
git clone (https://github.com/josefineweine/Donation.git)
cd donation-dapp

Step 2: Install Dependencies

Backend (Smart Contract) - Optional

If you want to deploy the contract yourself (optional), follow these steps. If not, skip to the Frontend steps. You can use mine contract adress: CONTRACT_ADDRESS=0x0b54FAD894c1EFC7B190cE92D122F5E93704D04B
      1.    Go to the backend/ folder:
cd backend

      2.    Install dependencies:
npm install

      3.    Compile the contract:
npx hardhat compile

      4.    Deploy the contract to Goerli or any testnet (make sure you have Alchemy keys and a funded wallet for Goerli):

npx hardhat run scripts/deploy.js --network goerli

Step 3: Set Up Environment Variables

Frontend .env (inside frontend/):
      1.    If you’ve deployed the contract yourself, copy the contract address from the deployment script. If you don’t want to deploy it yourself, you can use any existing deployed contract.

      2.    Create a .env file in frontend/ folder:
REACT_APP_ALCHEMY_API_URL=https://eth-goerli.alchemyapi.io/v2/your-alchemy-api-key
REACT_APP_CONTRACT_ADDRESS=your-deployed-contract-address

Step 4: Run the Frontend App
      1.    Go to the frontend folder:
cd frontend

      2.    Install dependencies:
npm install

      3.    Run the app:
npm start

      4.    The app will now be running at http://localhost:3000.

Step 5: Log in with MetaMask
      •     When you open the app, it will prompt you to connect your MetaMask wallet to the DApp.
      •     You can now start interacting with the contract, donating ETH, and viewing the donation data in real-time.

