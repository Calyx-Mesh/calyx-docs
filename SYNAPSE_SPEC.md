# Calyx Synapse Specification (v1.0)

## Overview
In the Calyx ecosystem, a **Synapse** is a discrete unit of intelligence. It is a bundle of SNN (Spiking Neural Network) weights, metadata, and execution logic that allows a node to perform "Useful Work."

## 1. Synapse Categories

### Type A: Atomic Synapses (Micro-Intelligence)
- **Scale:** Small (1MB - 50MB)
- **Function:** Complete inference for specialized tasks.
- **Examples:** Voice Activity Detection, Keyword Spotting, Sentiment Analysis.
- **Reward:** High frequency, low payout per spike.

### Type B: Neural Shards (Pipeline Intelligence)
- **Scale:** Large (100MB - 4GB)
- **Function:** A partial slice of a Massive Language Model (80B+).
- **Architecture:** Nodes cooperate in a "Pipeline" to pass spikes from Layer N to Layer N+1.
- **Reward:** High payout per spike, requires high uptime and low latency.

### Type C: Reflex Bridges (Hardware Intelligence)
- **Scale:** Variable
- **Function:** Bridges physical hardware (Home sensors, Cameras, Mics) to the mesh.
- **Reward:** Subsidized by the user requesting the data.

## 2. The Lifecycle of a Synapse

1.  **Synthesis (Building):** A developer uses the `new_synapse.py` tool to scaffold the model.
2.  **Incubation (Training):** The model is trained (usually on a Tier II PC like your 1080 Ti).
3.  **Packaging:** The weights and manifest are bundled into a `.calyx` file.
4.  **Registration:** The Synapse is added to the Global Registry.
5.  **Activation (Mining):** Node owners download the `.calyx` bundle.
6.  **Firing (Incentive):** When the network routes a spike through that node's synapse, the owner earns $SYN tokens.

## 3. Reward Formula (Proof of Useful Work)
A node earns tokens based on:
- **Throughput:** How many spikes were processed.
- **Precision:** How accurate the result was (verified by the Ensemble).
- **Stakes:** How much $SYN the node has already bonded to that synapse.

---
*Drafted by The Architect | Calyx Core*
