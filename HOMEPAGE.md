# Decibel Systems — Plugin Ecosystem for Claude Code

Build this as a single-page marketing site. Clean, dark, developer-focused. Think Vercel/Linear aesthetic — not corporate, not playful.

## Brand

- **Name:** Decibel Systems
- **Tagline:** "Composable intelligence for Claude Code"
- **Colors:** Dark zinc backgrounds (#09090B base, #18181B cards), Decibel Red (#FF3B30) as functional accent only, white text
- **Typography:** Inter for body, SF Mono or JetBrains Mono for code blocks
- **Tone:** Precise, craft-aware, no fluff

## Hero Section

**Headline:** Composable plugins for Claude Code agents

**Subhead:** Tools. Homebase. Peers. Superpowers. Four independent packages that give your Claude Code instances intelligence, identity, coordination, and workflow power.

**CTA:** `Get Started` button linking to #install

**Code block preview:**
```
/plugin marketplace add decibelsystems/marketplace
/plugin install tools@decibelsystems
/plugin install homebase@decibelsystems
/plugin install peers@decibelsystems
/plugin install superpowers@decibelsystems
```

## Package Cards Section

**Section title:** The Stack

Four cards. Top row: Tools (full width or prominent). Bottom row: Homebase, Peers, Superpowers side by side. Each card has an icon area, title, one-liner, and bullet list.

### Card 0: Tools
**Subtitle:** The MCP server, auto-wired
**Description:** 26 facade tools across 20 domains — work tracking, architecture, design, git forensics, coordination, and more. One plugin install, zero manual config.

- Sentinel (issues, epics, ADRs, project health)
- Architect (system design decisions)
- Oracle (portfolio summaries, project context)
- Designer (critiques, token audits, lateral sessions)
- Learnings, Git, Coordinator, Guardian, and 12 more domains
- Auto-connects via `.mcp.json` — just install and go

### Card 1: Homebase
**Subtitle:** Branch identity and protocol
**Description:** Defines what a Decibel branch IS. Conventions, project detection, tool priority, and a discovery contract that lets plugins find each other.

- Tool priority rules (Decibel MCP > skills > built-ins)
- `.decibel/` directory contract
- Project capability manifests
- Integration hooks for cross-package composability
- Verification-before-completion skill

### Card 2: Peers
**Subtitle:** Agent specialization and coordination
**Description:** Spin up Claude Code instances as specialist reviewers. Designer, architect, debugger — each with structured identity, discovery, and handoff protocols.

- Peer identity schema with capability tags
- Structured review artifact format
- Handoff protocol with offline queuing
- 4 specialist role templates (designer, reviewer, architect, debugger)
- Session-start hook for automatic peer announcement

### Card 3: Superpowers
**Subtitle:** Workflow remix with sentinel tracking
**Description:** Fork of superpowers by Jesse Vincent, refined with sentinel-powered project intelligence. Your planning, debugging, and review become project-aware.

- Sentinel-driven planning (issues, ADRs, epics from brainstorming)
- Sentinel-driven debugging (bugs tracked through full lifecycle)
- Sentinel-driven review (findings escalate to tracked issues)
- Project health checks before claiming done
- All 14 upstream superpowers skills included
- Graceful degradation without MCP tools

## Philosophy Section

**Section title:** Design Principles

Use a minimal two-column layout. Left column: principle name. Right column: one sentence.

| Principle | Description |
|-----------|-------------|
| **Composable, not coupled** | Every package works alone. Install any combination. No dependencies between them. |
| **Protocol over opinion** | Homebase defines where things live, not what you believe. Your branch, your rules. |
| **Graceful degradation** | Missing a package? Skills fall back cleanly. No silent failures — always visible logging. |
| **Upstream compatible** | Superpowers stays mergeable with the original. Your refinements layer on top, never fork away. |

## How It Works Section

**Section title:** How the pieces fit

Visual diagram or stepped layout showing:

```
Tools wires up the MCP server
    ↓
Homebase gives a branch its shape
    ↓
Peers gives it specialist coordination
    ↓
Superpowers gives it optional workflow juice
    ↓
Marketplace makes it discoverable
```

Short paragraph: "Each layer is independent. Install Tools and you get 26 MCP tools instantly. Add Homebase for conventions and identity. Add Peers and specialists can find each other. Add Superpowers and your workflows become sentinel-tracked. The marketplace is just an index — each package owns its own manifest."

## Peers Deep Dive Section

**Section title:** Specialist Peers

**Subhead:** Spin up a Claude as a design reviewer, code reviewer, architect, or debugger. It announces itself, other Claudes find it, and they coordinate through structured protocols.

Show a terminal-style mockup of a peer interaction:

```
# Terminal 1 — Designer Peer
$ cd designer-peer && claude
> Setting summary: "Decibel Designer — design system reviewer"
> Checking messages... 1 pending request

# Terminal 2 — Your working session
> list_peers → Found: designer-peer (design-review, token-audit)
> send_message → "Review the card layout in deck-web/src/components/CardGrid.tsx"

# Terminal 1 — Designer responds
> Finding: 8px rhythm broken at line 42 — gap-3 (12px) should be gap-2 (8px)
> Finding: Using hardcoded #18181B instead of token/surface-raised
> Summary: 2 issues, both fixable in place
```

## Install Section

**Section title:** Get Started
**id:** install

```bash
# Add the Decibel marketplace (one time)
/plugin marketplace add decibelsystems/marketplace

# Install what you need — any combination works
/plugin install tools@decibelsystems
/plugin install homebase@decibelsystems
/plugin install peers@decibelsystems
/plugin install superpowers@decibelsystems
```

**Note beneath:** "Requires Claude Code CLI. All plugins are MIT licensed."

## Footer

- **Links:** GitHub (github.com/decibelsystems) | Marketplace repo | Tools | Homebase | Peers | Superpowers
- **Credit line:** "Superpowers built on [superpowers](https://github.com/obra/superpowers) by Jesse Vincent"
- **Copyright:** 2026 Decibel Systems. MIT License.

## Technical Notes for Replit

- Single page, no routing needed
- Dark mode only — no light mode toggle
- Responsive: cards stack on mobile
- No JavaScript frameworks required — static HTML/CSS is fine, or use whatever is fastest
- Code blocks should use syntax highlighting with a dark theme
- Smooth scroll to #install from hero CTA
- No analytics, no cookies, no tracking
- Host-ready: should work on any static host (Vercel, Netlify, GitHub Pages, Replit)
