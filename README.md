# 🏥 Samplomatic Mastery Suite

**An interactive educational suite that teaches Samplomatic — Qiskit's framework for advanced quantum error mitigation — through games, quizzes, and a hospital emergency room metaphor.**

Built for the **WISER Education Challenge 2026**.

---

## 🎮 Quick Start

1. Download or clone this repository
2. Open `index.html` in any browser (Chrome, Firefox, Edge, Safari)
3. No installation, no server, no Python required
4. Navigate between all tools from the hub

 
 
## 📁 Project Structure

````
samplomatic-mastery-suite/
│
├── index.html # Main navigation hub
├── samplomatic_er.html # Hospital game with 3 wards
├── quizzes.html # 6-level Bloom's Taxonomy quiz
├── progress.html # Progress tracker and analytics
├── README.md # This documentation
└── thumbnail.png # Cover image (optional)
````
 
---

## 🧩 What Each File Does

| File | Description | Learning Mode |
|------|-------------|---------------|
| `index.html` | Navigation hub linking to all tools | Entry point |
| `game.html` | Matching game — 3 levels (Symptoms, Code, Hardware) | Pattern recognition |
| `quizzes.html` | 6 levels aligned with Bloom's Taxonomy | Structured assessment |
| `progress.html` | Tracks quiz completion, scores, and accuracy | Self-assessment |

---

## 👥 Target Audience

- Qiskit Global Summer School (QGSS) participants
- Quantum computing learners with basic Qiskit knowledge
- Anyone learning error mitigation on IBM Quantum hardware
- Students who want to understand Samplomatic without access to a real backend
- Educators teaching quantum error mitigation concepts

---

## 🎯 Learning Objectives

By using this suite, learners will master:

### Core Samplomatic Concepts

| Samplomatic Tool | What It Does | Real QGSS Lab 3 Context |
|------------------|--------------|--------------------------|
| **Twirl** | Converts coherent noise to stochastic Pauli channels | `Twirl()` annotation on gate boxes |
| **InjectNoise** | Declares where learned noise models apply | `InjectNoise` annotation + `NoiseLearnerV3` |
| **ChangeBasis** | Rotates measurement basis for non-Z observables | `ChangeBasis` on measurement boxes |
| **NoiseLearnerV3** | Characterizes noise per layer | Pauli-Lindblad model with per-generator rates |
| **PNA** | Rewrites observable to absorb anti-noise | `generate_noise_mitigating_observable()` |
| **SLC** | Prunes noise outside observable lightcone | `compute_forward_bounds()` + `compute_local_scales()` |

### Hardware & Backend Awareness

- Samplomatic requires **Heron devices** (ibm_marrakesh, ibm_fez)
- Basis gates for Heron: `cz, id, rz, sx, x`
- Noise models are **device-specific** — switching backends invalidates learned noise
- Simulators **cannot** replace real hardware for NoiseLearnerV3
- ibm_marrakesh = 156 qubits (Heron r2)
- `twirling_strategy="active"` twirls only qubits each box acts on

### Workflow Understanding
Box circuit → Annotate (Twirl/InjectNoise/ChangeBasis) → Build (template + samplex) →
NoiseLearnerV3 → Executor → PNA/SLC mitigation

text

---

## 🏥 Educational Methodology

### Multi-Modal Learning

This suite uses four complementary approaches to reinforce Samplomatic concepts:

| Mode | Tool | Learning Style |
|------|------|----------------|
| **Game-Based** | Hospital ER (`game.html`) |  Pattern recognition, code familiarity |
| **Quiz-Based** | 6-Level Quizzes (`quizzes.html`) | Reading, recall, Bloom's Taxonomy progression |
| **Tracking** | Progress Tracker (`progress.html`) | Self-assessment, motivation through visibility |

### Hospital (game.html)

The hospital game maps quantum error mitigation to emergency room procedures across three wards:

| Ward | Hospital Concept | Samplomatic Concept |
|------|------------------|---------------------|
| 🏥 Ward 1 — Diagnosis | Patient symptoms → treatment department | Noise type → annotation |
| 📋 Ward 2 — Prescriptions | Pick correct prescription from options | Annotation → code snippet |
| 🔬 Ward 3 — Lab Compatibility | Hardware compatibility check | Backend requirements |

### Bloom's Taxonomy Progression (quizzes.html)

| Level | Cognitive Skill | What Learners Do |
|-------|-----------------|------------------|
| 1️⃣ Remember | Recall facts | Identify definitions of Twirl, InjectNoise, ChangeBasis |
| 2️⃣ Understand | Explain concepts | Describe why boxing is important, how Twirl transforms noise |
| 3️⃣ Apply | Use knowledge | Choose the right annotation for a given scenario |
| 4️⃣ Analyze | Compare/contrast | Differentiate Twirl vs ChangeBasis, InjectNoise vs Twirl |
| 5️⃣ Evaluate | Make judgments | Assess when using all annotations is overkill |
| 6️⃣ Create | Design solutions | Design mitigation strategies for complex circuits |

### Immediate Feedback Across All Tools

- **Correct/incorrect indication** with visual feedback (green/red animations)
- **Educational explanations** after every answer
- **Score tracking** with streak bonuses for motivation
- **Progress persistence** via localStorage (quizzes)

---

## 💻 Technologies Used

