# NeuroGenius X v4 — Reflective Cognitive Studio

NeuroGenius X v4 is a single-file, browser-based cognitive studio that demonstrates local AI-assistant concepts without requiring a backend or API key. It combines a chat interface, adaptive modes, simulated cognitive metrics, local memory, knowledge-vault retrieval, reflection logs, evidence-gap tracking, trajectory learning, goals, export/import, voice controls, and animated neural visualizations.

The project is designed as an experimental interface for exploring how future personal assistants might expose memory, uncertainty, retrieval, reflection, and user-control mechanisms in a transparent way.

---

## Key Features

### Conversational Modes

NeuroGenius X includes six assistant modes:

* **Standard** — balanced, general-purpose responses.
* **Creative** — invention, analogies, remixing, and futuristic ideas.
* **Analytical** — structured reasoning, trade-offs, risks, and step-by-step breakdowns.
* **Empathetic** — supportive, tone-aware responses.
* **Research** — separates claims, evidence, uncertainty, and verification needs.
* **Builder** — implementation-focused planning, checklists, and prototype guidance.

Modes can be selected from the top chat toolbar or changed with commands such as:

```text
/mode creative
/mode analytical
/mode research
/mode builder
```

---

## Local Memory System

The app includes a browser-local memory system. You can save facts by typing messages such as:

```text
remember that I prefer detailed code examples
remember that this project should stay single-file
```

Saved memories appear in the **Long-term memory** panel and are retrieved automatically when relevant to future prompts.

Memory features include:

* Explicit memory capture using `remember that...`
* Automatic lightweight memory capture for longer, topic-rich messages
* Memory scoring based on relevance and retention
* Ebbinghaus-style memory decay
* Weak-memory pruning
* Context chips generated from active topics and useful memories

All memories are stored in the browser using `localStorage`.

---

## Knowledge Vault

The **Knowledge Vault** lets you paste project notes, requirements, source text, or facts into a local retrieval area.

Use cases:

* Store project requirements
* Paste research notes
* Add feature plans
* Keep design constraints
* Provide source material for future responses

The assistant retrieves relevant vault notes when answering and displays them as evidence pills under the response.

Example vault note:

```text
The app must remain a single HTML file, keep all existing features, and work offline except for optional CDN libraries.
```

---

## Evidence Gap Tracker

The **Evidence Gap Tracker** detects when a prompt may need missing information or external verification.

It can flag gaps such as:

* Time-sensitive information
* Current facts, prices, laws, schedules, or news
* Missing decision criteria
* Low user confidence
* No supporting local memory or vault evidence

This helps the app show where uncertainty comes from instead of only giving a single confidence number.

---

## Trajectory Learnings

Trajectory learnings are small strategy notes distilled from recent interaction patterns.

The system can learn patterns such as:

* When errors appear, isolate the failing feature and preserve working behavior.
* For innovation requests, convert research ideas into visible interface features.
* For documentation requests, explain feature value before setup and usage.

You can manually generate them with the **Distill** button, or they are generated automatically every few turns.

---

## Reflection Log

The **Reflection Log** summarizes recent conversation direction and suggests next moves.

It tracks:

* Recent topics
* User/assistant turn balance
* Suggested next actions
* Current focus areas

Click **Reflect now** to generate a reflection manually.

---

## Goals System

NeuroGenius X includes a simple local goal tracker.

You can create goals by:

* Clicking **+ Goal**
* Asking for a plan with `plan:`

Example:

```text
plan: build a study dashboard
```

The app will create a checklist in the Goals panel.

---

## Response Controls

The **Response Controls** panel lets you tune how the assistant responds.

Controls include:

* **Depth** — how detailed the answer should be.
* **Novelty** — how experimental or creative the answer should be.
* **Transparency** — how much trace/checker information to show.
* **Your confidence** — lets the assistant adapt explanations based on how confident you feel.

The **Defaults** button resets these controls.

---

## Checker Trace and Uncertainty Notes

When transparency is enabled, answers include a collapsible checker trace.

The trace usually includes:

* **Router** — whether the app used memory/vault retrieval.
* **Analyzer** — detected topic, domain, and complexity.
* **Retriever** — number of memories, vault notes, and trajectory learnings found.
* **Generator** — active mode and control settings.
* **Checker** — confidence and uncertainty notes.

For time-sensitive prompts, the app warns that it cannot verify live information by itself.

---

## Neural Dashboard

The left dashboard visualizes simulated cognitive capacity:

* Knowledge Matrix
* Creativity Engine
* Problem Solving
* Communication
* Intelligence score
* Confidence score
* Context depth
* Learning rate
* Memory usage

The values change as you interact with the assistant.

---

## Visualizations

NeuroGenius X includes two visual systems:

### Neural Pathways

An animated canvas graph showing simulated connections between cognitive modules.

### Capacity Radar

A radar chart powered by Chart.js when available. If Chart.js fails to load, the app falls back to a built-in bar-style visualization.

---

## Voice and Speech

The app supports browser-based voice features when available:

* **Voice input** using the Web Speech Recognition API
* **Speak last answer** using browser speech synthesis

Browser support may vary. Chrome-based browsers usually provide the best support.

---

## Commands

Available commands:

```text
/help
```

Shows a usage guide.

