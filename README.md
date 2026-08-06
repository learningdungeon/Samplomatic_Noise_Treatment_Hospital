# Samplomatic Noise Treatment Hospital

An interactive educational game that teaches **Samplomatic** — Qiskit's framework for advanced quantum error mitigation on IBM Quantum hardware.

Built for the **WISER Education Challenge 2026**.

---

## Quick Start

1. Open `samplomatic_matcher.html` in any browser (Chrome, Firefox, Edge, Safari)
2. No installation, no server, no Python required
3. Click "Admit Next Patient" to start

---

## Target Audience

- Qiskit Global Summer School (QGSS) participants
- Quantum computing learners with basic Qiskit knowledge
- Anyone learning error mitigation on real quantum hardware

## Learning Objectives

By playing this game, learners will:

1. **Match noise types to Samplomatic annotations:**
   - `coherent` → Twirl
   - `unknown` → InjectNoise (Diagnostic Scan)
   - `readout` / `measurement` → ChangeBasis (Repositioning)
   - `multi-layer` / `deep` → NoiseLearnerV3 (Pathology Lab)
   - `utility-scale` → PNA (Treatment Plan)
   - `local` → SLC (Targeted Therapy)

2. **Recognize Samplomatic code patterns** — pick correct Python/Qiskit code snippets for each annotation

3. **Understand the full Samplomatic workflow:**
   - Boxing circuits → Twirling coherent noise → Learning noise profiles → Advanced mitigation (PNA/SLC)

4. **Connect theory to practice** — all content based on QGSS 2026 Lab 3

## Educational Methodology

**Metaphor-based learning** using a hospital emergency room:

| Hospital Concept | Samplomatic Concept |
|------------------|---------------------|
| Patient with symptoms | Noisy quantum gate |
| Diagnosis by symptom tags | Noise type identification |
| Treatment department | Samplomatic annotation |
| Recovery / Fidelity | Circuit quality after mitigation |

**Two progressive levels:**
- **Level 1 — Symptom Matching:** Match noise symptoms to treatment departments
- **Level 2 — Code Matching:** Identify correct Samplomatic code from jumbled options

**Gamification elements:**
- Score tracking with streak bonuses
- Immediate feedback with educational explanations
- Completion tracking across 12 patient scenarios
- Skip and reset options for self-paced learning

## Technologies Used

- HTML5
- CSS3 (custom animations, responsive grid layout)
- Vanilla JavaScript (no frameworks, zero dependencies)
- Runs entirely in the browser

## How to Play

### Level 1: Match Symptoms
1. A patient card appears with noise symptom tags
2. Click the patient to select it
3. Click the correct treatment department
4. Read the explanation that appears
5. Click "Next Patient" to continue

### Level 2: Match Code
1. Click "Switch to Code Level"
2. A patient appears with symptoms
3. Four jumbled code snippets appear — pick the correct one
4. Wrong answers highlight the correct code
5. Continue through all 12 patients

### Controls
- **Next Patient** — advance after answering
- **Skip** — skip current patient (counts as wrong)
- **Reset Game** — restart from zero
- **Switch Level** — toggle between symptom and code modes

## Future Improvements

1. **Multi-step treatment chains** — Level 3 where patients need sequenced treatments (Twirl → InjectNoise → PNA)
2. **Timed mode** — add time pressure for advanced learners
3. **Real QPU integration** — connect to IBM Quantum backends to show live noise data
4. **Leaderboard** — track scores across players
5. **PWA version** — package for offline mobile play
6. **Additional languages** — translate symptom tags and explanations
7. **SLC lightcone visualization** — interactive diagram showing which noise generators are pruned

## Credits

Built by **Noor Ul Ain Faisal**
- IBM Qiskit Advocate (2025)
- QGSS 2026 Mentor
- unitaryHACK 2026 Winner (Elliot the Electron)
- Friend of OQI, Open Quantum Institute at CERN (2026)
- Member, IEEE GRSS QUEST Technical Committee

Based on QGSS 2026 Lab 3: *"Your New Tool For Quantum Advantage"* — Samplomatic, NoiseLearnerV3, PNA, and SLC.

## License

MIT — free to use, modify, and distribute for educational purposes.
