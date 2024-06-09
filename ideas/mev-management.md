# MEV Management (MEVBoost++)

## Summary
In the current MEV supply chain, validators can only offer a limited commitment – that they won’t double-sign conflicting block headers (equivocation). EigenLayer expands this landscape by enabling validators to make diverse commitments, allowing the development of various MEV mechanisms. This proposal introduces MEV-Boost+ and MEV-Boost++, which enable proposers to have both transaction inclusion power and MEV rewards, enhancing Ethereum’s liveness and censorship resistance.

## Problem Statement
Proposers currently face a binary choice: transaction inclusion power or MEV rewards. This limitation poses significant liveness and censorship risks for Ethereum. A single malicious relay can stall the chain, and the network’s censorship resistance becomes dependent on builders' discretion. Furthermore, the current MEV-Boost design centralizes power, increasing the risks of censorship and reducing the network's overall resilience.

## Proposed Solution
MEV-Boost+ and MEV-Boost++ allow proposers to auction off a portion of their block through a trusted relay (MEV-Boost+) or without a trusted relay (MEV-Boost++). These mechanisms provide options for partial block auctions, enabling proposers to retain some transaction inclusion power while still benefiting from MEV rewards. 

The expanded range of MEV mechanisms under EigenLayer allows validators to express their preferences more comprehensively, thus increasing the robustness and decentralization of the Ethereum network.

## Benefits
- **Enhanced Liveness**: Reduces the risk of a single malicious relay stalling the chain.
- **Censorship Resistance**: Increases the network’s resistance to censorship by restoring proposers' transaction inclusion power.
- **Economic Guarantees**: Provides cryptoeconomic guarantees to builders, ensuring fair compensation if atomicity is broken.
- **Decentralization**: Spreads the power across more nodes and relays, reducing centralization risks.

## Technical Details

- **Architecture**: 
  The MEV-Boost+ and MEV-Boost++ services will consist of:
  1. **Partial Block Relays**: Nodes that handle partial block auctions.
  2. **Full Block Relays**: Nodes that handle full block auctions.
  3. **Proposers**: Nodes that construct and propose blocks.
  4. **Builders**: Nodes that build partial or full blocks.
  5. **EigenLayer**: Provides economic trust and slashing mechanisms.

- **Components**:
  - **Partial Block Relay**: Facilitates the auction of partial blocks.
  - **Full Block Relay**: Facilitates the auction of full blocks.
  - **Proposer Node**: Constructs and proposes blocks based on received bids.
  - **Builder Node**: Builds partial or full blocks for auction.
  - **EigenLayer**: Ensures economic trust and handles slashing for malicious behavior.

- **Technologies**:
  - **EigenLayer**: For decentralized trust and economic mechanisms.
  - **Relay Protocols**: For handling partial and full block auctions.
  - **Slashing Mechanisms**: For penalizing malicious proposers or builders.

- **Implementation Plan**:
  1. **Design Service Architecture**: Define roles and responsibilities of partial block relays, full block relays, proposers, and builders.
  2. **Develop Relay Protocols**: Implement protocols for partial and full block auctions.
  3. **Set Up Nodes**: Deploy relay, proposer, and builder nodes with substantial Ethereum stakes.
  4. **Economic Trust Integration**: Implement mechanisms to leverage EigenLayer for economic trust and slashing.
  5. **Testing and Validation**: Thoroughly test the services for reliability, security, and performance.
  6. **Documentation**: Provide detailed documentation and usage guidelines.

- **Challenges**:
  - **Ensuring Coordination**: Coordinating partial and full block auctions across a decentralized network.
  - **Security**: Protecting the auction process from malicious actors.
  - **Guaranteeing Fair Compensation**: Ensuring builders are fairly compensated if atomicity is broken.

## Use Cases
- **Partial Block Auctions**: Allowing proposers to auction off parts of the block while retaining some inclusion power.
- **Full Block Auctions**: Allowing proposers to auction off entire blocks for maximum MEV rewards.
- **Enhanced Censorship Resistance**: Increasing the network’s resistance to censorship by restoring proposers' transaction inclusion power.

## Market Research
Market research shows that the existing MEV extraction mechanisms significantly impact Ethereum's decentralization and censorship resistance. The demand for more decentralized and secure MEV extraction solutions is growing, with increasing attention on proposals that enhance proposer power and network resilience.

## Competitor Analysis
Current MEV solutions, such as traditional MEV-Boost, centralize power and limit proposers' flexibility. MEV-Boost+ and MEV-Boost++ offer improved decentralization and security by allowing partial block auctions and eliminating the need for a trusted relay, addressing the weaknesses of existing solutions.

## Resources Required
- **Development Team**: Experienced blockchain developers to implement relay protocols and integrate with EigenLayer.
- **Testing Infrastructure**: Testnet environment for thorough testing and validation.
- **Economic Resources**: Ethereum stakes for deploying nodes and ensuring economic trust mechanisms.

## Risk Assessment
- **Coordination Risks**: Ensuring smooth coordination across decentralized nodes and relays.
- **Security Risks**: Protecting the auction and slashing mechanisms from malicious attacks.
- **Economic Risks**: Guaranteeing fair compensation to builders if atomicity is broken.

## References
- [EigenLayer Documentation](https://eigenlayer.com/docs)
- [MEV-Boost](https://github.com/flashbots/mev-boost)
- [Proposer-Builder Separation (PBS)](https://ethresear.ch/t/proposer-builder-separation-friendly-fee-market-designs/9725)
- [MEVBoost++ Research Proposal](https://research.eigenlayer.xyz/t/mev-boost-liveness-first-relay-design/15/2)

## Diagrams and Figures

### MEV-Boost+ and Partial Block Auction

![image](https://github.com/Layr-Labs/avs-ideas/assets/26431906/96c7877a-34bb-4c0b-af55-4c038cacf78a)

*Figure 1: MEV-Boost+ process showing the flow of partial block auction.*

![image](https://github.com/Layr-Labs/avs-ideas/assets/26431906/face6358-e382-40cd-91e0-2155c7bc679c)
*Figure 2: Interaction flow between builder, relay, MEV-Boost+, and Proposer.*

### Slashing Mechanisms

![image](https://github.com/Layr-Labs/avs-ideas/assets/26431906/45a3fb31-42c6-458b-9080-6012851aee5e)
*Figure 3: Slashing mechanism for proposers violating partial block atomicity.*
