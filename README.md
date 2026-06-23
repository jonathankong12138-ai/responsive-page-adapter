# Responsive Page Adapter

A Codex skill for responsive web adaptation and repair.

Its core principle is:

> 先同源，再重排，最后美化。

The desktop implementation or existing canonical design remains the single source of truth for content, interaction, state, validation, and accessibility meaning. Mobile is a responsive projection of the same experience, not a second page.

## What It Helps With

- Desktop-to-mobile page adaptation
- Mobile-only layout bugs
- Tablet breakpoint repair
- Figma or screenshot-to-responsive implementation review
- Mobile-only DOM and duplicated markup governance
- Horizontal scrolling, text overlap, media overflow, and sticky layout failures
- CSS media query and specificity conflicts
- Non-unified interaction state across responsive variants
- Multi-breakpoint validation before handoff

## Install

Clone or copy this folder into your Codex skills directory:

```bash
git clone https://github.com/<owner>/responsive-page-adapter.git ~/.codex/skills/responsive-page-adapter
```

If you already have the folder locally, copy or sync it into:

```text
~/.codex/skills/responsive-page-adapter
```

Codex can then discover the skill from its `SKILL.md` frontmatter. The user does not need to use a fixed prompt; the skill description is written to trigger for responsive adaptation, mobile bugs, breakpoint issues, duplicated mobile DOM, media query conflicts, and related web layout work.

## Contents

```text
responsive-page-adapter/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
├── scripts/
│   └── validate_skill.py
└── .github/
    └── workflows/
        └── validate.yml
```

## Validate

Run the bundled no-dependency validator:

```bash
python3 scripts/validate_skill.py .
```

If you have Codex's `skill-creator` skill available locally, you can also run its validator:

```bash
python3 ~/.codex/skills/.system/skill-creator/scripts/quick_validate.py ~/.codex/skills/responsive-page-adapter
```

## License

No license file is included yet. Choose a license before publishing publicly if you want others to reuse or contribute under explicit terms.
