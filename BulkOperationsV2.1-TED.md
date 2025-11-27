# Alpha Omega Coin (AOC) The Queen of cryptocurrencies
<br>

# Technical Explanatory Documentation (TED) 
## About 
## AOC BEP20 V2.1 Token Bulkoperations Smart Contract 
<br>

## Overview:

The **BulkOperations contract** enables bulk token transfers and distribution requests for **AOC BEP20 V2.1 tokens,** interacting with the **Alpha Omega Coin (AOC) BEP20 V2.1 Token contract.** All functions are owner-only and are categorized as **read** or **write**. Find them as follows : 

# Part 1 : Alpha Omega Coin  (AOC) BEP20 V2.1 Token  Identification Core Details
- **Name**: Alpha Omega Coin (AOC)
- **Symbol**: AOC
- **Decimals**: 18
- **Initial Fixed Supply** : 1,000,000,000,000 (**1 trillion**)
- **Total Maximum Fixed Supply** : 1,000,000,000,000 (**1 trillion**) _**No minting and No Burning**_
- **TYPE**: **U**tility, **D**onation, **C**harity and **P**ayment **T**oken (**UDCPT**) 
- **Network** / **Blockchain**: **B**inance **S**mart **C**hain (**BSC**)
- **Version** : Version 2.1 (V2.1)
- **Upgradeability**: Uses OpenZeppelin UUPS (Universal Upgradeable Proxy Standard)
- **Pausable**: Multi-sig Owners can pause/unpause transfers for security sake, migration sake or for a community-oriented intervention
- **Blacklist**: Multi-Sig Owners can block addresses from sending/receiving tokens for security sake, scam prevention, protection from malicious attacks and also for internal regulations sake




# Part 2 : AOC BEP20 V2.1 Token BulkOperations Smart Contract Testnet + Mainnet Codes Identification Urls 
# Testnet : 
**Explorer**:  https://testnet.bscscan.com/address/0xc5d3be6E0D5EA8Ac07dB001cf2D08A836546088d#readProxyContract
  
**Github** : 
- **Branch Name:** testnet-V2.4
- **Branch Link:** https://github.com/alphaomegacoinaoc/AOC-Bep20-V2-token-distribution-contract/blob/testnet-v2.4/contracts/BulkOperationsV2.1.sol


## Mainnet :
**Explorer**: https://bscscan.com/address/0x0c5418a22adad61d61ecd0d346d759f2b8fe1c3d#writeProxyContract
  
**Github** : 
- **Branch Name:** main-v2.1
- **Branch Link:** https://github.com/alphaomegacoinaoc/AOC-Bep20-V2-token-distribution-contract/blob/main-v2.1/contracts/BulkOperationsV2.1.sol



# Part 3 : AOC BEP20 V2.1 Token BulkOperations  Multi-Sig Smart Contract Testnet + Mainnet Codes Identification Urls 
# Testnet : 
**Explorer:**  https://testnet.bscscan.com/address/0x115D01dD6723ed1BC0DF2EB6A64350341a29fbBC#code

**Github :** 
- **Branch Name:** testnet-v1.0.0
- **Branch Link:** https://github.com/alphaomegacoinaoc/alphaomegacoinaoc-Multi-Sig-Contract/blob/testnet-v1.0.0/MultiSigTokenVault.sol

# Mainnet :
**Explorer:** https://bscscan.com/address/0x7c40e3711b23f80af63fba90ac3094ca8baab137#writeProxyContract

**Github :**
- **Branch Name:** Mainnet-v1.0.0
- **Branch Link:** https://github.com/alphaomegacoinaoc/alphaomegacoinaoc-Multi-Sig-Contract/blob/Mainnet-v1.0.0/MultiSigTokenVault.sol

# Part 4 :AOC BEP20 V2.1 Token BulkOperations Smart Contract Read + Write Functions
## 2.1 Read Functions
- _None : The **BulkOperations** contract has **no read-only functions**._

## 2.2 Write Functions
### Function: initialize(address _aoc)
 - **What it does:** Sets the _**Alpha Omega Coin (AOC) BEP20 V2.1 Token**_ contract address for interaction and _initializes ownership and pausability_.
- **Purpose:** Configures the contract to work with **Alpha Omega Coin (AOC) BEP20 V2.1 Token.**
### Function: _authorizeUpgrade(address newImplementation)
- **What it does:** Authorizes a _contract upgrade (owner-only)._
- **Purpose:** Enables _future contract improvements securely._
### Function: bulkTransfer(address[] recipients, uint256[] amounts)
- **What it does:** Transfers **AOC BEP20 V2.1 Tokens** from the **Multi-Sig Owners** to _multiple recipients in one transaction,_ checking the owner’s balance and AOC BEP20 V2.1 Tokens limits _**(e.g., blacklisting, LTAF/RAMS).**_
- **Purpose:** Enables _efficient distribution of tokens to multiple addresses._
### Function: bulkDistribution(string date, uint256 count)
- **What it does:** Emits an event with a date and count, signaling a bulk distribution request.
- **Purpose:** Facilitates off-chain or future on-chain distribution processes _**(no token transfer).**_

