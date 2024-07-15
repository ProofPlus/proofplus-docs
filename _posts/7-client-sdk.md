---
title: ProofPlus Client
author: Mihail Kirov
date: 2019-04-27
category: ProofPlus
layout: post
---

## ProofPlus Client SDK

An SDK module is implemented for the User that serves as a client to the protocol - `ProofPlusProver` - that:

- Initiates an on-chain request to the Orchestator network.
- listens for an event containing the `endpoint` of the server of the Prover tasked with the proof generation
- long-polls the prover for the ZKP response at the fetched `endpoint`
- verifies its received proof against the `proofHash` , as the Prover is also required to submit the task completion transaction to the Orchestration network

## Slashing

The SDK also serves as a Slasher. In case of mismatch of the locally computed proof hash and the one on-chain, or in case of liveness fault, the SDK calls the `slash` method, passing the whole proof, it’s local public inputs, the `taskId`, and the whole binary. If the proof with the public inputs (passed as calldata) verifies correctly on-chain and the binary, when hashed, don’t correspond to the `publicInputsHash` , then the Prover was mallicious and gets slashed.
