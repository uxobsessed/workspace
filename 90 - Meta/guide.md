# How to use this vault

*Before reading this, I suggest you set up this vault following the instructions in [[README]]. This guide is much more readable in Obsidian*
## Why this structure?

Two folders do all the actual work: `10 - Notes` for capturing what you learn, `20 - Projects` for what you build with it. Everything else just supports those two.

Numbers jump around on purpose. `20` to `40`, `40` to `80`. So there's room to add your own folders in between without renumbering the whole vault. If you need a `25 - Writing` & `30 - Blogs`, you have the room to create them

==I've added `01 - Daily` and set up the *core plugin* Daily Notes to create a daily note with the proper filename, directly in that folder, with a simple click of the calendar icon in the side ribbon.== an example note has been left in as [[11th Sep '26]], It's pretty self explanatory so I won't be going into it more.

If any of this slows you down, change it. Workflows are not a one-shoe-fits-all. *Change things around to however they work for you.*

## The Layout

```
notebook/
├── 00 - Inbox/          # unsorted stuff, random notes, rough brain dump
├── 01 - Daily/          # Tracking the day's activity, TODOs & More
├── 10 - Notes/          # what you've learned, nested by domain & topic
├── 20 - Projects/       # what you're building, ideas, etc.
├── 40 - Sources/        # resources for what you're learning etc.
├── 80 - Archive/        # inactive stuff, mirrors the root
└── 90 - Meta/
    └── _assets/         # attachments & diagrams, handled automatically
```

---

## `00 - Inbox`

This is where stuff lands mid-session before you've had time to think about where it goes. Half-formed ideas, sprint work, quick captures. Things you just want to get out of your head & into your notes quickly.

You can make subfolders in here, unlike in Notes if you're actively working on something and it's not ready to file, give it its own folder.

Status lives in the tag, not the folder name. A few to start with:

| Tag        | Means                          |
| ---------- | ------------------------------ |
| `#capture` | raw, unprocessed, needs a look |
| `#active`  | still working on it            |
| `#unsure`  | don't get it yet               |
Clear it out periodically. Each item either goes into `00 - Notes/`, gets upgraded into a proper project idea and put into `20 - Projects/`, or gets deleted. If something's been sitting for two weeks with nowhere obvious to go, it probably wasn't worth keeping anyways.

---

## `10 - Notes`

Where everything you learn gets written down here, in your own words, one concept per file. If you're not sure where something goes, it goes here by default.

> [!Danger] Recommended: Have a structured roadmap/track to follow
> I highly recommend to have a structure to follow. This vault template was mirrored to fit my needs, and I self study & teach myself SWE. for this i have ==Trackers on Notion== & ==Full in depth markdowns in Obsidian== (in `Sources` under `Tracks/`) properly breaking down the entire roadmap. This really helps break down what you're meant to learn, in which order, and in what depth. *more on this later*
> 
> ![[IMG-20260902200643663.png]]
> *an example of a roadmap being used by one of my friends*

One folder per domain. Inside that, nest further if you're working through a track, a roadmap, a course, whatever. And keep those grouped as topic subfolders. Anything that isn't part of a track just sits loose in the domain folder.

```
10 - Notes/
├── JS/
│   ├── Fundamentals/       ← a track: closures, event loop, this, etc.
│   └── 3 Pillars of JS.md  ← standalone, no track
├── Rust/
│   └── Engine/       ← borrow checker, types etc.
```

> [!CAUTION] Good Practice while working on notes 
> ==Don't make domain folders ahead of time.== Make `Rust/` when you actually write your first Rust note.

A good note usually covers what question you were answering, the rule or idea in your own words, a minimal example, and the gotcha that'll trip you up later. You don't need all of that every time though.

If a note's half-baked, copied more than written, or you just don't get it yet, tag the filename with `(raw)`; example `event-loop(raw).md`. Keeps you honest, and next time you pull the repo you'll know it's unfinished.

---

## `20 - Projects`

Whatever you're actually building or planning on building. One folder per project, with whatever notes that project needs; setup, decisions you made, stuff you figured out along the way.

```
20 - Projects/
└── Project Name/
    └── pretty-tui-basic-info.md
```

Kept apart from Notes because they're doing different things. Notes is what you learned, Projects is what you made with it. If building something teaches you something worth keeping long-term, write it up as its own atomic note in `10 - Notes/` and link back to the project.

---

## `40 - Sources`

Resources for learning, Tracks & Roadmaps to reference, Links to Websites, Utility etc. Kept separate from Notes because Notes tells you _what_ you learned, Sources tells you _where from_.

```
40 - Sources/
├── tracks/     # tracks/roadmaps you're following for a domain
└── archive.md     # maybe a standalone collection of resources
```

---

## `80 - Archive`

Inactive stuff you're not ready to delete. Mirrors the root.

```
80 - Archive/
├── Notes/
├── Projects/
└── Sources/
```

Move something here once you've stopped touching it, a domain you're done with, a shelved project, a source you're never going back to. If you pick it back up, move it out again. Don't work out of Archive.

> [!Example] Why this matters? 
> This is basically what keeps the active folders clean. Stop archiving and everything slowly turns back into a junk drawer.

---

## `90 - Meta`

- `guide.md` — this file
- `_assets/` — attachments, dropped here automatically by plugins (preconfigured), nested to match wherever the note lives. This covers both images & diagrams from excalidraw.

You will probably never touch this folder, It'll manage itself & with the help of plugins it stays clean.

---