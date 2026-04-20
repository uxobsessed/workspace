# How to use this vault

## Why this structure?

This vault exists for one thing: learning without losing what you've learned. The previous structure tried to handle *projects, areas, and active tracking on top of that* introducing friction & noise for someone wanting to learn something new. Better tools exist to accomplish those goals. I plan to use Obsidian for what it's best at; capturing, connecting & compounding knowledge over time.

## What's new?

This version strips it down to the only two things that actually matter: capturing raw knowledge while you're learning it (Notes), and turning that knowledge into something polished when you're ready (Technical Write-ups).

Like all things, this solution isn't perfect. If you find this method slowing you down, curate your own. There will never be a one-size-fits-all when it comes to something as personal as how you learn.

## Some things to know before you get started

> [!IMPORTANT]
> Git doesn't allow pushing empty folders. I've only added `.gitkeep` files to the top-level folders you'll need immediately. Domain subfolders inside `10 - Notes/` (e.g. `JS/`, `CSS/`, `React/`) are yours to create as you go. Don't pre-create folders for subjects you haven't started yet.

Also, these README files use traditional markdown links and relative links so these can be viewed on GitHub as-is without cloning first. The setting to use Wiki-links has been left turned _on_ so you get a better experience inside Obsidian. If you make a README for your own GitHub version, use normal markdown links there.

## Getting started
*Simply clone this repo and change the git remote to your personal repo to avoid issues when trying to push and pull in the future*.

> [!TIP] First thing to do once you've cloned this. Create a domain subfolder inside `10 - Notes/` for the subject you're currently studying. That's it. Start filing notes there immediately. Don't waste time setting up folders for things you haven't touched yet.

_If you're unsure where something goes, put it in `00 - Inbox/` and organize it later._

> [!NOTE] Keep active folders small. When a note or writeup becomes inactive, you're no longer referencing it, building on it, or planning to; move it to `40 - Archive/` instead of letting it rot in place.

---

## The folders (brief overview)

`00 - Inbox/` is the pressure valve. Dump anything here when you don't have time to think about where it belongs. The only rule is that you clear it periodically, weekly works. [W](#Whats-).

`10 - Notes/` is the knowledge base. Atomic notes written in your own words, organized by domain. One concept per file. This is where "what I learned" lives. For notes that are rough or unfinished, use a `(raw)` suffix so you don't lie to yourself: `Notes/JS/event-loop(raw).md`. [More on Notes](#What-goes-in-Notes-10---Notes).

