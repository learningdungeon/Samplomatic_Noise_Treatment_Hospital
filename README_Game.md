# 🏥 Samplomatic Emergency Room

**An interactive educational game that teaches Samplomatic — Qiskit's framework for advanced quantum error mitigation — through a hospital emergency room metaphor.**

Built for the **WISER Education Challenge 2026**.

---

## 🎮 Quick Start

1. Download `samplomatic_er.html`
2. Double-click to open in any browser (Chrome, Firefox, Edge, Safari)
3. No installation, no server, no Python required
4. Start treating patients immediately

---

## 👥 Target Audience

- Qiskit Global Summer School (QGSS) participants
- Quantum computing learners with basic Qiskit knowledge
- Anyone learning quantum error mitigation on IBM Quantum hardware
- Students who want to understand Samplomatic without access to a real backend

---

## 🎯 Learning Objectives

By playing this game, learners will master three core Samplomatic skills:

### Ward 1 — Diagnosis (Symptom → Annotation)
- Match noise types to the correct Samplomatic treatment
- `coherent` / `drift` → **Twirl** — converts coherent noise to stochastic Pauli channels
- `unknown` / `crosstalk` → **InjectNoise** — declares slots for NoiseLearnerV3
- `readout` / `measurement` → **ChangeBasis** — rotates measurement basis
- `multi-layer` / `deep` → **NoiseLearnerV3** — full Pauli-Lindblad characterization
- `utility-scale` → **PNA** — rewrites observable instead of circuit
- `local` / `lightcone` → **SLC** — prunes noise outside observable lightcone

### Ward 2 — Prescriptions (Annotation → Code)
- Identify correct Python/Qiskit code snippets for each Samplomatic annotation
- Recognize `generate_boxing_pass_manager()` options
- Understand `inject_noise_strategy` values (`no_modification`, `uniform_modification`, `individual_modification`)
- Read `NoiseLearnerV3`, `Executor`, `build()`, and `samplex` code patterns

### Ward 3 — Lab Compatibility (Hardware Awareness)
- Know which backend family Samplomatic requires (**Heron devices**)
- Understand basis gates: `cz, id, rz, sx, x`
- Learn that noise models are **device-specific** — switching backends invalidates them
- Know that simulators **cannot** be used for NoiseLearnerV3
- Know device specs: ibm_marrakesh = 156 qubits (Heron r2)

---

## 🏥 Educational Methodology

### Metaphor-Based Learning

The game uses a hospital emergency room where quantum computing concepts map to medical scenarios:

| Hospital Concept | Samplomatic Concept |
|------------------|---------------------|
| Patient arriving at ER | Noisy quantum gate entering a circuit |
| Patient symptoms (tags) | Noise type (coherent, unknown, readout, etc.) |
| Treatment department | Samplomatic annotation (Twirl, InjectNoise, ChangeBasis, etc.) |
| Prescription | Python/Qiskit code snippet |
| Lab compatibility test | Hardware backend requirements |
| Patient recovery / vitals | Circuit fidelity after mitigation |
| Treatment log | Execution history / learning trail |

### Three Progressive Wards

| Ward | Skill Level | Activity |
|------|-------------|----------|
| 🏥 Ward 1 — Diagnosis | Remember & Understand | Match noise symptoms to treatment departments |
| 📋 Ward 2 — Prescriptions | Apply & Analyze | Pick the correct code from jumbled options |
| 🔬 Ward 3 — Lab Compatibility | Evaluate | Answer hardware backend questions |

### Immediate Feedback

- Correct answers: patient fidelity improves, score increases with streak bonus
- Wrong answers: fidelity drops, correct answer is highlighted
- Every answer shows an educational explanation of the Samplomatic concept
- Treatment log records all actions with timestamps

### Gamification

- **Score** with streak bonuses (longer streaks = more points per correct answer)
- **Patient counter** — track how many patients you've successfully treated
- **Vitals monitor** — visual fidelity gauge shows circuit quality
- **Three wards** — switch between difficulty levels anytime

---

## 💻 Technologies Used

