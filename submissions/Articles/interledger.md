# Interledger Protocol (ILP) 💸

Interledger is an open protocol for sending payments across different payment networks or "ledgers." Think of it as the internet's TCP/IP, but for value. Just as the internet routes packets of data between networks, Interledger routes packets of value, enabling seamless transactions between different systems like PayPal, Venmo, traditional bank accounts, and cryptocurrencies.

---

## How It Works

Interledger enables interoperability without requiring every network to trust each other directly. Instead, it uses intermediaries called **Connectors**.



The process works like this:
1.  **Initiation**: A sender on Ledger A wants to send money to a receiver on Ledger C.
2.  **Routing**: The payment is broken down into small packets of value. Connectors form a path between Ledger A and Ledger C, potentially passing through Ledger B.
3.  **Secure Escrow**: Each connector in the path makes a conditional payment to the next connector using a cryptographic escrow mechanism (Hashed Timelock Agreements). The funds are locked and are only released when the receiver provides a cryptographic proof of receipt.
4.  **Settlement**: Once the receiver acknowledges receipt, the proof is passed back along the chain, unlocking the funds at each step. This ensures the entire transaction is **atomic**—it either completes successfully across all ledgers, or it fails and all funds are returned. No party can lose money.

This system allows for secure, fast, and efficient payments between otherwise incompatible systems.

---

## Core Concepts

* **Ledgers**: Any system that can track balances. This could be a bank, a mobile money app, a cryptocurrency blockchain, or even a simple database.
* **Connectors**: Routers that transfer value between ledgers. Connectors earn a small fee for providing this service but never take custody of the funds being transferred.
* **ILP Packets**: Standardized data packets that contain information about the sender, receiver, amount, and condition for the payment.
* **Interledger Address**: A universal address used to identify an account on any ledger. It's similar to an email address or an IP address, providing a standardized way to route payments. For example: `g.us.paypal.alice`.

---

## Key Features

* **Ledger Agnostic**: Works with any type of payment network, whether centralized or decentralized.
* **Currency Agnostic**: Can route payments between different currencies, with connectors handling the foreign exchange.
* **Scalability**: By breaking payments into small packets, Interledger can handle a high volume of transactions.
* **Security**: The use of cryptographic escrows eliminates counterparty risk. Connectors cannot steal funds in transit.
* **No Global Ledger**: It doesn't rely on a single blockchain or central authority, making it highly decentralized and resilient.

---

## Getting Started

Ready to build with Interledger? Here are some resources to help you get started:

* **[Interledger Website](https://interledger.org/)**: The official source for information, use cases, and community news.
* **[Official Documentation](https://interledger.org/developers)**: Dive into the technical specifications, tutorials, and developer guides.
* **[Rafiki](https://rafiki.dev/)**: An open-source, production-ready implementation of an Interledger connector and service, maintained by the Interledger Foundation. It's a great starting point for building ILP-enabled applications.
* **[Awesome Interledger](https://github.com/interledger/awesome-interledger)**: A curated list of Interledger projects, tools, and resources from the community.

---

## Learn More

Interledger is a community-driven project with a growing ecosystem.

* **Join the Community**: Get involved by joining the [Interledger Community Forum](https://community.interledger.org/) or the [Slack/Discord channels](https://interledger.org/community).
* **Read the Whitepapers**: For a deep dive, check out the original [Interledger whitepapers](https://interledger.org/rfcs/) that detail the protocol's architecture and design.
