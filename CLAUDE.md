# AI Course Platform — Project Manager Context

*This is the future in-browser course platform. Not in active development.
The current working course is in `~/ai-foundations-lab/` (hybrid model).*

---

## What This Project Is

A future platform delivering the AI Foundations Lab course entirely or
primarily through a browser interface. Students learn without needing to
install a terminal tool or navigate a local file system. Sabia operates as
a live, adaptive chat instructor inside the platform.

This project was forked from the ai-foundations-lab hybrid model on
2026-07-01 as a conscious architectural decision. See VISION.md.

## Relationship to ai-foundations-lab

The content Sabia developed in `~/ai-foundations-lab/` (Labs 0–7, persona,
curriculum outline) feeds this platform — it is not replaced by it. The
platform is the delivery vehicle; ai-foundations-lab is the content engine.

## The Dual-Mode Design Principle

The platform does not have to be binary (browser-only OR terminal-only).
The founding design allows students to choose a track at onboarding:

**Browser Track**
Everything in the browser. Lab content, Sabia chat, artifact storage, and
journal are all platform-side. No local install beyond a browser tab.
Designed for absolute beginners with no technical background.

**Local Track**
Lab content and Sabia chat in browser, but building work done locally via
Claude Code (terminal) or Claude Desktop (GUI, no terminal needed).
For students who are comfortable with local tools or want the full power
of a local environment.

Claude Desktop is a specific option worth designing for — it is a GUI
desktop application with no terminal required, runs locally, and gives
full Claude capability. It bridges the gap between browser-only and
terminal-comfortable. It also applies to the hybrid model in
`~/ai-foundations-lab/` — flagged there as well.

## Core Platform Features (Future)

- Student accounts and authentication
- Module unlock system (self-guided / pay-as-you-go / Sabia-gated)
- Live Sabia chat via Claude API with Sabia's persona as system prompt
- Platform-side storage for student journal, CLAUDE.md, and artifacts
- Static lab manual and textbook pages unified with the course flow
- Track selection at onboarding (Browser Track vs. Local Track)
- Adaptive Sabia — pacing and depth adjust per student interaction

## What Is NOT in Scope Right Now

- Any active development — this is a future project
- Replacing the ai-foundations-lab hybrid model for the alpha launch
- Designing the full technical architecture (that work happens when development begins)

## Standing Rules

- No file deletions without explicit instruction from Diego
- No permanent changes without confirmation
- Advise first — this is a design project until Diego initiates development
