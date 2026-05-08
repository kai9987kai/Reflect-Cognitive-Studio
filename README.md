# Reflect Cognitive Studio

**Reflect Cognitive Studio** is an experimental, browser-based cognitive AI interface built as a collection of single-file HTML prototypes. It explores local-first assistant design, simulated reasoning systems, adaptive memory, evidence tracking, reflective logs, research-style debate, goal planning, and transparent uncertainty tools.

The project does **not** require a backend, account, API key, database, or build step. Open one of the HTML files in a modern browser and start experimenting.

---

## Overview

Reflect Cognitive Studio is designed as a playground for testing how future personal AI tools could expose their internal behaviour to the user.

Instead of hiding everything behind a normal chatbot box, the studio shows systems such as:

- Local memory
- Knowledge vault retrieval
- Evidence-gap tracking
- Reflection logs
- Goal planning
- Agent-style routing
- Simulated reasoning traces
- Cognitive metrics
- Adaptive response controls
- Import/export tools
- Experimental research-inspired AI interface ideas

It is best understood as a **local AI-assistant simulation and interface research lab**, not as a real cloud LLM.

---

## Main Builds

The repository contains multiple experimental versions:

| File | Purpose |
| --- | --- |
| `Ultra - new version.html` | Flagship NeuroGenius X v4 reflective cognitive studio with memory, vault, goals, reflection, evidence gaps, voice tools, checker traces, and neural visualisation. |
| `Research Lab.html` | Research-heavy experimental lab with multi-agent routing, graph memory, uncertainty tracking, evidence auditing, debate/auditor modes, counterfactual concepts, and live analytics. |
| `max.html` | NeuroAdaptive Chat Lab v7 focused on associative memory graphs, contextual bandit-style controls, critic scoring, memory consolidation, debug traces, and evaluation tools. |
| `low.html` | Lightweight/no-CSP safe build that runs with fewer external dependencies and upgrades when optional libraries are available. |

---

## Features

### Local-first cognitive studio

Reflect Cognitive Studio runs in the browser and stores state locally. It is designed for experimentation without requiring a server.

Core local systems include:

- Browser-local memory
- Local conversation state
- Import/export of saved state
- Reset tools
- Privacy-first persistence
- Optional fallback behaviour when external libraries are unavailable

---

### Multiple assistant modes

The studio includes several interaction styles, depending on the build:

- Standard
- Creative
- Analytical
- Empathetic
- Research
- Builder
- Adaptive Router
- Agentic Research
- Debate + Auditor
- Math / Symbolic
- Creative Divergence
- Memory Recall

These modes are used to simulate different assistant behaviours such as planning, brainstorming, analysis, emotional support, research separation, and implementation guidance.

---

### Memory and retrieval

The project experiments with different memory ideas:

- Long-term browser memory
- Associative memory graphs
- Episodic memory
- Memory pruning
- Memory retention controls
- Memory hit scoring
- Knowledge Vault notes
- Local retrieval simulation
- Context chips
- Import/export of memory state

The aim is to make memory visible, adjustable, and inspectable instead of hidden.

---

### Knowledge Vault

The Knowledge Vault lets users add local notes, requirements, facts, research snippets, or project constraints.

Possible uses:

- Store project notes
- Add design requirements
- Keep research notes
- Save feature ideas
- Provide source material for answers
- Test retrieval-style assistant behaviour locally

---

### Evidence-gap tracking

The studio can simulate detection of missing information, uncertainty, or prompts that may require external verification.

It can flag issues such as:

- Time-sensitive questions
- Unsupported claims
- Missing evidence
- Unclear requirements
- Low confidence
- Lack of relevant memory or vault context

This helps explore transparent AI systems that show what they do not know.

---

### Reflection and metacognition

Reflect Cognitive Studio includes reflection-style features such as:

- Reflection logs
- Metacognitive summaries
- Micro-lessons
- Trajectory learning
- Conversation direction tracking
- Suggested next steps
- Recent topic awareness

These systems simulate an assistant that can review its own interaction patterns and improve future responses.

---

### Goal planning

Several builds include local goal and planning tools.

You can use them to:

- Create project goals
- Break ideas into checklists
- Track progress
- Generate plans from prompts
- Convert requests into action steps

Example prompt:

```text
plan: build a research assistant dashboard
```

---

### Experimental research-inspired systems

The more advanced builds explore ideas such as:

- Multi-agent routing
- Debate and auditor loops
- Graph memory
- Evidence auditing
- Counterfactual worlds
- Dream rehearsal
- Ablation testing
- Prompt-genome evolution
- Curiosity-driven experiment search
- Causal hypothesis mapping
- Uncertainty markets
- Red-team mutation loops
- Quality critics
- Contextual bandit-style adaptive controls

These are implemented as local simulations and interface experiments.

---

### Visual dashboards

The project includes visual and diagnostic panels such as:

