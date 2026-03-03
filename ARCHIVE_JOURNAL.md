# Calyx Project Archive (THOR/Synapse Era)

This document contains the historical session logs from the initial development of the project under the working titles "Project THOR" and "Synapse."

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
