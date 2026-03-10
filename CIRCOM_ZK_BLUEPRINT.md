# INGRVM ZK-Inference: Circom Blueprint (1-bit Math)
**Objective:** Prove the result of an XNOR-Popcount operation for Binary Neural Networks (BNNs).

## 1. The Circuit Constraint (Logic)
In a 1-bit linear layer, the activation $y$ is:
$$y = \text{popcount}(\text{XNOR}(\text{weights}, \text{inputs}))$$

To prove this in Circom (over a prime field), we must map bits to field elements {0, 1}.

### Arithmetic Mapping:
- **XNOR(a, b)** becomes: `1 - a - b + 2*a*b`
- **Popcount** becomes: `Σ(bits[i])`

## 2. Circom Implementation Sketch
```circom
pragma circom 2.0.0;

template BinaryLinear(N) {
    signal input in[N];
    signal input weights[N];
    signal output out;

    signal xnors[N];
    var sum = 0;

    for (var i = 0; i < N; i++) {
        // Enforce binary inputs
        in[i] * (in[i] - 1) === 0;
        weights[i] * (weights[i] - 1) === 0;

        // XNOR Logic: 1 if match, 0 if different
        xnors[i] <== 1 - in[i] - weights[i] + 2*in[i]*weights[i];
        sum += xnors[i];
    }

    out <== sum;
}

component main = BinaryLinear(1024);
```

## 3. Optimization Strategy
- **Batching:** Instead of proving one neuron at a time, we use a Merkle Root of the weights as a public input.
- **Commitments:** The Edge node provides a `poseidon` hash of its local weights. The Hub verifies that this hash matches the registered `ingrvm` CID in the marketplace.

## 4. Next Steps for PC Master
1.  [ ] Install `snarkjs` and `circom` on the desktop for circuit compilation.
2.  [ ] Develop the `circuit_verifier.py` to check these proofs during Swarm Auctions.
