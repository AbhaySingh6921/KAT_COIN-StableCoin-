# 🪙 KAT Stablecoin Engine (Decentralized Stablecoin Protocol)

A decentralized and overcollateralized stablecoin protocol built with Solidity and Foundry. Inspired by protocols like MakerDAO’s DAI, this implementation features core mechanics like collateral deposits, minting, burning, liquidation, and price feed integration via Chainlink oracles.

---

## ⚙️ Features

- ✅ **Collateralized Minting**: Deposit whitelisted ERC20 tokens like WETH or WBTC to mint KAT (stablecoin).
- 🔥 **Burn & Redeem**: Burn KAT tokens to reclaim your collateral.
- 🧯 **Liquidations**: Secure the protocol by liquidating unhealthy positions and claiming collateral with a bonus.
- 📊 **Price Feeds**: Chainlink price oracles ensure accurate USD values for tokens.
- 🔒 **Safety Checks**: Health factor enforcement to ensure positions are always sufficiently collateralized.
- 🧪 **Test Suite**: Unit tests using Foundry covering edge cases, errors, and core logic.

---

## 🛠️ Architecture

### Core Contracts

| Contract         | Responsibility                            |
|------------------|-------------------------------------------|
| `KATEngine`      | Manages collateral, minting, burning, liquidations |
| `DecentralizedStableCoin` | ERC20 token representing the stablecoin (KAT) |
| `HelperConfig`   | Network-specific configuration and price feeds |
| `DeployKAT`      | Deployment script using Foundry scripting tools |

---

## 🔐 Security Mechanisms

- **NonReentrant Modifier** to protect sensitive logic from reentrancy.
- **Health Factor** logic to ensure overcollateralization.
- **Access Control** to prevent unauthorized minting.
- **Events** for transparent on-chain activity tracking.

---

## 🚀 Getting Started

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation) installed
- Node.js & npm (optional for scripting)
- Git, a code editor (VSCode recommended)

### Installation

```bash
git clone https://github.com/yourusername/KAT-Stablecoin.git
cd KAT-Stablecoin
forge install
forge build



#catorgaized of stable coin
```Our stablecoin is going to be:

1. Relative Stability: Anchored or Pegged to the US Dollar
   1. Chainlink Pricefeed
   2. Function to convert ETH & BTC to USD
2. Stability Mechanism (Minting/Burning): Algorithmicly Decentralized
   1. Users may only mint the stablecoin with enough collateral
3. Collateral: Exogenous (Crypto)
   1. wETH
   2. wBTC
```
