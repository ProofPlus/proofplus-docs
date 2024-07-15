---
title: Flow
author: Mihail Kirov
date: 2019-04-27
category: ProofPlus
layout: post
---

1. The user requests proof generation from the On-chain protocol using an SDK.
2. The user listens for a specific event from the Orchestrator network to get the server URL of the assigned prover.
3. The user requests a Zero-Knowledge Proof (ZKP) from the prover.
3. The prover generates the ZKP and simultaneously:
- Submits the task result to the Orchestrator network.
- Returns the ZKP to the user.
4. The user listens for a task completion event from the Orchestrator network, then validates the received proof and data against those on-chain.
If there is a mismatch or a liveness fault, the user triggers a slashing method.


![ProofPlus Flow](interaction-diagram.png)