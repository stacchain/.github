<p align="left">
    <img src="https://raw.githubusercontent.com/stacchain/.github/main/profile/stacchain-ghbanner.svg" alt="stacchain Logo" width="100%" />
</p>

<br/>

StacChain is an open-source initiative building the standards and infrastructure to bring **Deep Integrity**, **Provenance**, and **Web3 Economics** to the geospatial ecosystem.

> **Our Goal:** To upgrade the STAC specification from "Discovery" to "Commerce."

---

## The Architecture

StacChain is not a monolith; it is a suite of modular standards and middleware that connect the geospatial web to the decentralized web.

### 1. The Data Standard: Deep Integrity
We maintain the specs that turn mutable metadata into immutable assets.
* **[merkle-tree](https://github.com/stacchain/merkle-tree):** The STAC Metadata Extension for cryptographically binding raw assets (GeoTIFFs) to Item metadata using Merkle Roots.
* **[stac-api-merkle-verification](https://github.com/stacchain/stac-api-merkle-verification):** The OpenAPI specification defining the standard `GET /verify` endpoints for server-side integrity checks.

### 2. The Middleware: Trust and Verification
We build backend-agnostic libraries that can be dropped into existing STAC implementations.
* **[stac-fastapi-merkle](https://github.com/stacchain/stac-fastapi-merkle):** A Python extension that adds integrity verification to *any* `stac-fastapi` backend (Postgres, Elasticsearch, etc.).
* **[stac-merkle-tree-cli](https://github.com/stacchain/stac-merkle-tree-cli):** The core utility for hashing datasets, generating proofs, and managing local trees.

### 3. The Economy: Tokenized Access
We are building the bridge between STAC APIs and EVM-compatible blockchains.
* **[stacchain-smart-contracts](https://github.com/stacchain/stacchain-smart-contracts)**: Solidity contracts for Registry Anchoring and Tokenized Licenses.

---

## Core Repositories

| Layer | Repo | Status | Description |
| :--- | :--- | :--- | :--- |
| **Spec** | **[merkle-tree](https://github.com/stacchain/merkle-tree)** | **Stable** | The Metadata Schema defining `merkle:root` and `merkle:object_hash`. |
| **Spec** | **[stac-api-merkle-verification](https://github.com/stacchain/stac-api-merkle-verification)** | **Beta** | The API Specification for server-side verification endpoints. |
| **Code** | **[stac-fastapi-merkle](https://github.com/stacchain/stac-fastapi-merkle)** | **Beta** | Python middleware for adding verification logic to `stac-fastapi`. |
| **Tooling** | **[stac-merkle-tree-cli](https://github.com/stacchain/stac-merkle-tree-cli)** | **Stable** | CLI tool for hashing datasets and generating inclusion proofs. |
| **Web3** | **[stacchain-smart-contracts](https://github.com/stacchain/stacchain-smart-contracts)** | **Alpha** | Solidity contracts for Registry Anchoring and Tokenized Licenses. |

---

## Future Direction

We have established the foundation for **Integrity** (proving the data is real). The next frontier is **Commerce** (enabling peer-to-peer data markets). While the exact implementation details are evolving, we are exploring two major pathways.

### The "Gatekeeper" Concept
We envision a middleware service that replaces traditional API Keys with cryptographic proofs of ownership.
* **Wallet-Based Auth:** Authenticating users via SIWE (Sign-In with Ethereum) to establish persistent, portable identity.
* **License Tokens:** Representing data usage rights (e.g., "Commercial Use: 1 Year") as ERC-1155 tokens.
* **Access Control:** A service that intercepts STAC API requests, validates the user's token balance on-chain, and issues short-lived, signed URLs for asset access.

### The Decentralized Marketplace
We are investigating how to enable direct, automated settlement between data providers and consumers.
* **Direct Sales:** Allowing data providers to list STAC Collections directly on-chain.
* **Instant Settlement:** Enabling users to purchase "License Tokens" with stablecoins, providing immediate revenue to the publisher and immediate API access to the buyer.
* **Automated Royalties:** Using smart contracts to automatically split revenue between satellite operators, algorithm developers, and platform hosts.

---

## Community & Contributing

We are deeply committed to the principles of open source. StacChain is designed to be a community-driven standard, not a walled garden.

* **Project Lead:** [**Jonathan Healy**](https://github.com/jonhealy1)
* **Discussions:** [Join the conversation](https://github.com/orgs/stacchain/discussions)

We welcome contributions of all kinds—whether you are a cryptographer, a geospatial engineer, or a documentation wizard.

*Built with ❤️ for the Open Metaverse.*
