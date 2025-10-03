# Hyperledger Besu 🚀

Hyperledger Besu is an open-source, enterprise-grade Ethereum client written in Java. It's designed to be versatile, allowing you to run it on the public Ethereum Mainnet or on private, permissioned networks. As a project under the Hyperledger umbrella, Besu is built with the needs of businesses in mind, offering features for privacy, permissioning, and various consensus algorithms.



---

## Key Features

* **Ethereum Mainnet Compatible**: Fully compliant with the Ethereum Mainnet, allowing it to act as a standard node on the public network.
* **Multiple Consensus Algorithms**: Supports various consensus mechanisms to fit different network needs:
    * **Proof of Work (PoW)**: For mining on networks like Ethereum.
    * **Proof of Stake (PoS)**: For participating as a consensus and execution client on networks like the Ethereum Mainnet.
    * **Proof of Authority (PoA)**: Includes **IBFT 2.0** and **QBFT**, which are ideal for private or consortium networks that require faster block times and higher transaction throughput.
* **Enterprise-Focused**: Offers advanced features for enterprise use cases, including comprehensive permissioning schemes (node-level and account-level) and privacy controls.
* **Built in Java**: Developed in Java and licensed under Apache 2.0, making it accessible to a large community of developers.
* **Extensive APIs**: Provides standard Ethereum JSON-RPC APIs as well as additional APIs for administrative tasks and monitoring.
* **Monitoring and Diagnostics**: Comes with built-in tools for monitoring node health and performance through Prometheus and Grafana.

---

## Getting Started

This guide provides a quick overview. For in-depth instructions, tutorials, and network configuration details, please refer to the **[Official Hyperledger Besu Documentation](https://besu.hyperledger.org/)**.

---

## Prerequisites

Before you begin, ensure you have the following installed on your system:
* **Java 17+**: Besu is a Java application and requires a compatible JDK. You can check your version with:
    ```sh
    java -version
    ```

---

## Installation

You can install and run Besu in several ways.

### Option 1: Using Binary Releases

1.  Download the latest binary release from the [Besu GitHub Releases page](https://github.com/hyperledger/besu/releases).
2.  Unpack the downloaded file:
    ```sh
    tar -xzf besu-<version>.tar.gz
    ```
3.  Navigate into the directory:
    ```sh
    cd besu-<version>
    ```
4.  You can now run Besu from the `bin` directory.

### Option 2: Using Docker

A Docker image is available on Docker Hub, which is often the easiest way to get started.

1.  Pull the latest Besu image:
    ```sh
    docker pull hyperledger/besu:latest
    ```
2.  Run the container:
    ```sh
    docker run hyperledger/besu:latest --help
    ```

---

## Running a Node

To run a Besu node, you simply execute the `besu` command with the desired options.

### Example: Running a Development Node

A development node is perfect for local testing. It generates a genesis file and a key pair for you.

```sh
besu --network=dev --miner-enabled --miner-coinbase=<YOUR_ETHEREUM_ADDRESS> --rpc-http-enabled --rpc-http-api=ETH,NET
