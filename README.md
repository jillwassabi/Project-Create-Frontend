# Betting Game

This Solidity smart contract enables a betting system where users can place bets of 1 ETH with a chance to win 2 ETH based on a randomly generated number.

__Functions__

- getBalance(): Returns the current balance of the contract.
- determineWin(uint256 randomNumber): Internal function that determines if the generated random number (from 1 to 6) results in a win (specifically when the random number is 1, 3, or 5).
- placeBet(): Allows users to place a bet of exactly 1 ETH. It generates a random number based on block data and checks if the user wins. If they win, the contract pays out 2 ETH (assuming sufficient balance) to the user and emits a Win event. If they lose, the contract keeps the bet amount and emits a Lose event.

__Events__

- Deposit: Triggered when a user deposits funds into the contract.
- BetPlaced: Triggered when a user places a bet, capturing the bettor's address, bet amount, generated random number, and whether they won.
- Win: Triggered when a user wins a bet, indicating the amount won.
- Lose: Triggered when a user loses a bet, indicating the amount lost.

# How to Run the Program:

1. Inside the project directory, open the terminal and type: npm i
2. Open two additional terminals in your VS Code.
3. In the second terminal, type: npx hardhat node
4. In the third terminal, type: npx hardhat run --network localhost scripts/deploy.js
5. In the first terminal, type: npm run dev to launch the front-end.
6. After these steps, the project will be running on your localhost, typically at http://localhost:3000/.
