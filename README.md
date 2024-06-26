# AVS Ideas Repository

## Welcome to AVS Ideas

This repository is a curated collection of innovative AVS project ideas for developers and builders. The list has been meticulously curated by the Eigen Labs team, representing concepts that could significantly benefit the broader Web3 community.

## Getting Started

1. **Explore Project Ideas**: Browse through the list of AVS project ideas in this repository. Each idea is detailed, providing a comprehensive overview to help you understand the potential and scope of the project.
2. **Select a Project**: Choose a project that aligns with your interests and skills. Each idea includes technical details, potential challenges, and a suggested implementation plan to guide you.

## Project Ideas

1. **AI Inference**
   - [AI Inference](ideas/ai-inference.md)
   - Summary: Implement AI inference onchain using EigenLayer to leverage its decentralized trust and economic mechanisms, ensuring program integrity, session privacy, and supporting federated learning.

2. **Inbound and Outbound Bridge**
   - [Inbound and Outbound Bridge](ideas/inbound-outbound-bridge.md)
   - Summary: Utilize a decentralized network of relay operators on EigenLayer to enhance the resilience and security of cross-chain bridges.

3. **Keeper Network**
   - [Keeper Network](ideas/keeper-network.md)
   - Summary: Deploy nodes to respond to 'if-this-then-that' demands for both non-time-sensitive and time-sensitive actions, leveraging Ethereum inclusion trust via EigenLayer.

4. **MEV Management**
   - [MEV Management](ideas/mev-management.md)
   - Summary: Introduce MEV-Boost+ and MEV-Boost++ to enable proposers to have both transaction inclusion power and MEV rewards, enhancing Ethereum’s liveness and censorship resistance.

5. **Relay Networks**
   - [Relay Networks](ideas/relay-networks.md)
   - Summary: Implement a decentralized network of relay operators on EigenLayer to support bridge operations and provide dApp developers with robust and flexible bridging solutions.

6. **Reorg Resistance**
   - [Reorg Resistance](ideas/reorg-resistance.md)
   - Summary: Develop a service to guarantee nodes with substantial stake in Ethereum attest to the block header of the most recently finalized block, ensuring resistance to chain reorganizations.

7. **Trusted Execution Environment (TEE) Committees**
   - [Trusted Execution Environment (TEE) Committees](ideas/tee-committes.md)
   - Summary: Construct decentralized TEE Committees through EigenLayer, enhancing the reliability of any committee by requiring multiple distinct TEE models and economic trust.

8. **Threshold Cryptography**
   - [Threshold Cryptography](ideas/threshold-cryptography.md)
   - Summary: Implement threshold cryptography using EigenLayer nodes to perform distributed computation on encrypted data, delivering robust privacy guarantees.

9. **Threshold Fully Homomorphic Encryption (FHE)**
   - [Threshold Fully Homomorphic Encryption (FHE)](ideas/threshold-fhe.md)
   - Summary: Enable distributed computation on encrypted data using EigenLayer nodes for threshold FHE, ensuring privacy and security while performing computations on sensitive data.

10. **Ceramic Node Operator AVS**
   - Summary: This project request is to build an AVS network of Ceramic Node operators for the Ceramic user community so that they can enhance decentralized trust in the service and enable rewards for operators and their stakers.
   - Ideas: Start with the existing [Ceramic node binary](https://developers.ceramic.network/docs/protocol/js-ceramic/nodes/running-a-node). Build an offchain daemon that integrates the nodes behaviors with. You may use the [pinception offchain daemon](https://github.com/wesfloyd/pinception/blob/main/operator/pinner-ipfsd.js) as an example.

11. **Decentralized HTTP Load Balancer Network**
   - Summary: many web3 services would like to make calls to a known set of available server endpoints for a variety of tasks. Currently there isn't a Web3 analogue to services such as the [Google Load Balancer](https://cloud.google.com/load-balancing/docs/application-load-balancer) or [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/) . This may also be used as a component in an alternative architecture for DNSs for future "consumer" web3 apps.
   - Ideas: implement a simple network of Operators that implement a basic proxy service (eg [node-http-proxy](https://github.com/http-party/node-http-proxy)) and forward those requests as needed per the service configuration. The list of Operator IP addresses can be registered and maintained on-chain when operators opt-in to the AVS, copying EigenDA's approach for its blob storing Operator instances. Clients invoking the service can simply read the state of the AVS contracts to get the list of available Operator endpoints and invoke them round-robin as needed to emulate the services of a global load balancer. 


## Sharing Updates

### Interested in Building?
If you decide to build one of the ideas from this repository:
- **Share Your Progress**: Head over to the [Discussions](https://github.com/avs-ideas/discussions) section to share your updates. Connect with like-minded community members, seek advice, and collaborate.

### Completed a Project?
If you successfully complete one of the projects:
- **Submit a Pull Request (PR)**: Post a PR to this repository. We will review your submission and, once approved, tag your hosted project next to the original idea. This will help others see your work and inspire further innovation.
- **Get Exposure**: Tweet out your completed project to @BuildOnEigen to gain more exposure and receive confirmation on proof of concept. This can help you connect with a wider audience and showcase your work to potential collaborators and investors.

## Contributing

We welcome contributions to this repository! Whether you have a new AVS project idea or improvements to an existing one, we encourage you to share them.

1. **Adding New Ideas**: Submit a pull request with a detailed proposal using our [Idea Proposal Template](./template.md).
2. **Improving Existing Ideas**: Suggest enhancements or modifications to existing ideas through pull requests or discussions.
3. **Feedback**: Provide feedback on existing ideas through issues or discussions.

## License

This repository is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## Contact

For any questions or further information, please reach out to the Eigen Labs team:

- **Twitter**: [Build On Eigen](https://twitter.com/BuildOnEigen)
- **GitHub**: [EigenLayer](https://github.com/Layr-Labs)
