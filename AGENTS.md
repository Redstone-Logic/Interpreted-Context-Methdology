# Interpreted-Context-Methdology

ICM is a framework for building structured, multi-stage AI workflows out of markdown files and folder conventions. Each workbench gives AI agents the right context at each stage of a task, and gives humans clear edit surfaces between stages.

## Folder Map

```
model-workbench-protocol/
├── AGENTS.md                          (you are here)
├── README.md                          (project overview)
├── LICENSE
├── _core/                             (shared conventions and templates)
│   ├── CONVENTIONS.md                 (source of truth for all patterns)
│   ├── placeholder-syntax.md          (how {{VARIABLES}} work)
│   └── templates/                     (blank starting points for new workbenches)
└── workbenches/
    ├── script-to-animation/           (content idea -> animated video)
    ├── course-deck-production/        (unstructured material -> course PowerPoints)
    └── workbench-builder/             (builds new ICM workbenches)
```

## Routing

| You want to... | Go to |
|-----------------|-------|
| Create content with script-to-animation | `workbenches/script-to-animation/AGENTS.md` |
| Build course slide decks from source material | `workbenches/course-deck-production/AGENTS.md` |
| Build a new workbench for any domain | `workbenches/workbench-builder/AGENTS.md` |
| Read the full ICM specification | `_core/CONVENTIONS.md` |
| Understand the placeholder system | `_core/placeholder-syntax.md` |
| Use a template for a new workbench | `_core/templates/` |

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run onboarding in whatever workbench you are in |
| `status` | Show pipeline completion for the current workbench |

## How It Works

Each workbench is self-contained with its own AGENTS.md. Navigate into a workbench folder and that workbench's AGENTS.md takes over. You do not need to read this root file once you are inside a workbench.