- Cognitive module cards
- Simulated intelligence/confidence metrics
- Memory usage
- Context depth
- Learning rate
- Neural pathways
- Capacity radar
- Live diagnostics
- Debug logs
- Decision traces
- Event streams
- Built-in test panels

---

### Voice and speech

Where supported by the browser, some builds include:

- Voice input
- Speak last response
- Speech synthesis
- Browser-native speech features

Browser support may vary. Chromium-based browsers usually work best for speech recognition.

---

## How to Run

### Option 1: Open directly

Download or clone the repository, then open one of the HTML files in your browser:

```text
Ultra - new version.html
Research Lab.html
max.html
low.html
```

No installation is required.

---

### Option 2: Run with a local server

Some browser features behave better when served from a local server.

Using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Choose one of the HTML files from the directory listing.

---

## Recommended Starting Point

For the most complete experience, start with:

```text
Ultra - new version.html
```

Use:

```text
Research Lab.html
```

when you want the more experimental research-lab version.

Use:

```text
max.html
```

when testing adaptive memory, reward, critic, and debug systems.

Use:

```text
low.html
```

when you want the lightweight fallback version.

---

## Example Commands and Prompts

Try prompts like:

```text
/help
```

```text
/mode creative
```

```text
/mode research
```

```text
remember that this project should stay single-file
```

```text
plan: improve this into a transparent research assistant
```

```text
Use my vault notes to make a feature checklist
```

```text
Brainstorm novel cognitive-studio features
```

```text
Compare local memory and cloud memory
```

```text
Run an evidence audit on this idea
```

---

## Privacy

Reflect Cognitive Studio is built around local-first experimentation.

The project is designed so that:

- No backend is required
- No account is required
- No API key is required
- State can be stored in the browser
- Memory and vault data can be reset
- Brain/state exports can be saved manually
- Some optional CDN libraries may be loaded depending on the build

Important: because state is browser-local, clearing browser storage may remove saved memories, goals, logs, and vault notes unless exported first.

---

## Limitations

Reflect Cognitive Studio is an experimental prototype.

Current limitations:

- It is not a real LLM.
- It does not truly understand text like a cloud AI model.
- Many cognitive systems are simulated.
- It cannot verify live facts by itself.
- It cannot browse the web.
- Local memory is device/browser-specific.
- Voice features depend on browser support.
- Optional libraries may fail if blocked by browser settings, extensions, CSP rules, or network issues.
- It should not be used for medical, legal, financial, safety-critical, or emergency decisions.

For factual, current, legal, medical, financial, or safety-sensitive topics, verify information with trusted external sources.

---

## Project Structure

```text
Reflect-Cognitive-Studio/
├── CODE_OF_CONDUCT.md
├── LICENSE
├── README.md
├── SECURITY.md
├── Research Lab.html
├── Ultra - new version.html
├── low.html
└── max.html
```

---

## Technology

The project is mainly built with:

- HTML
- CSS
- JavaScript
- Browser APIs
- Local storage
- Canvas-based visualisation
- Optional browser speech APIs
- Optional external frontend libraries depending on the build

No package manager or build tool is required.

---

## Browser Compatibility

Recommended browsers:

- Chrome
- Edge
- Brave
- Other modern Chromium-based browsers

Firefox and Safari may work for many features, but some voice or experimental browser APIs may behave differently.

---

## Security Notes

This project is a client-side prototype. When developing or modifying it:

- Avoid rendering user input as raw HTML.
- Keep local-storage data resettable.
- Be careful with imported state files.
- Treat exported brain/state files as potentially sensitive.
- Review any CDN scripts before production use.
- Do not enter secrets, passwords, private keys, or sensitive personal data into experimental builds.

See `SECURITY.md` for the repository security policy.

---

## Roadmap Ideas

Possible future upgrades:

- Rename the flagship build to `index.html`
- Add GitHub Pages deployment
- Add screenshots/GIF demo
- Add a proper version table
- Add service worker offline mode
- Add workspace/project tabs
- Add searchable transcript history
- Add memory editing UI
- Add memory contradiction detection
- Add visual memory graph
- Add markdown export
- Add theme editor
- Add accessibility preferences
- Add drag-and-drop vault import
- Add plugin-style modules
- Add real test suite
- Add benchmark/evaluation page
- Split large builds into modular files while keeping single-file releases

---

## Contributing

Contributions are welcome.

Good contribution areas include:

- UI improvements
- Accessibility fixes
- Better documentation
- Bug fixes
- Browser compatibility improvements
- Safer local-state handling
- More useful test cases
- New experimental cognitive-interface ideas

Suggested workflow:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test in a modern browser.
5. Open a pull request with a clear explanation.

---

## License

This project is licensed under the MIT License.

See `LICENSE` for details.

---

## Credits

Created by Kai Piper.

Reflect Cognitive Studio is an experimental browser-based lab for exploring transparent, local-first, research-inspired AI assistant interfaces.
