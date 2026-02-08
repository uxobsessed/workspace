# How to use this vault

This vault exists so I can capture ideas, learn properly, track project work; without everything becoming a giant unorganized mess. Like all things this solution isn't perfect, If you find this method slowing you down I encourage you to curate your very own customized experience; Since there will never be a one-size-fits-all solution when it comes to hyper-personal things like learning.

**IMPORTANT**
Git doesn't allow me to push empty folders, and adding a hidden `.gitkeep` into folders you will probably never need is redundant (Areas specific to my use-case). So I've only added them to the most basic folders *you could need to get started*.

Also, these README files use traditional markdown links like so,
```
![Text/Usually file name](<inside angled brackets so you dont have to type %20 for spaces in path names>)
```
using the vault path from root so these can be viewed on GitHub as is without needing to be cloned first. <u>But the setting to use Wiki-links has been left turned *on*</u> so you can have a better experience using Obsidian. If you do plan to make a README for your own GitHub version, use similar markdown links in that version.

> [!TIP] 
> First thing to do once you've cloned the Template. 
> Create folders inside `Areas` about things you want to study/learn using this vault. Similarly create a folder with the same name inside `Resources`. [Below I will attach the tree output of my vault to give you an idea of how to shape the vault](#^26bb2f).

*If You're unsure where something goes, put it in `00 - Inbox/` and sort it later.*

> [!NOTE]
> Keep active folders small. When something stops being active, move it to `40 - Archive/` instead of letting it rot in place.

## The folders (brief overview)

`10 - Projects/` is for things You're building. If it has an outcome (ship a tool, finish an app, implement a feature set), it lives here. A project folder is allowed to be messy while You're working, because it’s a workspace. [More on how to work inside the Projects folder & Template](#What%20goes%20in%20a%20Project%20(`10%20-%20Projects`)).

`20 - Areas/` is for tracks you're maintaining over time (no finish line). This is where you track what you're focusing on right now, what “good” looks like, and what you should revisit. It’s not where the actual deep notes live. [More on how to manage an Area](#What%20goes%20in%20an%20Area%20(`20%20-%20Areas`)).

`30 - Resources/` will be the knowledge base: notes in your words, written so future you can get up to speed quickly. This is where “what I learned” lives. For rough, draft like notes which are not yet polished, use a `(raw)` suffix at the end to mark it as so. `Resources/rust/ownership/ownership_model(raw).md`. [More on Resources and how to work inside the folders](#What%20goes%20in%20Resources%20(30%20-%20Resources)).

`40 - Archive/` is for inactive stuff. This keeps the active folders clean. If You're done with a project or something you haven't touched in weeks, move it here (inside the respective nested folder). If you plan to work on something again that was archived, move it back out. [More on Archives](#What%20Archive%20is%20(40%20-%20Archive)).

`90 - Meta/` is the vault’s “operating manual”: [Templates](#Templates%20(presets%20for%20some%20of%20the%20top%20level%20folders)), [MOCs (Maps of Content)](#MOCs%20(Maps%20of%20Content)), and rules for how to run this workspace.

---
## What goes in a Project (`10 - Projects`)

When you get an idea and want to build it, create a folder under the  `10 - Projects/` folder and copy the Project Folder template into it.

Start with `00 - scope` first. If you can’t explain the MVP and what “done” means, you're not ready to plan tasks yet. So, the flow would be:

- `00 - scope` the idea in one paragraph, what problem it solves, MVP criteria.
- `01 - specs` features, constraints, platforms, acceptance criteria.
- `02 - architecture` for deciding how it should work. data model, API sketches, decisions, trade offs etc.
- `03 - tasks` planned tasks for that project to progress, blockers which stopped progression previously, links to sources you plan to use to help with clearing these tasks.
- *OPTIONAL* `04 - links`: For me this will contain links to published content about projects after I've shipped something. For you this could be sources relevant to that project, If contributing to OSS this could be links to that project repo, wiki etc.

## What goes in an Area (`20 - Areas`)

An Area is a “maintenance lane.” It’s where you track how your learning is going, what is yet to be learned and things you plan to revisit and solidify in the near future. you may use it like this:

- `00 - roadmap` a very detailed roadmap, tailored to your needs, your goals and where you want to go with this Area. You may use an LLM to generate if you feel like generic road-maps are cutting it for you (properly defined topics, tasks, something you can follow and actually grow with), go back and forth reiterating unless you're satisfied with the resulting path defined for *this* area and *it's* goals.
- `01 - now` will be your short-term focus (keep it tight. if it becomes a wishlist, it stops being useful).
- `02 - review_queue` is a list of links to the few notes you know you'll forget unless revisited. Things you want to polish up on.

If you stop maintaining an area for a while, move the whole Area folder to `40 - Archive/Areas/`.

> [!CAUTION]
> Make sure you cross-check your "resulting" roadmap multiple times with multiple thinking and reasoning models. Make sure it's up to date, Make sure it actually makes you build stuff and doesn't send you off into tutorial hell.

## What goes in Resources (30 - Resources)

Resources is “learned knowledge” written so that it’s easy to revisit. If it’s unrefined, still put it here, but name it in a way that doesn’t lie to you; like adding a `(raw)` suffix.

A good Resources note usually answers:  
- What question was I trying to answer
- what’s the rule/idea in my words
- what’s a minimal example
- and what’s the one gotcha that *will* bite me later.

This folder is allowed to grow and be messy, Don't be a perfectionist. If you are one, don't follow this template and go build a better workflow because this isn't and won't ever be perfect.

## What Archive is (40 - Archive)

Archive is not a trash can. It’s a parking lot for inactive things from Projects, Areas and Resources. That’s the whole point of the system: active stays visible; inactive gets out of the way.​

I use Archive when:

- A project is done or abandoned.
- An area is paused, I haven't made much progress in a while and don't plan to.
- A set of notes is no longer relevant to what I'm doing right now.

## Templates (presets for some of the top level folders)

Templates live in `90 - Meta/Templates/`. If You're starting a new Project or planning to start learning/working on a new Area; copy the respective folder out and rename it.
```
utkarsh@arch~/D/v/n/9/Templates $ tree
.
├── Area Folder
│   ├── 00 - roadmap.md
│   ├── 01 - now.md
│   └── 02 - review_queue.md
└── Project Folder
    ├── 00 - scope.md
    ├── 01 - specs.md
    ├── 02 - architecture.md
    ├── 03 - tasks.md
    └── 04 - links.md

4 directories, 8 files
```

## MOCs (Maps of Content)

==PENDING!! Under Development==

MOCs live in `90 - Meta/MOCs/`. An MOC is just a curated “entry point” note for a topic: it links to the best Resources notes, active Areas, relevant Projects, and any other unorganized files in your Inbox about a specific topic/Area.

==(WIP)== A template will be included showcasing how one would implement filtering which will locate files with tags if *any one* of the conditions are met. Make sure to mark your files with an appropriate tag like so #help

> [!IMPORTANT]
> Keeping MOCs inside Area or Resources folder is redundant and breaks the flow and purpose of those folders. Whereas Meta is built for navigating the Vault, so *use MOCs to create detailed Map of Contents for your Areas and simply Bookmark them*.
> 
> I've bookmarked this `How to` note so you can easily access it under the bookmarks tab.

---
## How this will work: with various examples

When You're studying and want to take notes: you write in `30 - Resources/`.
When You're building something: you work in `10 - Projects/`.
When you want to keep your learning on track: update `20 - Areas/<Area>/01 - now` and add links to `02 - review_queue`. When something becomes inactive: move it to `40 - Archive/`.

---
## Git (keep it clean)

One commit should represent *one kind of work*. If I studied a topic and also worked on a side project & tracked that, those should usually be separate commits. The goal is to make history readable later, not to "save clicks"

---

# Structure to base your personal Workspace off of: ^26bb2f

```
utkarsh@arch~/D/v/notebook $ tree --gitignore
.
├── 00 - Inbox
├── 10 - Projects
│   ├── Production     # For professional project tracking
│   └── Side Projects  # For more casual, personal projects/internal tools
├── 20 - Areas         # Your areas-of-interest go here
│   ├── DSA
│   ├── Rust
│   └── Web
├── 30 - Resources     # Mirrored, same as Areas/
│   ├── DSA
│   ├── Rust
│   └── Web
├── 40 - Archive     # Archive inactive projects, areas, resources
│   ├── Areas          Mirror of root level folders (keep it nested)
│   ├── Projects
│   └── Resources
├── 90 - Meta
│   ├── _assets       # Attachments go here by default
│   │   ├── diagrams
│   │   └── images    # Automatic nesting for imgs mirroring folder layout
│   │       └── README
│   │           ├── IMG-20260206163250296.png
│   │           ├── IMG-20260206164013920.png
│   │           └── IMG-20260206165129843.png
│   ├── guide.md
│   ├── MOCs          # MOCs for all Areas, Suggested to bookmark
│   └── Templates             # Template for Area & Projects Folders
│       ├── Area Folder
│       │   ├── 00 - roadmap.md
│       │   ├── 01 - now.md
│       │   └── 02 - review_queue.md
│       └── Project Folder
│           ├── 00 - scope.md
│           ├── 01 - specs.md
│           ├── 02 - architecture.md
│           ├── 03 - tasks.md
│           └── 04 - links.md
└── README.md
```
