# Calyx Project Archive (THOR/Synapse/Calyx Era)

This document contains the historical session logs and reconstructed summaries from the development of Calyx.

---

### [2026-02-24 to 2026-02-27] - Sessions 10-17: The Bridge & Sharding Epoch (RECONSTRUCTED)
*Note: These entries were reconstructed after a synchronization gap. They represent the core technical milestones achieved during the transition from Synapse to Calyx.*

- **The Naming Pivot:** Officially transitioned from "Project THOR" to "Calyx."
- **Neural Sharding Alpha:** Developed the `shard_manager.py` to handle the splitting of `.pt` weight files across nodes.
- **The Mailroom Protocol:** Created the first version of the file-based "Postal Service" for nodes to communicate intent without a persistent socket connection.
- **DAP (Distributed Authority Protocol):** Established the first rules for machine-file ownership to prevent Git merge conflicts between the PC and Laptop.
- **Mesh Topology:** Implemented the `mesh_discovery/` directory system, allowing nodes to broadcast their existence via JSON heartbeats.
- **Inference Hardening:** Successfully executed a 3-hop "Virtual Spike" across PC, Laptop, and a mock Mobile node.

---

### [2026-02-23] - Session 9: Reward Validation & High-Frequency Benchmarking
- **Reward Integrity Secured:** Implemented `reward_validator.py`. The node can now verify Ed25519 signatures on every spike.
- **Stress-Test Ready:** Developed `high_throughput_probe.py` to fire 100+ signed spikes per second.

---

### [2026-02-23] - Session 8: Physical LAN Bridge Verified
- **Physical Handshake SUCCESS:** Verified end-to-end physical connection between Laptop and PC using Raw TCP.
- **Firewall Solved:** Explicitly opened ports 60001 and 60005 on the PC.

---

### [2026-02-23] - Session 7: Physical LAN Mesh Success
- **Physical LAN Mesh Verified:** Successfully linked PC and Laptop via LAN IP.
- **Hybrid Discovery Success:** Verified file-based fallback logic.

---

### [2026-02-22] - Session 1: The Virtual Pivot & Environment Setup
- **Environment Setup:** Installed `torch`, `snntorch`, `libp2p`, and `trio`.
- **Logic Pillars:** Created 20+ core modules including the LIF neuron model, MessagePack binary optimization, Ensemble Consensus, and Solarpunk mobile mockup.
- **Security:** Implemented Ed25519 node identities and zkML proof mocks.

---
*Archived for historical reference by The Architect.*
