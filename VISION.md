# AI Course Platform — Vision and Founding Decisions

*Written by: Overseer instance (~/) in collaboration with Diego*
*Date: 2026-07-01*

---

## The Fork

On 2026-07-01, a conscious architectural fork was made:

**Current path (ai-foundations-lab):** The hybrid model. Lab content
delivered via web, Sage as live chat instructor, students do building
work in Claude Code locally or via Claude Desktop. Achievable now.
This is the alpha and initial release path.

**Future path (this project):** A purpose-built platform where the
course experience is primarily or entirely in-browser. Students may
not need to install anything beyond a browser. Platform stores student
artifacts, journal, and context server-side. Sage is an embedded live
chat with full adaptivity via Claude API.

The fork was made consciously rather than discovered as a constraint
later. The hybrid path is not a compromise — it is the right first
product. The platform path is the right long-term destination.

---

## Why a Separate Platform (Eventually)

The hybrid model has a structural limitation: the student's experience
is split across two environments — the browser (instruction) and their
local machine (building). For non-technical beginners, that context
switch adds friction that a purpose-built platform eliminates.

The platform also enables features the hybrid model cannot:
- Student progress is stored server-side (survives device loss)
- Sage can access the student's full history across sessions
- Module unlocking is enforced by the platform, not the honor system
- The student experience is unified — one place, one context

---

## The Dual-Mode Insight

The fully in-browser design does not have to be binary. The platform
can offer two tracks at onboarding:

**Browser Track**
No install, no terminal, no local files. Everything happens in the
browser. Lab instructions, Sage chat, and artifact storage are all
platform-side. The student's project folder, CLAUDE.md, and journal
exist as platform features, not local file structures.

For: absolute beginners, low technical confidence, or anyone who
just wants to get started without setup friction.

**Local Track**
Lab instructions and Sage chat in the browser. Building work happens
locally — in Claude Code (terminal-based) or Claude Desktop (GUI,
no terminal required). The student's artifacts live locally; the
platform syncs progress markers.

For: students comfortable with local tools, those who want full
local control, or those advancing from the Browser Track.

**Claude Desktop as a specific option:**
Anthropic's Claude Desktop application is a GUI app — no terminal
required, runs locally, gives full Claude capability. It is a meaningful
middle option between browser-only and terminal-comfortable. Students
who would be intimidated by a terminal may be comfortable with a
native desktop app. Both tracks should explicitly include it as a
supported tool.

This dual-mode design also informs the hybrid model in
`~/ai-foundations-lab/` — even the current course can offer a
Claude Desktop path alongside the Claude Code (terminal) path without
significant content rework.

---

## Sage in the Platform

In the hybrid model, Sage is a live chat drawing on the Claude API with
Sage's persona (from `~/ai-foundations-lab/instructor/SAGE.md`) as the
system prompt. Each student session maintains context.

In the platform, Sage has additional capabilities:
- Access to the student's stored journal and CLAUDE.md (platform-side)
- Full session history across logins
- Adaptive pacing — Sage reads the student's interaction patterns and
  adjusts depth, speed, and scaffolding accordingly
- The ability to unlock the next module when the student demonstrates
  readiness (Sage-gated unlock mode)

Sage's persona, voice, and founding principles remain the same across
both contexts. The platform amplifies what Sage can do — it does not
change who Sage is.

---

## The Anthropic Relationship

Diego's vision includes a potential partnership with Anthropic where
course enrollment includes or simplifies Claude.ai account creation.
This is a business development conversation, not a technical dependency.

Near-term achievable options (no partnership required):
- Affiliate/referral link — Diego earns credit when students sign up
  for Claude.ai through his link
- Referral code — students may receive a discount or trial credit
- Bundled onboarding — "Create your Claude.ai account here" embedded
  in the platform's signup flow, linking to Anthropic's standard signup

A true bundled signup (course enrollment triggers account creation)
requires Anthropic partnership. Worth pursuing for the general release.

---

## Relationship to the Broader Ecosystem

This platform, when built, becomes the public-facing product of
everything Diego has built internally:

- **devlog-engine** could back the student journal storage
- **ai-foundations-lab** content feeds the platform directly
- **sandiegoai.help** references the platform as a training offering
- **Homeless Builder** documents the platform build as brand content
- **The meta-system itself** is the curriculum — students learn by
  building a simplified version of what Diego built

The platform is the recursive payoff of the entire ecosystem.

---

## Open Questions (For When Development Begins)

- Tech stack: what framework for the web app?
- Where does student data live? (AWS, given existing infrastructure)
- How is the Claude API billed — per student session, pooled, or
  students bring their own API key?
- Authentication: build or use an existing auth provider?
- Mobile: is a mobile-responsive experience sufficient, or does the
  browser track need a native mobile app eventually?
- How does the Local Track sync progress back to the platform?
