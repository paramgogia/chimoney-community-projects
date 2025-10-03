# Polygon zkEVM 🧠

Polygon zkEVM is a Layer 2 scaling solution for Ethereum that leverages the power of Zero-Knowledge (ZK) proofs to offer significantly higher throughput and lower transaction fees, all while inheriting the security of the Ethereum mainnet. It is designed to be equivalent to the Ethereum Virtual Machine (EVM), which means developers can deploy their existing Ethereum smart contracts and use familiar tools without any code changes.

---

## How It Works

Polygon zkEVM operates as a **ZK-Rollup**. This means it bundles or "rolls up" thousands of off-chain transactions into a single batch and generates a cryptographic proof for it—a ZK-SNARK. This single proof is then submitted to the Ethereum mainnet to be verified by a smart contract. This process ensures that a massive batch of transactions can be validated on Layer 1 with the computational cost of a single transaction, leading to dramatic scalability improvements.

The core of this process is the **validity proof**, which mathematically guarantees the integrity of the transactions within the batch without revealing the data of each individual transaction.

---

## Key Features

* **EVM Equivalence**: No need to rewrite or modify your existing Solidity smart contracts. If it works on Ethereum, it works on Polygon zkEVM. This also means compatibility with standard Ethereum tools like MetaMask, Hardhat, and ethers.js.
* **Ethereum-Grade Security**: By settling transactions and verifying proofs on the Ethereum mainnet, Polygon zkEVM inherits the robust security and decentralization of Layer 1.
* **Massive Scalability**: It significantly increases transaction throughput, allowing for thousands of transactions per second (TPS).
* **Drastically Lower Costs**: By batching transactions, the gas cost is distributed among many users, making individual transaction fees a fraction of what they would be on the Ethereum mainnet.
* **Faster Finality**: Transactions achieve fast finality on Layer 2, with full security settlement once the ZK-proof is verified on Ethereum.

---

## Architecture Overview

The Polygon zkEVM network consists of several key components that work in tandem:

* **zkNode**: The software that clients run to participate in the network. It includes components for synchronizing, sequencing, and aggregating transactions.
* **Sequencers**: These nodes collect transactions from users, order them, and propose them in batches to be included in the L2 chain.
* **Aggregators**: These participants take the transaction data from Sequencers and generate the zero-knowledge proofs that validate the state transitions. These proofs are then submitted to Layer 1.
* **Proof of Efficiency (PoE)**: The consensus mechanism that allows anyone to become a Sequencer or an Aggregator in a permissionless way, ensuring the network remains decentralized and censorship-resistant.
* **Consensus Contract**: A smart contract deployed on the Ethereum mainnet that coordinates the Sequencers and Aggregators and verifies the validity proofs.

---

## Getting Started for Developers

Deploying your dApp on Polygon zkEVM is straightforward.

### 1. Configure Your Wallet

Add the Polygon zkEVM network to your browser wallet (e.g., MetaMask).

**Mainnet Details:**
* **Network Name**: Polygon zkEVM
* **RPC URL**: `https://zkevm-rpc.com`
* **Chain ID**: `1101`
* **Currency Symbol**: ETH
* **Block Explorer URL**: `https://zkevm.polygonscan.com/`

**Testnet (Cardona) Details:**
* **Network Name**: Polygon zkEVM Cardona Testnet
* **RPC URL**: `https://rpc.cardona.zkevm-rpc.com`
* **Chain ID**: `2442`
* **Currency Symbol**: ETH
* **Block Explorer URL**: `https://cardona-zkevm.polygonscan.com/`

### 2. Bridge Your Assets

You will need ETH on the zkEVM network to pay for gas fees. You can transfer ETH from the Ethereum mainnet to Polygon zkEVM using the official **[Polygon zkEVM Bridge](https://portal.polygon.technology/zkevm/bridge)**. For the testnet, you can use a faucet to get test ETH.

### 3. Deploy Your Contracts

Use your preferred development framework like Hardhat, Truffle, or Foundry. Simply update your configuration file to point to the Polygon zkEVM RPC URL and deploy your contracts as you would on Ethereum.

---

## Learn More

* **[Official Documentation](https://docs.polygon.technology/zkevm/)**: The primary source for all technical details.
* **[Polygon zkEVM Website](https://polygon.technology/zkevm)**: General information and ecosystem updates.
* **[Block Explorer](https://zkevm.polygonscan.com/)**: Explore transactions, blocks, and contracts on the mainnet.
* **[Developer Community](https://discord.com/invite/polygon)**: Join the Polygon Discord to connect with other developers and get support.
