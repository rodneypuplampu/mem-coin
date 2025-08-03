# Mem-Coin Protocol

This repository contains the reference implementation for the Mem-Coin protocol, a framework for decentralized AI computation on the blockchain.

## Directory Structure

Here is the recommended directory structure for the project:

```
/
├── .github/              # GitHub-specific files (e.g., issue templates, workflows)
│   └── workflows/        # CI/CD workflows for automated testing and deployment
├── api/                  # gRPC API definitions for immutable, multi-layered communication
│   └── v1/
│       └── memcoin.proto # Protobuf file for the core Mem-Coin API
├── docs/                 # Project documentation
│   ├── rfc/              # The open-source RFC info paper
│   │   └── rfc-xxxx-mem-coin-framework.md
│   ├── architecture.md   # A detailed explanation of the system architecture
│   └── integration/      # Guides for integrating with other crypto currencies
│       └── bitcoin.md    # Specific guide for Bitcoin stack compatibility
├── src/                  # Source code for the protocol implementation
│   ├── core/             # Core protocol logic
│   │   ├── pouw/         # Optimistic Proof-of-Useful-Work (PoUW) implementation
│   │   ├── optimistic/   # Optimistic verification and challenge period logic
│   │   └── vdo/          # VDO/memvid data structure handling for AI computations
│   ├── node/             # The blockchain node implementation
│   │   └── ...
│   ├── governance/       # MPC-HSM Committee implementation for high-assurance governance
│   │   └── ...
│   ├── sentinel/         # The autonomous AI Sentinel for network monitoring and arbitration
│   │   └── ...
│   └── cli/              # Command-line interface for interacting with the protocol
│       └── ...
├── examples/             # Example code demonstrating how to use the API and protocol
│   ├── python/           # Python examples
│   └── go/               # Go examples
├── tests/                # Unit and integration tests for all components
│   ├── unit/
│   └── integration/
├── scripts/              # Helper scripts for building, deploying, and managing the project
│   ├── build.sh
│   └── deploy.sh
├── .gitignore            # A list of files and directories to be ignored by version control
├── LICENSE               # The open-source license for the project
└── README.md             # This file: an overview of the project and how to get started
```

---

## Key Components

### Core Protocol (`/src/core/`)
- **PoUW Implementation**: Handles the Proof-of-Useful-Work consensus mechanism
- **Optimistic Verification**: Manages challenge periods and dispute resolution
- **VDO Handling**: Processes Verifiable Data Objects for AI computations

### Governance (`/src/governance/`)
- **MPC-HSM Committee**: Multi-Party Computation with Hardware Security Modules
- **High-Assurance Decision Making**: Cryptographically secure governance processes
- **Protocol Upgrades**: Manages network upgrades and parameter changes

### AI Sentinel (`/src/sentinel/`)
- **Network Monitoring**: Continuous surveillance of network activity
- **Fraud Detection**: AI-powered anomaly detection and threat identification
- **Autonomous Response**: Automated responses to security threats

### Node Implementation (`/src/node/`)
- **Blockchain Core**: Full node implementation with consensus
- **P2P Networking**: Peer-to-peer communication protocols
- **State Management**: Blockchain state storage and synchronization

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/mem-coin/protocol.git
   cd protocol
   ```

2. **Build the project**
   ```bash
   ./scripts/build.sh
   ```

3. **Run tests**
   ```bash
   ./scripts/test.sh
   ```

4. **Start a node**
   ```bash
   ./src/cli/memcoind start --config config/default.toml
   ```

## API Documentation

The gRPC API definitions are located in `/api/v1/memcoin.proto`. Generate client libraries using:

```bash
protoc --go_out=. --go-grpc_out=. api/v1/memcoin.proto
```

## Contributing

This structure provides a clear separation of concerns, making it easier for developers to:
- Navigate the codebase
- Understand different system components
- Contribute to specific areas of expertise
- Maintain code quality and consistency

Please refer to `CONTRIBUTING.md` for detailed contribution guidelines.

## License

This project is licensed under the terms specified in the `LICENSE` file.
