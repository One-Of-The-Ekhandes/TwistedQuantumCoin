# Twisted Quantum Coin

[![CI](https://github.com/One-Of-The-Ekhandes/TwistedQuantumCoin/actions/workflows/ci.yml/badge.svg)](https://github.com/One-Of-The-Ekhandes/TwistedQuantumCoin/actions/workflows/ci.yml)

A follow-up to [Quantum Coin Flip](https://github.com/One-Of-The-Ekhandes/quantum-coin-flip): what happens if you "twist" the coin with an X (NOT) gate after putting it into superposition?

## The circuit

```text
|0⟩ ── H ── X ── measure
```

- **H (Hadamard)** turns |0⟩ into the equal superposition |+⟩ = (|0⟩ + |1⟩)/√2.
- **X** swaps |0⟩ and |1⟩. Applied to |+⟩ it gives (|1⟩ + |0⟩)/√2, which is the same state.
- So the twist does **not** change the odds: the result is still 0 or 1 with 50% probability each.

The script runs a single shot, so each run prints one random outcome, for example `{'1': 1}`. Change `shots=1` to `shots=1024` to see the 50/50 split.

The lesson: X only changes measurement odds when the qubit is not in an equal superposition. Try `ry(0.5, 0)` instead of `h(0)` to see X flip a biased coin.

## How to run

```bash
pip install -r requirements.txt
python TwistedQuantumCoin.py
```

## Author

Rujuta Ekhande
