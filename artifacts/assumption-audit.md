# ASSUMPTION AUDIT
## Project: No Thing There — Qubit Physical Ontology

**Date:** 2026-07-20  
**Stage:** Phase 4, Stage 2 — Assumption Audit

---

## §1 Enabling Assumptions Table

For each of the 5 Research Questions from the Domain Topology Map, we enumerate all enabling assumptions with confidence ratings (0-1).

### RQ1: Ontology of the Qubit — What persists?

| # | Assumption | Confidence | Fragility | Justification |
|---|-----------|-----------|-----------|---------------|
| A1.1 | Multi-level spectroscopy measures the bare Hamiltonian eigenstates before the qubit subspace restriction | 0.90 | LOW | Standard procedure: anharmonicity measurement confirms |0⟩↔|1⟩↔|2⟩ spacing; done before any qubit operations |
| A1.2 | The two-level subspace is well-isolated from higher levels (anharmonicity ≫ linewidth) | 0.85 | LOW | Transmon EJ/EC ~ 50-100 gives ~5% anharmonicity; sufficient for sub-μs gates |
| A1.3 | The computational subspace is operationally stable across many gate operations | 0.80 | MEDIUM | Leakage to |2⟩ is measurable and modeled; not zero but bounded |
| A1.4 | "Qubit" as a label refers to the two-level subspace, not to any substance or particle | 0.95 | LOW | Semantic — but the whole debate hinges on this assumption being explicit |
| A1.5 | The same physical system presents the same two-level subspace across different calibration runs | 0.90 | LOW | Temporal drift exists but is slow and calibratable; charge noise in transmon is suppressed by EJ/EC |

### RQ2: Physical Interpretation of Control

| # | Assumption | Confidence | Fragility | Justification |
|---|-----------|-----------|-----------|---------------|
| A2.1 | Microwave pulses couple linearly to the qubit's dipole moment | 0.95 | LOW | Established by circuit QED theory (Blais 2004, Wallraff 2004) and verified by Rabi chevron patterns |
| A2.2 | The rotating wave approximation (RWA) is valid for typical pulse parameters | 0.90 | LOW | ωq ~ 5 GHz, Ω ~ 10-100 MHz, RWA error ~ (Ω/ωq)² ~ 10⁻⁴ |
| A2.3 | The "state vector rotation" picture and the "mode excitation" picture are equivalent | 0.85 | MEDIUM | Mathematically equivalent within the two-level subspace; differ only when higher levels are involved |
| A2.4 | Gate operations can be modeled as unitary without tracking the underlying mode dynamics | 0.80 | MEDIUM | Valid when leakage is negligible; breaks down for fast gates (DRAG pulses needed) |
| A2.5 | Two-qubit gates mediated by a bus resonator can be described as state transfers without tracking the bus mode occupation | 0.75 | HIGH | Virtual excitation in the bus means the bus is never "really" excited — but only if detuning is large compared to coupling |

### RQ3: The Amplifier as Measurement Anvil

| # | Assumption | Confidence | Fragility | Justification |
|---|-----------|-----------|-----------|---------------|
| A3.1 | The projection (wavefunction collapse) occurs at the first irreversible amplification stage | 0.70 | HIGH | No experimental test of WHERE collapse happens; operational definition only |
| A3.2 | The JPA adds negligible noise beyond the quantum limit | 0.85 | MEDIUM | Near-quantum-limited amplification demonstrated; but added noise is not zero |
| A3.3 | The dispersive readout does not disturb the qubit state before the probe tone exits the resonator | 0.80 | MEDIUM | Measurement-induced dephasing depends on χ/κ ratio; non-QND for certain parameter regimes |
| A3.4 | The "Heisenberg cut" location has no operational consequence for gate fidelities | 0.65 | HIGH | Core of the self-referential metrology debate: if the cut location matters for calibration circularity, this assumption is false |
| A3.5 | The readout outcome reliably indicates the pre-measurement qubit state (with known fidelity) | 0.85 | MEDIUM | Readout fidelity 98-99% demonstrated; but state assignment errors correlate with qubit relaxation during measurement |

### RQ4: Self-Referential Tomography

| # | Assumption | Confidence | Fragility | Justification |
|---|-----------|-----------|-----------|---------------|
| A4.1 | Gate Set Tomography converges to a self-consistent error model that corresponds to physical reality | 0.75 | HIGH | GST guarantees internal consistency, not external accuracy. Gauge freedom in the estimates. |
| A4.2 | Randomized Benchmarking is operationally independent of GST | 0.80 | MEDIUM | RB and GST probe different aspects; but both rely on the same physical control and readout apparatus |
| A4.3 | Multi-level spectroscopy provides an independent anchor for the computational subspace | 0.85 | MEDIUM | Spectroscopy of bare Hamiltonian does not require qubit operations — but still uses the same readout chain |
| A4.4 | Calibration circularity is not a practical problem below error rates of 10⁻⁴ | 0.70 | HIGH | Unknown: has not been tested at the 10⁻¹⁰ threshold needed for fault-tolerant logical qubits |
| A4.5 | The gauge freedom in GST is irrelevant to error correction thresholds | 0.65 | HIGH | Gauge transformations change which errors are assigned to which gates — this matters for decoder design |

### RQ5: Relational Metrology and Logical Abstraction

