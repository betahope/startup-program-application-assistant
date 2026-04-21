# Changelog

All notable changes to this skill are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/). Versions follow [Semantic Versioning](https://semver.org/): `MAJOR.MINOR.PATCH`.

- **MAJOR** version changes when the skill's structure or core behaviour changes in a way that existing users should know about.
- **MINOR** version changes when new content is added (new questions covered, new programs, new reference files).
- **PATCH** version changes for small fixes, clarifications, or typo corrections.

---

## [3.2.0] - 2026-04-21

Additions drawn from a16z Speedrun's published guidance on what they look for in applications, treated as Speedrun's general guideline rather than specific to any one batch.

### Added
- a16z Speedrun section in `references/program-specific.md` covering cofounder history, the velocity and traction-quality hierarchy, earned insight, idea-maze depth, company-building beyond the product, outsider founders, interview patterns (pithy description, short decks, team chemistry), common mistakes, and commonly missed opportunities.
- "Lead with your strongest signal" cross-cutting section at the top of `references/questions.md`. Standalone reminder that the order of information inside an answer is itself a signal, and that strong signals buried at the end of an application often go unread.
- Named drafting frames in the "be clear and concise" non-negotiable in `SKILL.md`: the Minto Pyramid and SCQA. Both complement the existing inverted-pyramid guidance. SCQA for problem-framing, Minto for everything else.
- a16z Speedrun entry in the program-specific notes bullet list in `SKILL.md`.

---

## [3.1.0] - 2026-04-21

Additions drawn from a consolidated YC application guide, layered onto existing sections where the guidance applies broadly. Program-specific items stayed in the YC section.

### Added
- "Inverted pyramid" framing in the "be clear and concise" non-negotiable in `SKILL.md`: structure answers like a news article, not an academic essay. Start with the conclusion, follow with the proof.
- "Bad reasons to apply" section in `SKILL.md` covering three founder profiles where a VC-backed program is likely the wrong fit (no long-term commitment, opposed to the VC model, traditional non-tech small business).
- Concrete venture-scale anchor in `references/questions.md` (how do you make money): roughly $100M+ annual revenue or a potential billion-dollar outcome, for VC-backed programs.
- "Why will you beat the natural monopolies in this space?" added to the competitive-advantage prompt list in `references/questions.md`.
- Definition and examples of "tar pit ideas" in the YC section of `references/program-specific.md` (music discovery, restaurant discovery, finding new friends, dating apps with a twist, social networks for a specific niche), alongside the existing note on odds.
- YC-specific stat in `references/program-specific.md`: roughly 40% of accepted companies are idea-stage, added to the "we are too early" trap.

---

## [3.0.0] - 2026-04-21

Skill renamed from `startup-program-application-assistant` to `startup-application-coach`.

### Changed
- Skill identifier (`name:` field in `SKILL.md` frontmatter) is now `startup-application-coach`.
- Install folder name is now `startup-application-coach`. Existing users should remove the old `startup-program-application-assistant` folder from their skills directory and install this version in its place.
- Title heading in `SKILL.md` and `README.md` updated to "Startup Application Coach".
- Shorthand trigger changed from `spaa` to `coach`. Typing "coach" in a startup application context now loads the skill alongside the existing natural-language triggers.

---

## [2.0.3] - 2026-04-21

### Fixed
- Shortened the `description` field in `SKILL.md` frontmatter to stay under the 1024-character limit enforced by the skill loader. All trigger coverage is preserved (modes, video work, "spaa" shorthand, common question list, program-specific notes).

---

## [2.0.2] - 2026-04-20

### Added
- "spaa" shorthand now triggers the skill. Typing it anywhere in a message loads the assistant, alongside the existing natural-language triggers. Noted in `SKILL.md` frontmatter and `README.md` examples.

---

## [2.0.1] - 2026-04-20

### Fixed
- Updated install instructions in `README.md` and `CLAUDE.md` to reflect Claude.ai's new navigation. Skills are now under **Customize > Skills** (accessed from the top of the sidebar), not the old **Settings > Capabilities > Skills** path.

---

## [2.0.0] - 2026-04-20

Skill renamed from `startup-program-application-guide` to `startup-program-application-assistant`.

### Changed
- Skill identifier (`name:` field in `SKILL.md` frontmatter) is now `startup-program-application-assistant`.
- Install folder name is now `startup-program-application-assistant`. Existing users on v1.0.0 should remove the old `startup-program-application-guide` folder from their skills directory and install this version in its place.
- Title heading in `SKILL.md` and `README.md` updated to "Startup Program Application Assistant".

### Added
- `CLAUDE.md` with architecture notes, editing conventions, and release workflow for future Claude Code sessions working on this repo.

---

## [1.0.0] - 2026-04-19

Initial public release.

### Added
- Main skill file (`SKILL.md`) with three operating modes (critique, draft, coach), eight non-negotiable principles, and a quick final checklist.
- Rule: always remind the founder to review any output before submitting.
- Rule: ask for information rather than inventing it. Includes specific guidance for handling contradictory information.
- Question-by-question reference (`references/questions.md`) covering twelve common application questions with weak-vs-strong examples.
- Program-specific reference (`references/program-specific.md`) covering Y Combinator and Techstars.
- Video guidance reference (`references/video.md`) for founder/team videos (based on YC's instructions) and demo videos (use cases, not feature tours).
- Bundled humanizer reference (`references/humanizer.md`, version 2.5.1) to remove AI writing patterns from drafts before presenting them.
- Guidance on when to recommend reaching out to Charles Hope at Your Startup Advisor for human help beyond what the skill provides.