```text
/mode creative
/mode analytical
/mode empathetic
/mode research
/mode builder
/mode standard
```

Switches assistant mode.

```text
/memory
```

Shows saved local memories.

```text
/vault
```

Shows saved Knowledge Vault notes.

```text
/export
```

Exports the current brain state as JSON.

```text
/clear
```

Resets the local app state.

---

## Export and Import

Use **Export brain** to download a JSON file containing:

* Conversation history
* Memories
* Vault notes
* Reflections
* Evidence gaps
* Trajectory learnings
* Goals
* Settings
* Cognitive metrics

Use **Import** to restore a previous export.

The export version is currently:

```text
4.0.0
```

---

## Privacy

NeuroGenius X v4 is privacy-first by design.

The app stores data locally in the browser using:

```text
localStorage
```

It does not send chat content to a server. It does not require an account, API key, or backend.

Optional CDN libraries are loaded for enhanced features, but the app includes fallbacks if they fail.

Stored browser data includes:

* Memory items
* Vault notes
* Goals
* Conversation history
* Reflections
* Evidence gaps
* Trajectory learnings
* Settings

To erase local data, click **Reset System** or use:

```text
/clear
```

---

## Optional External Libraries

The app attempts to load these optional libraries:

* **Chart.js** — radar chart visualization
* **Math.js** — safe arithmetic expression evaluation
* **Compromise NLP** — topic, noun, and entity extraction

If a library does not load, NeuroGenius X continues using built-in fallback logic.

---

## How to Run

### Option 1: Open directly

Save the file as:

```text
index.html
```

Then open it in a modern browser.

### Option 2: Run with a local server

Some browsers apply stricter rules when opening files directly. A local server is recommended for best results.

Using Python:

```bash
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

---

## Browser Compatibility

Recommended:

* Chrome
* Edge
* Brave
* Other modern Chromium-based browsers

Also works in many recent versions of Firefox and Safari, though voice recognition support may vary.

---

## Project Structure

NeuroGenius X v4 is intentionally built as a single HTML file:

```text
index.html
```

Inside that file:

```text
<head>
  CSP policy
  optional CDN libraries
  CSS design system
</head>

<body>
  dashboard UI
  chat interface
  cognitive laboratory
  JavaScript app logic
</body>
```

Major JavaScript systems:

* State loading and saving
* NLP processing
* Mode routing
* Response generation
* Memory capture and retrieval
* Vault retrieval
* Evidence-gap tracking
* Trajectory-learning distillation
* Reflection generation
* Goal management
* Chart rendering
* Canvas neural animation
* Export/import
* Voice input
* Speech output

---

## Security Notes

The app includes a Content Security Policy to reduce unsafe behavior.

It avoids rendering user chat as raw HTML. Messages are inserted using text nodes and controlled DOM creation.

Arithmetic evaluation is restricted to simple mathematical characters before Math.js is used.

---

## Limitations

NeuroGenius X v4 is an experimental local simulation, not a real cloud AI model.

Current limitations:

* It cannot browse the web.
* It cannot verify live facts by itself.
* Its reasoning is rule-based and simulated.
* Its memory is local to the browser and device.
* Clearing browser storage will remove saved state unless exported first.
* Voice features depend on browser support.
* Optional CDN libraries may be blocked by privacy extensions, offline use, or CSP/network restrictions.

For current facts, news, prices, legal rules, medical details, financial decisions, or safety-critical information, verify with trusted external sources.

---

## Example Prompts

Try:

```text
/help
```

```text
remember that I like advanced single-file HTML apps
```

```text
plan: improve this app into a research assistant
```

```text
brainstorm novel features for a cognitive studio
```

```text
compare local memory versus cloud memory
```

```text
summarize our current project direction
```

```text
24*(3+7)
```

```text
Use my vault notes to make a feature checklist
```

---

## Suggested Roadmap

Possible future upgrades:

* Assumption ledger for tracking hidden assumptions
* Self-debate snapshots with proposer, skeptic, and arbiter roles
* Memory contradiction detection
* Memory confidence and evidence-quality scores
* Searchable transcript timeline
* Markdown export
* Theme editor
* Offline service worker support
* Plugin-style feature modules
* Better accessibility preferences
* More advanced local summarization
* User-editable memory cards
* Visual memory graph
* Drag-and-drop vault import
* Project workspaces

---

## Development Philosophy

NeuroGenius X v4 follows these principles:

1. **Keep existing features working.**
2. **Turn placeholders into real interactions.**
3. **Expose uncertainty instead of hiding it.**
4. **Store personal data locally by default.**
5. **Prefer visible, inspectable systems over invisible magic.**
6. **Make complex assistant behavior understandable through UI.**
7. **Support experimentation without requiring a backend.**

---

## License

Choose a license before publishing. Suggested options:

* MIT License for open, permissive reuse
* Apache-2.0 for permissive reuse with patent language
* GPL-3.0 if derivatives should remain open source

Example placeholder:

```text
MIT License — add full license text before distribution.
```

---

## Credits

Built as an experimental single-file browser app exploring:

* Local-first AI interfaces
* Reflective memory
* Retrieval-augmented interaction
* Transparent uncertainty
* Cognitive dashboards
* Human-controlled assistant behavior

NeuroGenius X v4 is intended for learning, prototyping, experimentation, and interface design exploration.
