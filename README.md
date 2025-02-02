# Flashloan_Arbitrage
This a smart contract for performing arbitrage with AAVE flashloan between Uniswap & Sushiswap

Features:
Flashloans are one of the most exciting concept in the web3.0 & Defi industry, they allow users to borrow a large amounts of assets (ERC20) and use the them for any kind of application in condition that the borrowed money is returned in the same transaction.Many protocols provide the possibility of flashloan like aave, uniswap, dydx,...

The FlashLoanArbitrage smart contrat uses the aave flashloan to do arbitrage between Uniswap & Sushiswap exchanges, it's devided into 2 part: The first is for the arbitrage logic and deposit and withdraw functionalities and the second implement the flashloan logic that can be found in the aave Docs

Built With:
Solidity
Brownie
OpenZeppelin
Usage:
Installation & Setup:
Installing Brownie: Brownie is a python framework for smart contracts development,testing and deployments. It's quit like HardHat but it uses python for writing test and deployements scripts instead of javascript. Here is a simple way to install brownie.

 pip install --user pipx
 pipx ensurepath
 # restart your terminal
 pipx install eth-brownie
Or if you can't get pipx to work, via pip (it's recommended to use pipx)

pip install eth-brownie
Install ganache-cli:

 npm install -g ganache-cli
Clone the repo:


cd aave-flashloan-arbitrage
Set your environment variables:

To be able to deploy to real testnets you need to add your PRIVATE_KEY (You can find your PRIVATE_KEY from your ethereum wallet like metamask) and the infura project Id (just create an infura account it's free) to the .env file:

PRIVATE_KEY=<PRIVATE_KEY>
WEB3_INFURA_PROJECT_ID=<< YOUR INFURA PROJECT ID >>
How to run:
To start an arbitrage on the mainnet fork (for testing purposes only, you can also use the kovan testnet) you just need to run the command :

brownie run scripts/flashloan_arbitrage.py --network=mainnet-fork
