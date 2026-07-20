# PROJECT-PLAN: No Thing There

**Project:** Control, Readout, and Self-Referential Metrology in Engineered Quantum Systems
**Slug:** `no-thing-there`
**Status:** Phase 0 — Initiated 2026-07-20
**Branch:** `feature/phase0-init`

---

## §1 Charter

### 1.1 Purpose

This project produces a **pedagogical synthesis paper** that bridges the ontological critique of qubit-as-particle (advanced by QNFO's "The Qubit Delusion" and "Beyond the Qubit") to the actual working physics of engineered qubit platforms. It answers, in accessible yet rigorous terms:

> If no quantum engineer actually believes a qubit is a billiard-ball "particle," then what are control pulses actually manipulating, and what is actually read out?

### 1.2 Core Claim (LOCKED)

**C1:** The qubit-gate-circuit model's pedagogical framing as "particles we poke with gates" is a map-territory confusion — but the working physics of engineered qubits has always been relational and mode-based. Control pulses manipulate the field quadratures of a constrained two-level subsystem of a collective excitation mode (plasmon mode, spin state, electronic transition). Readout is a macroscopic projective map through a calibrated transducer chain. Self-referential metrology (tomography) is genuinely circular but anchored by the physical reality of the engineered system's multi-level spectroscopy. Recognizing this relational character does not invalidate existing platforms but clarifies what error correction thresholds and logical-qubit benchmarks actually measure.

**Falsifiability condition:** C1 would be disconfirmed if (a) a qubit's computational subspace cannot be identified with specific eigenstates of a multi-level physical Hamiltonian verified by independent spectroscopy, or (b) gate set tomography fails to self-consistently converge on physically plausible error models across multiple independent calibration runs.

## §2 Phases and WBS

| Phase | Deliverables | Gate Criteria |
|-------|-------------|---------------|
| **0 — Init** | Repo, scaffold, PROJECT-PLAN, README, .gitignore, core claim lock | P1-P8 HARD gates passed |
| **1 — Due Diligence** | QNFO cross-reference report, gap analysis, novelty assessment | KG + D1 + Vectorize + 2 external sources queried |
| **2 — Literature** | Classified bibliography (core/supporting/background), dedup report | ≥5 core, ≥10 supporting, ≥5 background |
| **3 — Deep Research** | Domain topology map, domain assessment, assumption audit, calibration register | All 5 adversary challenges passed |
| **4 — Synthesis Paper** | `paper.md` with full argument, BibTeX, YAML frontmatter | Publication Language Gate passed, rubric ≥4.0 |
| **5 — Publication** | PDF (Pandoc+XeLaTeX), Zenodo DOI, D1 insert, papers-server deploy | DOI resolves, D1 record live |
| **6 — Dissemination** | Buffer social posts, IPFS pin, DNSLink, 4-D verification | All 4 dimensions verified |

## §3 Milestones

| Milestone | Date | Tag |
|-----------|------|-----|
| Phase 0 complete | 2026-07-20 | `v0.1-phase0` |
| Due Diligence complete | 2026-07-20 | `v0.2-phase1-dd` |
| Literature Search complete | 2026-07-20 | `v0.3-phase2-lit` |
| Deep Research complete | 2026-07-21 | `v0.5-phase4-deep` |
| Paper published | 2026-07-22 | `v1.0` |

## §4 Deliverable Registry

| ID | Deliverable | Path | Archival Target |
|----|-------------|------|----------------|
| D0 | Source note (Obsidian) | `docs/_26201090032-source.md` | R2, GitHub |
| D1 | Due Diligence Report | `artifacts/due-diligence-report.md` | R2, GitHub |
| D2 | Literature Bibliography | `artifacts/bibliography.md` | R2, GitHub |
| D3 | Domain Topology Map | `artifacts/domain-topology.md` | R2, GitHub |
| D4 | Assumption Audit | `artifacts/assumption-audit.md` | R2, GitHub |
| D5 | Calibration Register | `artifacts/calibration-register.md` | R2, GitHub |
| D6 | Synthesis Paper | `paper.md` | R2, Zenodo, D1, IPFS |
| D7 | Paper PDF | `paper.pdf` | R2, Zenodo, IPFS |
| D8 | BibTeX | `refs.bib` | R2, GitHub |

## §5 Risk Register

| ID | Risk | Likelihood | Impact | Mitigation |
|----|------|-----------|--------|------------|
| R1 | Overlap with existing QNFO papers renders synthesis redundant | Medium | High | Gap analysis (§2) must identify unique contribution before Phase 4 |
| R2 | Self-referential metrology argument is too philosophical for physics audience | Medium | Medium | Ground in concrete platform examples (transmon spectroscopy, gate set tomography) |
| R3 | External literature returns insufficient core papers on qubit ontology | Low | Medium | Broaden search to include measurement theory, quantum foundations |
| R4 | Pandoc/XeLaTeX not available on Windows for PDF build | Medium | Low | Fallback: install MiKTeX; verify early |
| R5 | Zenodo API rate-limit or 500 during publication | Low | Low | Retry protocol (3x exponential backoff) |

## §6 Success Criteria

1. Paper passes Publication Language Gate (zero internal language hits)
2. Self-evaluation rubric score ≥ 4.0 average, all dimensions ≥ 3
3. Zenodo DOI resolves and cross-references prior QNFO papers
4. D1 living-paper record live at papers.qnfo.org
5. 4-D distribution complete (Distributed, Durable, Discoverable, Duplicated)

## §7 Version History

| Version | Date | Description |
|---------|------|-------------|
| v0.1-phase0 | 2026-07-20 | Project initialization, scaffold, core claim lock |