- **HTML5** — semantic structure
- **CSS3** — custom animations, responsive grid layout, hospital-themed design
- **Vanilla JavaScript** — all game logic, no frameworks, zero dependencies
- **localStorage** — patient progress persists across sessions (in quiz companion)
- Runs entirely in the browser — no server, no build step, no installation

---

## 🕹️ How to Play

### Ward 1 — Diagnosis
1. A patient arrives in the ambulance bay with symptom tags
2. **Click the patient** to select them (blue border appears)
3. **Click the correct department** based on their symptoms
4. Watch the vitals monitor — fidelity goes up if correct, down if wrong
5. Read the educational explanation
6. Click **Admit Next Patient** to continue

### Ward 2 — Prescriptions
1. Click the **Ward 2: Prescriptions** tab
2. A patient arrives with symptoms
3. Four code snippets appear — **pick the correct prescription**
4. Wrong answers highlight the correct code
5. Read the explanation and continue

### Ward 3 — Lab Compatibility
1. Click the **Ward 3: Lab Compatibility** tab
2. Answer multiple-choice questions about Samplomatic hardware requirements
3. Topics: Heron devices, basis gates, backend switching, simulator limitations
4. Click **Next Question** to continue through all hardware topics

### Controls
- **Admit Next Patient / Next Question** — advance after answering
- **Reset** — restart current ward
- **Ward tabs** (🏥 📋 🔬) — switch between difficulty levels

---

## 📁 Project Structure
samplomatic-emergency-room/
├── samplomatic_er.html # Main game file (all three wards)
├── README.md # This documentation
└── assets/
 

text

---

## 🔮 Future Improvements

1. **Ward 4 — Multi-Step Surgery** — Patients requiring sequenced treatments (Twirl → InjectNoise → PNA) in the correct order
2. **Real QPU Integration** — Connect to IBM Quantum backends to show live noise data and run actual NoiseLearnerV3 jobs
3. **Leaderboard** — Track scores across players using a simple backend
4. **Timed Emergency Mode** — Add time pressure for advanced learners
5. **PWA Version** — Package as Progressive Web App for offline mobile play
6. **SLC Lightcone Visualization** — Interactive diagram showing which noise generators are pruned for local observables
7. **Multi-language Support** — Translate symptom tags and explanations
8. **Accessibility** — Screen reader support, keyboard-only navigation

---

## ⚠️ Important Note

This game is an **educational simulation** that teaches Samplomatic concepts, workflows, and code patterns. It does **not** connect to IBM Quantum hardware.

Real Samplomatic requires:
- An IBM Quantum Platform account with access to a **Heron device**
- Qiskit Runtime sessions for `NoiseLearnerV3` and `Executor` jobs
- Real QPU execution time (approximately 1-2 minutes per noise learning job)

This game prepares learners to use those tools correctly when they do have hardware access — teaching which annotation to choose, what code to write, and which backend requirements to check.

---

## 🙏 Credits

Built by **Noor Ul Ain Faisal**

**Credentials:**
- IBM Qiskit Advocate (2025)
- Friend of OQI, Open Quantum Institute at CERN (2026)
- QGSS 2026 Mentor — Qiskit Advocate Mentorship Program
- unitaryHACK 2026 Winner — Elliot the Electron (BB84 Quantum Game)
- Member, IEEE GRSS QUEST Technical Committee
- IBM Community Blogger
- Only participant from Pakistan to pass IBM QGSS (anti-LLM conditions)

**Location:** Sialkot, Pakistan

**Based on:** QGSS 2026 Lab 3 — *"Your New Tool For Quantum Advantage"* covering Samplomatic, NoiseLearnerV3, Propagated Noise Absorption (PNA), and Shaded Lightcones (SLC).

---

## 📄 License

MIT — free to use, modify, and distribute for educational purposes.

---

## 🔗 Links

- [Qiskit Samplomatic Documentation](https://github.com/Qiskit/samplomatic)
- [QGSS 2026](https://qiskit.org/events/summer-school-2026)
- [IBM Quantum Platform](https://quantum.ibm.com)
- [WISER Education Challenge](https://wiser-education.challenge)