`20 - Devlog/` is for shippable writing. Refined writeups you understand well enough to explain clearly — meant for a portfolio, a blog, or just your own record of mastery. These can be drafts first. Use tags like `#draft` and `#final` to track state. [More on Devlog](#What-goes-in-Devlog-20---Devlog).

`30 - Sources/` tracks where your knowledge comes from. Books, courses, documentation sites, YouTube channels — logged here with status and links to the notes they produced. This is not a notes folder; it's a _provenance_ folder. [More on Sources](#What-goes-in-Sources-30---Sources).

`40 - Archive/` is for inactive material from any of the above folders. Active stays visible; inactive gets out of the way. [More on Archive](#What-Archive-is-40---Archive).

`90 - Meta/` is the vault's operating manual: this guide, templates, and attachments. [More on Meta](#What-goes-in-Meta-90---Meta).

---

## What goes in Inbox (`00 - Inbox`)

Inbox has no structure and no rules except one: don't leave things here permanently.

Use it when:

- You're mid-session and want to capture something without breaking flow.
- You've encountered a concept you don't understand yet and want to come back to it.
- You have a half-formed idea for a writeup but aren't ready to start it.

Clear it weekly. For each item: either file it into `10 - Notes/` under the right domain, promote it to a `20 - Devlog/` draft, add it to `30 - Sources/`, or delete it. If something sits in Inbox for more than two weeks without a clear destination, it probably wasn't worth keeping.

---

## What goes in Notes (`10 - Notes`)

Notes is the core of this vault. Everything you learn gets written here first, in your words, at the atomic level — one concept, one file.

**How to organize it:** Create one subfolder per domain. Keep it one level deep. Don't nest subfolders inside subfolders.

```
10 - Notes/
├── JS/
├── CSS/
├── React/
├── Browser/
└── Tooling/
```

> [!CAUTION] Don't create domain folders preemptively. Create `React/` when you have your first React note, not before. Empty folders are dead weight that makes the vault feel half-finished.

**What a good note looks like:** It answers four things:

- What question was I trying to answer?
- What's the rule or idea, in my words?
- What's a minimal example?
- What's the one gotcha that _will_ bite me later?

You don't need all four every time. Two sentences that clarify a concept are worth more than an empty structured template.

**The `(raw)` suffix:** If a note is incomplete, speculative, or copied more than written, name it `event-loop(raw).md`. This keeps you honest without blocking you from filing it. Raw notes are fine — unlabelled raw notes aren't.

**Linking:** When two notes are genuinely connected, link them. `closure.md` and `prototype-chain.md` both touch how JS scoping works — link them. Don't over-link. A link should mean "you'll want to read this too," not just "these words appeared near each other."

This folder is allowed to grow and be messy. Don't be a perfectionist about it. If you are one, this system will frustrate you — go build something better, because this isn't and won't ever be perfect.

---

## What goes in Devlog (`20 - Devlog`)

Devlog is the "shippable writing" lane. A note graduates here when you understand the topic well enough to explain it to someone else — not when you've memorized it, but when you've internalized it.

These are the pieces that end up on a portfolio, a blog, or a public repo. They reference and synthesize Notes but are written for a reader, not as a personal reminder.

A Devlog entry is allowed to start as a draft. The progression looks like this:

1. You've accumulated several Notes on a related cluster of concepts.
2. You notice a coherent explanation forming across them.
3. You open a new file in `20 - Devlog/`, tag it `#draft`, and write a first pass that references those notes.
4. You iterate until it reads cleanly without needing the source notes open beside it.
5. Tag it `#final` when it's done.

If your understanding of a topic is still half-baked, keep it in `10 - Notes/` and don't force a Devlog entry. A weak writeup is harder to fix later than a raw note.

> [!NOTE] The folder name `Devlog` is a suggestion, not a rule. Rename it to `Writing/`, `Blog/`, `Essays/`, or whatever matches how you think about it. The purpose is what matters: finished output, not active learning.

---

## What goes in Sources (`30 - Sources`)

Sources tracks where your knowledge comes from. It exists separately from Notes because they serve different jobs: Notes is what you learned, Sources is what you learned it _from_.

Without this folder, source information bleeds into Notes and pollutes them — or you lose track of what you've actually read versus what you've skimmed.

**One file per source.** A source is a book, a course, a documentation site, a YouTube channel, a specific talk. Each file should answer:

- What is this? (one-line description)
- Status: reading / done / abandoned / ongoing
- Which notes did this produce? (links to `10 - Notes/` files)
- What sections or chapters are still worth returning to?

**What Sources is not:** A notes folder. Don't copy content into a Source file. If a book explains something worth keeping, write that understanding in `10 - Notes/` in your own words, then link back to the Source. The Source file just says "chapter 4 produced `Notes/JS/closure.md`."

Example Source file for a book:

```markdown
# You Don't Know JS — Kyle Simpson

**Status:** In progress (Book 1 done, Book 2 ch.3)
**Type:** Book

## Notes produced
- [[Notes/JS/closure]]
- [[Notes/JS/prototype-chain]]
- [[Notes/JS/event-loop(raw)]]

## Worth returning to
- Book 2, ch.5 — async patterns
- Book 3 — types & coercion (not started)
```

---

## What Archive is (`40 - Archive`)

Archive is not a trash can. It's a parking lot for things that are no longer active but might be useful later. The structure mirrors the root level — archived Notes go in `Archive/Notes/`, archived Devlog drafts go in `Archive/Devlog/`, and so on.

```
40 - Archive/
├── Devlog/
├── Inbox/
├── Notes/
└── Sources/
```

Move something here when:

- A Notes subfolder for a domain you've stopped studying is just sitting there.
- A Devlog draft has been abandoned (but you don't want to delete it).
- A Source you've finished and won't reference again is adding noise.
- Inbox clutter that you've decided isn't worth filing properly.

If you want to work on something again that was archived, move it back out. Don't leave "re-activated" material inside Archive — it defeats the point.

> [!NOTE] Archive is the reason active folders stay clean. If you stop moving things here, the vault degrades back into a mess over time. The discipline isn't in how you file new things — it's in how consistently you archive old ones.

---

## What goes in Meta (`90 - Meta`)

Meta is the vault's infrastructure. It has three things:

- `guide.md` — this file. The operating manual.
- `Templates/` — note and writeup templates you can copy from.
- `_assets/` — all attachments (images, diagrams, PDFs) land here automatically. Obsidian is configured to route attachments here by default, nested by the folder structure they came from.

Don't store learning content in Meta. If something you're writing doesn't belong in Notes, Devlog, Sources, or Inbox, it probably doesn't belong in the vault at all.

**Templates:** Two templates are included. Copy them out when starting something new — don't write in the template files themselves.

```
90 - Meta/Templates/
├── note-template.md      # For atomic Notes entries
└── writeup-template.md   # For Devlog drafts
```

`note-template.md` covers: topic, date, status (raw/done), concept in your words, minimal example, gotcha, and links to related notes.

`writeup-template.md` covers: title, status tag, the question this answers, core concept, mechanism, common mistakes, and further reading.

---

## How this will work: with examples

**You're learning something new:** Write in `10 - Notes/<domain>/`. File it under the right domain subfolder, or drop it in `00 - Inbox/` if you don't have time to think about it.

**You're reading a book or following a course:** Create a file for it in `30 - Sources/` and link the notes it produces back to it.

**You want to write up something you understand well:** Open a new draft in `20 - Devlog/`, tag it `#draft`. Pull from your Notes. Iterate until it stands on its own.

**A domain you were studying has gone cold:** Move the subfolder from `10 - Notes/` to `40 - Archive/Notes/`.

**A Devlog draft is dead:** Move it to `40 - Archive/Devlog/`.

---

## Git (keep it clean)

One commit should represent one kind of work. If you took notes and also rewrote a Devlog post, those should be separate commits. The goal is readable history later, not saving keystrokes now.

Good commit messages say what changed and why, not just what file was touched:

- `notes: add closure + prototype-chain (JS)`
- `devlog: first draft — how JS handles async`
- `archive: JS basics folder, no longer active`

---

# Vault structure ^vault-tree

```
notebook/
├── 00 - Inbox/                    # Unsorted captures, clear weekly
├── 10 - Notes/                    # Atomic notes by domain, one concept per file
│   ├── JS/
│   │   ├── event-loop.md
│   │   ├── closure.md
│   │   ├── prototype-chain.md
│   │   └── promises-vs-async-await.md
│   ├── CSS/
│   │   ├── flexbox.md
│   │   ├── specificity.md
│   │   └── stacking-context.md
│   ├── React/
│   │   ├── useEffect-mental-model.md
│   │   ├── reconciliation.md
│   │   └── context-vs-state.md
│   ├── Browser/
│   │   ├── critical-render-path.md
│   │   ├── http-caching.md
│   │   └── cors.md
│   └── Tooling/
│       ├── vite-vs-webpack.md
│       └── git-rebase-vs-merge.md
├── 20 - Devlog/                   # Finished or in-progress writeups
│   ├── how-js-handles-async.md           #final
│   ├── css-layout-systems-explained.md   #final
│   ├── react-rendering-deep-dive.md      #draft
│   └── web-performance-checklist.md      #draft
├── 30 - Sources/                  # Where your knowledge comes from
│   ├── you-dont-know-js.md
│   ├── javascript-info.md
│   ├── web-dev-simplified-yt.md
│   └── mdn-bookmarks.md
├── 40 - Archive/                  # Inactive material, mirrors root structure
│   ├── Devlog/
│   ├── Inbox/
│   ├── Notes/
│   └── Sources/
├── 90 - Meta/
│   ├── _assets/                   # All attachments routed here automatically
│   │   ├── diagrams/
│   │   └── images/
│   ├── Templates/
│   │   ├── note-template.md
│   │   └── writeup-template.md
│   └── guide.md                   # This file
└── README.md
```