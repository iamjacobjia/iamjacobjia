# Build A Blockchain with Rust

> - Repo: [https://github.com/jacob-chia/tinychain](https://github.com/jacob-chia/tinychain)

## Table of Contents

- [00 | Overview](README.md)
- [01 | Architecture](doc/en/01-architecture.md)
- [02 | Initialization: Pre-commit Hooks & Github Action](doc/en/02-init-project.md)
- [03 | Defining Data Structure & API](doc/en/03-data-structure-api.md)
- [04 | Wallet: Sign & Verify](doc/en/04-wallet.md)
- [05 | Command Line & Config File](doc/en/05-cmd-config.md)
- [06 | Thinking in Libp2p](doc/en/06-libp2p.md)
- [07 | Tinyp2p: A CSP Concurrency Model](doc/en/07-tinyp2p.md)
- [08 | Network Layer](doc/en/08-network.md)
- [09 | Biz Layer: How to Do Read/Write Separation?](doc/en/09-biz.md)
- [10 | Data Layer & Demo](doc/en/10-data.md)

## Intro

This project aims to demonstrate the basic principles of blockchain through a `distributed ledger`. The main features include:

- `HTTP JSON API` provides users with interfaces such as `transfer` and some `query` apis;
- `P2P Protocol` is used for interaction between nodes, and data is serialized/deserialized by `protobuf`. The functions include `peer discovery`, `transaction broadcast`, `block broadcast`, and `block synchronization`;
- `PoW` is used as the consensus mechanism;
- `Sled`, an embedded key-value database, is used as the storage backend;
- For the convenience of demonstration, there is a `wallet` in each node that stores the users' private keys, so that the node can sign the transaction on behalf of users.
