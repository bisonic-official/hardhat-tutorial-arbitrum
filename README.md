# Hardhat Contract Tutorial

This repository aims to document the process of deploying a smart contract using Arbitrum.

Please follow steps 1-6 from: https://hardhat.org/tutorial

> The repo contains code for steps 1-6, you can just compile and run tests for the contract.

Once you reach step 7, you just need to modify the `hardhat.config.js` file as follows:

```js
require("@nomicfoundation/hardhat-toolbox");

// Replace this private key with your Goerli account private key
// To export your private key from Metamask, open Metamask and
// go to Account Details > Export Private Key
// Beware: NEVER put real Ether into testing accounts
const GOERLI_PRIVATE_KEY = "";

/** @type import('hardhat/config').HardhatUserConfig */
module.exports = {
  solidity: "0.8.17",
  networks: {
    goerli: {
      url: `https://goerli-rollup.arbitrum.io/rpc`,
      accounts: [GOERLI_PRIVATE_KEY]
    }
  }
};
```

Please note that you need to add your `GOERLI_PRIVATE_KEY` to the file, and the URL used for deployment using Goerli and Arbitrum must be: https://goerli-rollup.arbitrum.io/rpc

> More details about public chains in Arbitrum: https://developer.arbitrum.io/public-chains

### **IMPORTANT!**

You need to have Arbitrum Goerli ETH for testing purposes.

You can get Goerli credits from the Goerli Faucet:
https://goerlifaucet.com/

In order to convert Goerli ETH to Arbitrum Goerli ETH, you can use the Arbitrum Bridge: https://bridge.arbitrum.io/?l2ChainId=421613