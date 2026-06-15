# JUNIX
Deterministic unit-manifold tensors with cryptographic policy enforcement

# JUNIX

**Deterministic Unit-Manifold Tensors with Cryptographic Policy Enforcement**

JUNIX is a mathematically sovereign tensor engine where invalid floating-point drift does not silently continue. Every tensor operation is guarded by a unit-manifold invariant, and every critical state can be cryptographically locked via the TUNE layer.

## Core Invariant

For every vector `v` in a PhaseTensor: `||v|| = 1.0` within tolerance. If drift exceeds budget, the operation is rejected.

## Quick Start

```bash
# Rust
cargo test

# Python
maturin develop --features python
python -c "import junix; print(junix.PyPhaseTensor.from_angles([0.1,0.2], [2]).lock_state())"