- **HTML5** — semantic structure across all pages
- **CSS3** — custom animations, responsive grid layouts, themed design
- **Vanilla JavaScript** — all game logic, quiz engine, progress tracking
- **localStorage API** — persistent progress across sessions
- **Zero dependencies** — no frameworks, no build tools, no npm
- **Runs entirely in browser** — no server, no Python, no installation

---

## 🕹️ How to Use

### Starting Out
1. Open `index.html` — the main hub
2. Choose your learning path:
   - **🏥 Hospital Game** (`game.html`) — Match symptoms, code, and hardware
   - **📝 Quizzes** (`quizzes.html`) — Test knowledge across 6 Bloom's levels
   - **📊 Progress** (`progress.html`) — Track your mastery

### Noise Matcher (game.html)
- **Level 1** — Match noise symptom tags to treatment cards
- **Level 2** — Pick correct Python/Qiskit code from jumbled snippets
- **Level 3** — Answer hardware/backend multiple-choice questions

### Quizzes (quizzes.html)
- 6 levels aligned with Bloom's Taxonomy
- Each level has 3-5 questions
- Score tracking and completion badges
- Keyboard shortcuts: `1-4` to select, `Enter` to advance, `R` to reset

### Progress Tracker (progress.html)
- View completed quiz levels
- Track total score and accuracy percentage
- Reset progress option

---

## ⚠️ Important Note

This suite is an **educational simulation** that teaches Samplomatic concepts, workflows, and code patterns. It does **not** connect to IBM Quantum hardware.

Real Samplomatic requires:
- An IBM Quantum Platform account with access to a **Heron device**
- Qiskit Runtime sessions for `NoiseLearnerV3` and `Executor` jobs
- Real QPU execution time (approximately 1-2 minutes per noise learning job)

This suite prepares learners to use those tools correctly when they do have hardware access — teaching which annotation to choose, what code to write, and which backend requirements to verify.

---

## 🔮 Future Improvements

1. **Multi-Step Surgery (Ward 4)** — Patients requiring sequenced treatments (Twirl → InjectNoise → PNA) in the correct order
2. **Real QPU Integration** — Connect to IBM Quantum backends for live noise data and actual NoiseLearnerV3 jobs
3. **Leaderboard** — Track scores across players via a simple backend
4. **Timed Emergency Mode** — Add time pressure for advanced learners
5. **PWA Version** — Package as Progressive Web App for offline mobile play
6. **SLC Lightcone Visualization** — Interactive diagram of which noise generators are pruned for local observables
7. **Multi-language Support** — Translate symptom tags and explanations
8. **Accessibility** — Screen reader support, keyboard-only navigation
9. **Teacher Dashboard** — Track class progress across all students
10. **API Integration** — Submit scores to a central WISER leaderboard

---

## 🧪 Content Source

All educational content is based on **QGSS 2026 Lab 3**: *"Your New Tool For Quantum Advantage"*

Topics covered from the lab:
- **Chapter 1:** Error mitigation as a Runtime product (DD, PT, TREX, ZNE, PEA, PEC)
- **Chapter 2:** Samplomatic boxes, annotations, NoiseLearnerV3, Executor, templates, samplex
- **Chapter 3:** Propagated Noise Absorption (PNA), Probabilistic Error Cancellation (PEC), Shaded Lightcones (SLC)

---

## 🙏 Credits

Built by **Noor Ul Ain Faisal**

**Credentials:**
- IBM Qiskit Advocate  
- QGSS 2026 Mentor —
- Mentor - Qiskit Advocate Mentorship Program (QAMP)
- unitaryHACK 2026 Winner — Elliot the Electron (BB84 Quantum Game)
- unitaryHack February 2026 - PR Merged
- Member, IEEE GRSS QUEST Technical Committee
- IBM Community Blogger

**Location:** Sialkot, Pakistan

**Background:** Quantum Mechanics for Scientists and Engineers, EdX Stanford, MA English Literature, PGD Computer Science, B.Com. Self-taught in quantum mechanics, Python, Qiskit, NetSquid, and AI/ML.

---

## 📄 License

MIT — free to use, modify, and distribute for educational purposes.

---


## 🤖 AI Use Disclosure

**Generative AI tools used in this project:**

| Tool | Purpose | Extent |
|------|---------|--------|
| **DeepSeek** (via Cursor) | Game design brainstorming, code scaffolding, README drafting | Assisted with initial HTML/CSS/JS structure, hospital metaphor development, quiz question formulation, and documentation |
| **Manual refinement** | All code reviewed, tested, debugged, and finalized by the author | 100% of final code verified and validated |

**All Samplomatic educational content** is sourced directly from **QGSS 2026 Lab 3** materials, not generated by AI. The hospital metaphor, patient scenarios, code snippets, and hardware questions are based on the author's experience as a QGSS 2026 Mentor and IBM Qiskit Advocate.

**The author can explain, verify, and defend every line of code and every educational concept in this submission.**

---
## 🔗 Links

- [Qiskit Samplomatic Documentation](https://github.com/Qiskit/samplomatic)
- [WISER Education Challenge](https://wiser-education.challenge)
- [Qiskit Addon PNA](https://qiskit.github.io/qiskit-addon-pna/)
- [Qiskit Addon SLC](https://qiskit.github.io/qiskit-addon-slc/)
