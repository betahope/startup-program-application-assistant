# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

This repository **is a Claude Skill**, not an application. There is no code, no build, no test runner, no lint. The deliverable is the markdown content itself, which end users install into `~/.claude/skills/` (Claude Code) or upload via Settings > Capabilities > Skills (claude.ai). "Running" the skill means Claude loads `SKILL.md` when a conversation matches the frontmatter `description` trigger.

Practical consequence: when editing files here, treat every change as a content/prompt change that will be read by a future Claude instance mid-conversation with a founder. Precision of wording matters more than it would in code — ambiguous phrasing produces bad behavior in the wild.

## Architecture

Single entry point with on-demand references:

- `SKILL.md` — the only file Claude loads automatically when the skill triggers. YAML frontmatter `name` + `description` determines whether the skill fires; everything in `description` is matched against user intent. Keep triggers broad enough to catch indirect phrasings ("help with my YC application") but specific to startup-program applications.
- `references/questions.md` — loaded by Claude only when the founder is working on a specific application question (problem, solution, team, traction, etc.). Contains weak-vs-strong examples.
- `references/program-specific.md` — loaded when the founder names YC or Techstars. **Do not add speculative content for programs not already covered** — the skill explicitly instructs Claude to say "program-specific patterns for that one are not in the skill" rather than invent guidance.
- `references/video.md` — loaded for founder/team video or demo video work.
- `references/humanizer.md` — vendored from [github.com/blader/humanizer](https://github.com/blader/humanizer) (MIT). Applied to every draft before presenting. Keep the attribution in README.md and the file itself if updating.

The references pattern is load-on-demand to keep the initial skill context small. When adding a new topic, prefer a new reference file + a pointer from `SKILL.md` over inlining into `SKILL.md`.

## Non-negotiable behaviors encoded in the skill

These are rules Claude follows when the skill is active. When editing `SKILL.md`, do not weaken them:

1. **Ask, do not invent.** Never fabricate numbers, customer names, team credentials, dates, market sizes. If information is missing, ask the founder. If two pieces of their information contradict, flag it rather than silently picking one.
2. **Always remind the founder to review.** Every response (critique, draft, coach) ends with one short line telling them to review before submitting. Vary the phrasing; don't stack disclaimers.
3. **Run the humanizer pass on every draft** before presenting. Application readers are unusually good at spotting AI writing tells.
4. **Three modes: critique, draft, coach.** Pick based on the founder's ask. Coach mode is the default when context is thin.
5. **Final checklist** at the bottom of `SKILL.md` must be run on every answer before presenting it.

## Editing conventions

- **Voice.** Matter-of-fact, plain language, no marketing speak. The skill preaches this to founders, so the skill itself must model it. No em dashes, no "not just X but Y" constructs, no inflated three-item lists, no "nestled"/"vibrant"/"transformative". When in doubt, invoke the `humanizer` skill on your own edits.
- **Specificity.** Same rule the skill teaches: if a sentence could describe any skill, rewrite it.
- **No code examples in founder-facing sections.** The audience is non-technical founders drafting applications.

## Versioning and releases

Follows [Keep a Changelog](https://keepachangelog.com/) + SemVer, per `CHANGELOG.md`:

- **MAJOR** — structural or core-behavior changes users should know about.
- **MINOR** — new content (new questions, programs, reference files).
- **PATCH** — fixes, clarifications, typos.

When making a release-worthy change, add a dated entry to `CHANGELOG.md` under the new version heading. Current released version: `1.0.0` (2026-04-19).

## Testing changes

There is no automated test. To verify a change:

1. Install locally: `cp -r . ~/.claude/skills/startup-program-application-assistant/` (or symlink).
2. Start a new Claude Code session and send a prompt that should trigger the skill (e.g. "help me critique my YC problem answer"). Confirm the skill loads and behaves as intended.
3. For reference-file changes, use a prompt that forces that reference to load (e.g. naming Techstars for `program-specific.md`).

## Authoritative sources

Content is grounded in published guidance from Paul Graham + Dalton Caldwell (YC) and Andres Barreto (Techstars), plus Charles Hope's layer at Your Startup Advisor. New guidance should either cite these sources or be clearly flagged as Charles Hope's own principles (see the "Additional guidance layered on top" section of `SKILL.md` for the existing convention).
