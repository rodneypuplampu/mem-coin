# Mem-Vid Cryptocurrency Protocol
Mem-coin is a Cryptocurrency protocol based on Memvid video Machine Learning embeddings and vector media storage.

Welcome to the official repository for the Mem-Vid Protocol, an open-source cryptocurrency revolutionizing the intersection of artificial intelligence, blockchain, and finance. This protocol introduces a hybrid verification architecture designed for efficiency, security, and real-world adoption.

The foundational data layer of our protocol is the `memvid` library, an innovative technology for highly compressed, verifiable data objects. For more information on this core component, please see the original implementation here: <https://github.com/Olow304/memvid>.

This repository is based on the principles outlined in the foundational whitepaper, "Architectural Simplification and Hardening of the Mem-Coin Protocol: A Hybrid Verification Approach".

## Introduction to the Mem-Vid Cryptocurrency

Mem-Vid represents a significant evolution in blockchain design, engineered to address the critical challenges of cost, energy consumption, and scalability that face many current cryptocurrencies. The protocol is built on the groundbreaking idea of **Proof-of-Useful-Work (PoUW)**, where the energy spent to secure the network is not wasted on arbitrary puzzles but is instead used for productive, real-world tasks like training and running AI models.

However, the original blueprint faced a significant hurdle: the "prover's burden.". Requiring every computation to be verified by a computationally intensive Zero-Knowledge Proof (ZKP) created an unsustainable economic and energetic cost for network participants.

To solve this, Mem-Vid implements a strategic pivot to a multi-layered, hybrid verification architecture that is more practical, efficient, and accessible.

## Core Architectural Pillars

The Mem-Vid protocol is built on a sophisticated, multi-layered architecture designed for defense-in-depth security, efficiency, and regulatory compliance.

### 1. A Tiered, Hybrid Verification Model

To solve the "prover's burden," Mem-Vid replaces the mandatory ZKML verification with a more flexible, tiered system.

* **Tier 1: Optimistic PoUW (The Efficiency Layer)**
    * This is the default mechanism for verifying work on the network.
    * Miners submit their AI computation results with a substantial economic bond (a stake of MEM tokens) rather than a costly ZKP.
    * The submission is "optimistically" assumed to be correct, and a 7-day challenge period begins.
    * This model dramatically reduces costs and power consumption, making participation accessible to those with standard GPU hardware.
    * Security is crypto-economic: honest work is rewarded, and fraudulent actors are punished by having their bond "slashed" (confiscated). A portion of the slashed bond is given to the "Challenger" who successfully proves the fraud, creating a "bounty hunter" system that makes the network self-policing.

* **Tier 2: ZKML PoUW (The Premium Privacy Layer)**
    * While Optimistic PoUW is the default, Zero-Knowledge Machine Learning (ZKML) is retained as a premium, on-demand feature.
    * This allows users, such as corporations with proprietary data or AI models, to pay a higher fee to have their computation verified with a ZKP, guaranteeing absolute privacy and computational integrity.

* **Tier 3: MPC-HSM Committee (The Arbitration & Governance Layer)**
    * To prevent the collusion risks associated with a federated group of verifiers, Mem-Vid establishes a maximally secure committee for high-stakes governance and arbitration.
    * This committee uses **Secure Multi-Party Computation (MPC)**, where a single private key is split into "shards" held by committee members. A signature requires a threshold of members to interact, but the full key is never reconstructed, making collusion cryptographically impractical.
    * Each member's key shard is further protected within a **Hardware Security Module (HSM)**, a physical, tamper-resistant device, providing an unparalleled level of security against both internal collusion and external hacks.

### 2. A Regulated, Two-Tier Monetary System

To bridge the gap between decentralized innovation and traditional finance, Mem-Vid introduces a regulated, two-tier monetary system inspired by Central Bank Digital Currency
