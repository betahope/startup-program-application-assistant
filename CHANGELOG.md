# Changelog

All notable changes to this skill are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/). Versions follow [Semantic Versioning](https://semver.org/): `MAJOR.MINOR.PATCH`.

- **MAJOR** version changes when the skill's structure or core behaviour changes in a way that existing users should know about.
- **MINOR** version changes when new content is added (new questions covered, new programs, new reference files).
- **PATCH** version changes for small fixes, clarifications, or typo corrections.

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
