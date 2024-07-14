---
title: Prover
author: Mihail Kirov
date: 2019-04-27
category: ProofPlus
layout: post
---

## Prover SDK
A lightweight SDK, on-chain listener and server are implemented to aid the prover:
-  ProverServer - that exposes a POST endpoint `/proof`, allowing the User to pass all constituents necessary for proof generation - the ELF binary and the private inputs. 
- An on-chain listener that fetches the proof generation request metadata and verifies correctness of the downloaded binary and inputs against the hashes. 
- It then starts the proof generation process locally. Upon successful proof generation, it returns the proof back to the requester off-chain. It also submits a task submission response to the on-chain protocol with the `taskId , proofHash and binaryHash`.