| # | Assumption | Confidence | Fragility | Justification |
|---|-----------|-----------|-----------|---------------|
| A5.1 | A logical qubit in a surface code is a stable topological property of the code space | 0.90 | LOW | Mathematically proven; the question is physical implementation, not theoretical existence |
| A5.2 | The "relation of relations" framing is a category error — logical qubits are mathematical, not physical | 0.60 | HIGH | Debate hinges on what "physical" means. If physical = relational, then layered relations are still physical. |
| A5.3 | Error correction thresholds are robust to calibration errors in the underlying physical gates | 0.70 | HIGH | Threshold theorem assumes independent Pauli errors; calibration errors may be correlated |
| A5.4 | The surface code decoder can operate with noisy syndrome measurements | 0.85 | MEDIUM | Yes in theory; practical decoder latency vs. physical error rate tradeoff is tight |
| A5.5 | Logical qubit fidelity can be verified without circularity | 0.65 | HIGH | How do you verify a logical qubit's fidelity when the verification itself uses physical qubits whose calibration is circular? |

---

## §2 Blocking Assumptions

These are assumptions that must be TRUE for the current paradigm to work. If any of these are false, the paradigm breaks.

| # | Blocking Assumption | Would Be Disconfirmed By | Severity if False |
|---|-------------------|--------------------------|-------------------|
| B1 | Multi-level spectroscopy anchors the computational subspace in a larger, independently verifiable Hilbert space | Demonstration that spectroscopy itself depends on qubit-calibrated measurements | **CRITICAL** — removes the only anchor for the calibration circle |
| B2 | The two-level subspace is sufficiently isolated from higher levels that leakage is correctable | Leakage rates that scale with gate count beyond QEC correction threshold | **HIGH** — current QEC codes do not efficiently correct leakage |
| B3 | Gate set tomography's gauge freedom does not mask correlated errors at the 10⁻¹⁰ level | Evidence that GST-estimated error models diverge from true errors at low rates | **HIGH** — defeats fault tolerance |
| B4 | Readout fidelity can be independently characterized (e.g., by state preparation and measurement error rates from Rabi/Ramsey) | Demonstration that all readout characterization is circular in a way that grows with system size | **CRITICAL** — no verifiable computation |
| B5 | The relational view (qubits as relational constructs) is consistent with the threshold theorem for fault-tolerant QEC | A no-go theorem showing that relational qubits cannot achieve threshold because calibration circularity introduces systematic errors | **HIGH** — undermines fault tolerance scaling claims |

---

## §3 Dependency Chain

```
Bare Hamiltonian spectroscopy (A1.1, A4.3)
    │
    ├──► Qubit subspace isolation (A1.2, B2)
    │       │
    │       ├──► Control pulse calibration (A2.1-A2.4)
    │       │       │
    │       │       ├──► Gate operations (RQ2)
    │       │       │       │
    │       │       │       └──► GST/RB calibration (A4.1, A4.2)
    │       │       │               │
    │       │       │               └──► Error models for QEC (A5.3)
    │       │       │                       │
    │       │       │                       └──► Logical qubit verification (A5.5)
    │       │       │
    │       │       └──► Two-qubit gates via bus (A2.5)
    │       │
    │       └──► Readout calibration (A3.1-A3.5)
    │               │
    │               └──► Measurement fidelity characterization (B4)
    │
    └──► Calibration anchor for the entire stack
```

**Key insight:** The entire quantum computing stack depends on the assumption that bare Hamiltonian spectroscopy (A1.1, A4.3) provides an independent anchor. If spectroscopy is itself circularly dependent on qubit-calibrated measurements, the entire stack loses its mooring. The question is NOT whether spectroscopy is independent — it almost certainly is, since it probes energy level differences of a multi-level system without restricting to the two-level subspace. The question is whether residual circularity in the readout chain (same amplifiers, same digitizers) introduces subtle correlations at the 10⁻¹⁰ level that current calibration methods cannot detect.

---

## §4 Fragility Heatmap

| Assumption | Confidence | Fragility | Risk Level |
|-----------|-----------|-----------|------------|
| A1.1 (Spectroscopy anchor) | 0.90 | LOW | 🟢 SAFE |
| A1.2 (Subspace isolation) | 0.85 | LOW | 🟢 SAFE |
| A2.1 (Linear dipole coupling) | 0.95 | LOW | 🟢 SAFE |
| A2.5 (Bus virtual excitation) | 0.75 | HIGH | 🟡 MONITOR |
| A3.1 (Projection location) | 0.70 | HIGH | 🟡 MONITOR |
| A3.4 (Heisenberg cut irrelevant) | 0.65 | HIGH | 🔴 RISK |
| A4.1 (GST corresponds to reality) | 0.75 | HIGH | 🟡 MONITOR |
| A4.4 (Circularity not a problem) | 0.70 | HIGH | 🔴 RISK |
| A4.5 (Gauge freedom irrelevant) | 0.65 | HIGH | 🔴 RISK |
| A5.2 (Category error debate) | 0.60 | HIGH | 🔴 RISK |
| A5.5 (Logical qubit verification) | 0.65 | HIGH | 🔴 RISK |

**Summary:** 4 HIGH-RISK assumptions, 3 MODERATE, 4 SAFE. The HIGH-RISK assumptions cluster around calibration circularity and the validity of extrapolating error models to the fault-tolerance regime.
