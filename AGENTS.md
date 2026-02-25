# AGENTS.md

## Cursor Cloud specific instructions

### Project overview
This is an NFT Marketplace Solidity smart contract project built with Hardhat. There is no frontend — only the smart contract (`contracts/NFTMarketplace.sol`) and boilerplate Hardhat scaffolding.

### Key commands
- **Compile:** `npx hardhat compile`
- **Test:** `npx hardhat test`
- **Local node:** `npx hardhat node`
- **Deploy script:** `npx hardhat run scripts/deploy.js`
- **Console:** `npx hardhat console`

### Known issues
- The tests in `test/Lock.js` and the deploy script in `scripts/deploy.js` are Hardhat boilerplate that reference a `Lock` contract which does not exist. Only `NFTMarketplace.sol` is in the `contracts/` directory. Running `npx hardhat test` will show 9 failing tests — this is a pre-existing repo issue, not an environment problem.
- Hardhat emits a warning about Node.js v22 not being officially supported. This does not affect functionality.

### Running the contract
To deploy and interact with the NFTMarketplace contract locally, use `npx hardhat run scripts/<your_script>.js`. The Hardhat in-memory network spins up automatically — no persistent node is required for script execution or tests.
