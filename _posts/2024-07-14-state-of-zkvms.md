---
title: State of zkVMs
author: Mihail Kirov
date: 2019-04-27
category: ProofPlus
layout: post
---

# Current State of zkVMs

Recently, user-friendly zero-knowledge virtual machines (zkVMs) like SP1 and Risc Zero have emerged, streamlining the integration of zero-knowledge proofs into various platforms. These zkVMs simplify the development process, enabling developers to leverage advanced cryptography without extensive expertise, thus broadening the adoption of secure, privacy-preserving technologies across industries.

# Challenges zkVM projects are facing

Zero-knowledge virtual machines (zkVMs) face challenges, particularly with the slow generation of Groth16 proofs. While these proofs are efficient for verification, their creation can be computationally intensive. For instance, generating a proof to validate a single BLS signature can take over eight hours on a high-end GPU virtual machine. An in-depth report of the benchmarks and findings for local and remote proof generation using Risc Zero can be found [here](https://www.notion.so/Hedera-State-Consensus-ZK-PoC-Findings-f86d92f22f684f3c8ba26dd182eaf122?pvs=21).

In addition to proof generation time, current zkVM provers face centralization challenges. Relying on a single entity to provide valid proofs is suboptimal, as it introduces the risk of censorship and control over request processing. Decentralizing the proof generation process is crucial to ensuring transparency and resilience, allowing for a more secure and trustworthy blockchain ecosystem where no single point of failure or control exists.