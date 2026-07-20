# DOMAIN TOPOLOGY MAP
## Project: No Thing There — Qubit Physical Ontology

**Date:** 2026-07-20  
**Stage:** Phase 4, Stage 0 — Domain Assessment

---

## §1 Domain Architecture

The qubit ontology problem sits at the intersection of four domains, each with distinct research traditions:

```
                    ┌──────────────────────────────┐
                    │     QUANTUM FOUNDATIONS       │
                    │  (Rovelli, Fuchs, Zurek,      │
                    │   RQM, QBism, Decoherence)     │
                    └──────────┬───────────────────┘
                               │
           ┌───────────────────┼───────────────────┐
           │                   │                   │
           ▼                   ▼                   ▼
┌──────────────────┐ ┌──────────────────┐ ┌──────────────────┐
│  DEVICE PHYSICS   │ │   MEASUREMENT    │ │  COMPUTATIONAL   │
│  (Koch, Devoret,  │ │    THEORY        │ │   ARCHITECTURE   │
│   Martinis,        │ │  (Blume-Kohout,  │ │  (DiVincenzo,    │
│    Blais, Wallraff)│ │   GST, RB, QST)  │ │   Fowler, Nayak) │
└────────┬─────────┘ └────────┬─────────┘ └────────┬─────────┘
         │                    │                    │
         └────────────────────┼────────────────────┘
                              │
                              ▼
               ┌──────────────────────────┐
               │  QNFO CRITICAL SYNTHESIS  │
               │  (The Qubit Delusion,      │
               │   Beyond the Qubit,         │
               │   ZBW p-Adic Observable)    │
               └──────────────────────────┘
                              │
                              ▼
               ┌──────────────────────────┐
               │  THIS PROJECT:            │
               │  No Thing There —          │
               │  Pedagogical Bridge        │
               └──────────────────────────┘
```

## §2 Key Research Questions (Mapped from Source Note)

### RQ1: Ontology of the Qubit

**Question:** If a transmon qubit is the two lowest eigenstates of a nonlinear oscillator, and a spin qubit is the orientation of a single electron spin, what exactly *persists* between state preparations and measurements that warrants the label "qubit"?

**Domain:** Device Physics ∩ Quantum Foundations  
**Key tension:** Substance vs. stable transition rules

**Active paradigms:**
- **Device-physics view:** The qubit *is* the protected two-level subspace, operationally identified by spectroscopy
- **Philosopher's view:** The qubit is a relational property — defined by its Hamiltonian symmetries, not by any "thing"
- **QNFO view:** The qubit is a scaffold, not an invariant; the invariant is the correlation structure

### RQ2: Physical Interpretation of Control

**Question:** When we apply a calibrated microwave pulse to a transmon, are we "rotating a state vector" in a pre-existing Hilbert space, or are we actively shaping the modal occupation numbers and coherences of the underlying superconducting circuit?

**Domain:** Device Physics ∩ Computational Architecture  
**Key tension:** Mathematical abstraction vs. physical process

**Active paradigms:**
- **Circuit QED view:** Control pulses couple to the dipole moment of the plasmon mode; the rotating-frame Bloch sphere is a convenient picture but the underlying physics is mode excitation
- **Gate-model abstraction:** Control pulses implement unitary operations on abstract qubit states — the physical mechanism is irrelevant so long as fidelities are high
- **QNFO view:** The "gate" is a scaffold; what matters is correlation manipulation, not discrete operations

### RQ3: The Amplifier as a Measurement Anvil

**Question:** Where in the amplification chain does the projection actually occur? Is the qubit measured when the probe tone exits the resonator, or only after the signal is irreversibly amplified?

**Domain:** Device Physics ∩ Measurement Theory  
**Key tension:** The "Heisenberg cut" — where does quantum become classical?

