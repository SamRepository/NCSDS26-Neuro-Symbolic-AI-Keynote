# Neuro-Symbolic AI — NCSDS-26 Keynote

> How knowledge graphs and ontologies are learning to live inside large
> language models — and why that changes everything.

A 20-minute keynote delivered at **NCSDS-26**, ENSET-Skikda (Azzaba, Algeria)
by **Dr. Samir Sellami** — LIRE Laboratory, Univ-Constantine 2 / Dept. of
Mathematics & Computer Science, ENSET-Skikda.

**Live deck:** https://samrepository.github.io/NCSDS26-Neuro-Symbolic-AI-Keynote/Neuro-Symbolic%20AI.html
*(available once GitHub Pages is enabled — see "Publishing" below)*

---

## The argument

Twenty-one slides in four acts:

1. **History** — the symbolic and neural traditions, and how they got us to LLMs.
2. **Limits** — hallucination, no provenance, no consistency: why fluent
   confidence is a liability in high-stakes domains.
3. **Structure returns** — knowledge graphs and ontologies as the explicit,
   queryable, auditable alternative to billions of opaque weights.
4. **Synthesis — Knowledge-Infused Learning** — the architecture of the next
   decade, with benchmarks (Soman 2023, Xu 2024 SIGIR, MEGA-RAG 2025,
   Microsoft GraphRAG 2024) and four practice cases: healthcare, legal,
   enterprise, education.

Close: **"The future of AI is not neural, it is not symbolic — it is both.
Build with both hands."**

---

## Files

| File | What it is |
|---|---|
| [`Neuro-Symbolic AI.html`](Neuro-Symbolic%20AI.html) | The 21-slide deck itself. Open in a browser, press `F11`. |
| [`deck-stage.js`](deck-stage.js) | Slide navigation (keyboard + presenter bridge). |
| [`presenter.html`](presenter.html) | Companion window — shows current note + next note + timer, syncs to the deck via `postMessage`. |
| [`full-notes.html`](full-notes.html) | Printable speaker notes — ~7 A4 pages with timing per slide. |
| [`cheatsheet.html`](cheatsheet.html) | One-page A4 cue card with opening sentences and anchor beats. |
| [`logos/`](logos/) | NCSDS-26 and ENSET-Skikda institutional logos. |

PDFs of the speaker notes and cue card are gitignored — regenerate locally
with **Ctrl+P → Save as PDF** in your browser.

---

## Run locally

```bash
git clone https://github.com/SamRepository/NCSDS26-Neuro-Symbolic-AI-Keynote.git
cd NCSDS26-Neuro-Symbolic-AI-Keynote
```

Then double-click `Neuro-Symbolic AI.html` to open in your default browser.

Keyboard shortcuts on the deck:

| Key | Action |
|---|---|
| `→` / `Space` / `PgDn` | Next slide |
| `←` / `PgUp` | Previous slide |
| `Home` / `End` | First / last slide |
| `R` | Reset to slide 1 |
| `F11` | Toggle fullscreen |

---

## Presenter view (second screen with synced notes)

1. Open **`presenter.html`** on your laptop screen.
2. Click **"Open the deck"** — the deck opens in a new window.
3. Drag the deck window to the projector display, then press `F11`.
4. Click back on the presenter window — that's where you'll read from.

The presenter window shows:

- Current slide number + screen-label (e.g. `15 The evidence`)
- The note for the current slide (large)
- The note for the next slide (smaller, dimmed)
- An elapsed timer that turns amber at 16:00 and red at 18:00 (target 20:00)

The two windows talk to each other via `window.postMessage` — no server, no
network. The presenter is the opener; the deck broadcasts
`{ slideIndexChanged: N }` and accepts `{ type: "presenter:nav", … }`
commands.

---

## Publishing on GitHub Pages

This repo is pure static HTML/JS — it works perfectly as a Pages site.
To enable:

1. Repo **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main` / `/ (root)`
4. **Save** — wait ~30 seconds

The deck will then be live at:

`https://samrepository.github.io/NCSDS26-Neuro-Symbolic-AI-Keynote/Neuro-Symbolic%20AI.html`

You can share that link directly with attendees.

---

## Citations referenced on the Evidence slide

- **[Soman et al., 2023]** *Biomedical knowledge graph-optimized prompt
  generation for large language models.* Bioinformatics. — KG-RAG with
  SPOKE: +71% on biomedical multiple-choice QA.
- **[Xu et al., 2024]** *Retrieval-Augmented Generation with Knowledge Graphs
  for Customer Service Question Answering.* ACM SIGIR. — LinkedIn
  deployment: +77.6% MRR, −28.6% median resolution time.
- **[Xu et al., 2025]** *MEGA-RAG: multi-evidence guided answer refinement
  for mitigating hallucinations in public health.* Frontiers in Public
  Health. — over −40% hallucination rate.
- **[Edge et al., 2024]** *From Local to Global: A Graph RAG Approach to
  Query-Focused Summarization.* Microsoft Research. — substantial gains on
  global sense-making over million-token corpora.

---

## Built with

[Claude Designer](https://claude.ai) for the deck export, with subsequent
manual edits to the SVG diagrams, evidence citations, presenter companion,
and printable notes.
