---
title: Introduction
author: Mihail Kirov
date: 2019-04-27
category: ProofPlus
layout: post
---

Zero-knowledge technology significantly enhances blockchain by providing privacy, scalability, and efficiency. It allows transactions to be verified without revealing sensitive information, ensuring user confidentiality while maintaining trust. This is particularly valuable in financial and identity-related applications, where privacy is crucial. Additionally, zero-knowledge proofs can improve scalability by reducing the amount of data processed on-chain, leading to lower operating costs. By enabling secure and private interactions, zero-knowledge technology fosters greater adoption of blockchain across various sectors, promoting a more secure and efficient decentralized ecosystem.

Groth16 proofs, known for their succinctness, allow complex computations to be verified with minimal calldata, reducing on-chain processing and transaction costs. Compared to executing the same logic in the Ethereum Virtual Machine (EVM), these proofs offer a more cost-effective solution in terms of on-chain gas. Currently, a Groth16 proof verification on-chain costs about a constant ~280k gas without regard to the size and complexity of the underlying logic that is being proven.