**Active paradigms:**
- **Operational view (mainstream):** The projection happens at the first stage of amplification where the signal becomes irreversible (JPA → HEMT). The exact location of the cut is a philosophical question with no operational consequence.
- **Decoherence view:** The measurement is complete when the qubit's state information is irreversibly transferred to the environment — this can be modeled as a continuous process.
- **Self-referential view (this project's angle):** The cut's location matters because calibration circularity means we never independently verify where projection happens.

### RQ4: Self-Referential Tomography and Calibration Bootstrapping

**Question:** Can we break the circularity of gate set tomography by introducing operationally independent verification of measurement operators through energy-level spectroscopy of the bare multi-level system?

**Domain:** Measurement Theory ∩ Quantum Foundations  
**Key tension:** All calibration is circular — is there an anchor?

**Active paradigms:**
- **Gate Set Tomography (GST):** Self-consistency is a feature, not a bug. GST jointly estimates gates and measurements without needing pre-calibrated references.
- **Randomized Benchmarking (RB):** Provides a partially independent check by measuring average gate fidelity through sequence-length scaling.
- **Spectroscopic anchoring:** Multi-level spectroscopy (measuring |1⟩↔|2⟩ transition frequencies, anharmonicity) is an independent measurement of the bare Hamiltonian — it anchors the computational subspace in a larger Hilbert space.

### RQ5: Relational Metrology and Logical Abstraction

**Question:** If each physical qubit is already a relational construct, is a logical qubit a "relation of relations"?

**Domain:** Computational Architecture ∩ Quantum Foundations  
**Key tension:** How many layers of relational abstraction before the whole stack becomes unmoored?

**Active paradigms:**
- **Standard QEC view:** Logical qubits are protected subspaces of the multi-qubit Hilbert space — they are as "real" as physical qubits, just more robust.
- **Relational QM view:** Logical qubits are relational properties at a higher level of abstraction — no loss of grounding because grounding was relational at all levels.
- **QNFO view:** The "relation of relations" framing is the correct one; the question is whether this layered self-reference introduces fragility or robustness.

---

## §3 Domain Intersection Matrix

| Intersection | RQ | Key Papers | Consensus Level |
|-------------|-----|-----------|----------------|
| Device Physics × Foundations | RQ1 | Koch 2007, Rovelli 1996, Qubit Delusion | **Low** — active disagreement on ontology |
| Device Physics × Architecture | RQ2 | Blais 2004, Wallraff 2004, Beyond the Qubit | **Medium** — agreed on mechanism, disagree on interpretation |
| Device Physics × Measurement | RQ3 | Blume-Kohout 2013, Zurek 2003 | **Medium** — operational consensus, interpretive divergence |
| Measurement × Foundations | RQ4 | GST, RB, Merkel 2013, Kochen-Specker 1967 | **Low** — circularity acknowledged but severity debated |
| Architecture × Foundations | RQ5 | Fowler 2012, Rovelli 1996, Adelic QEC | **Low** — "relation of relations" is a novel framing |

---

## §4 Methodological Approaches by Domain

| Domain | Primary Method | Strength | Weakness |
|--------|---------------|----------|----------|
| Device Physics | Hamiltonian engineering + spectroscopy | Direct experimental access | Cannot escape operational definitions |
| Measurement Theory | GST, RB, process tomography | Self-consistent error models | Inherently circular calibration |
| Quantum Foundations | Conceptual analysis, no-go theorems | Identifies hidden assumptions | Often disconnected from experimental practice |
| Computational Architecture | Error models, threshold theorems | Engineering-relevant | Assumes qubit abstraction works |
| QNFO Synthesis | Deconstruction Spiral v4.0, scaffold-invariant analysis | Identifies map-territory confusions | Can overstate the practical import of ontological problems |

---

## §5 Synthesis: The Central Tension

The qubit ontology problem reveals a **fundamental tension between two operational stances**:

1. **The device physicist's stance:** "I know what a qubit is — it's the two-level subspace I see in spectroscopy. I manipulate it with pulses calibrated by Ramsey/Rabi. I read it out via dispersive shift. Tomography is self-consistent calibration, not a circularity problem. The system works."

2. **The foundational critic's stance:** "You've assumed the computational subspace exists before you 'see' it in spectroscopy. Your calibration uses the very measurements it calibrates. Your readout collapses a state whose pre-measurement existence you can only infer circularly. The system 'works' only within its own self-consistent bubble."

**The synthesis (this project's contribution):** Both are correct, but at different levels. The device physicist is operationally right: the qubit is a real, stable, engineerable subsystem of a larger physical system, anchored by multi-level spectroscopy that operates on the bare Hamiltonian before the qubit subspace restriction is imposed. The foundational critic is epistemically right: we cannot escape the circularity entirely — but the circle has an anchor, and that anchor is the bare multi-level Hamiltonian verified by spectroscopy that does NOT depend on the qubit abstraction. This is the key insight missing from both the QNFO critique and the mainstream defense.

---

## §6 Next Steps

1. **Assumption Audit** (Stage 2): For each RQ, enumerate enabling and blocking assumptions
2. **Calibration Register** (Stage 5): Dated predictions about self-referential metrology resolution
3. **Strategic Memo** (Stage 7): Synthesize into paper-ready argument
