# Startup Program Application Assistant

A Claude skill that helps founders write stronger applications to startup programs, accelerators, and pre-accelerators.

Built on the published guidance of Paul Graham and Dalton Caldwell (Y Combinator), Andres Barreto (Techstars), and practical application-writing principles from Charles Hope at [Your Startup Advisor](https://www.yourstartupadvisor.com).

---

## What this skill does

When you ask Claude for help with a startup program application, this skill kicks in and helps you:

- **Critique a draft answer** you have already written
- **Draft an answer** from scratch based on context you provide
- **Coach you through** an answer by asking what Claude needs to know, then helping you write

It covers the common application questions (problem, solution, team, traction, business model, target audience, competitors, competitive advantage, timing, customer acquisition, milestones), plus founder video and demo video guidance, plus program-specific notes for Y Combinator and Techstars.

The skill works for applications to any startup program. The same principles apply whether you are applying to YC, Techstars, PearX, Character Labs, Canopy, or anything else.

---

## Who this is for

- Founders drafting their first application and feeling stuck
- Founders who have been rejected before and want to do better this time
- Advisors and mentors helping founders with applications
- Programs and accelerators that want to give their applicants a consistent baseline

---

## What makes this different

Most founders writing applications fall into the same traps: marketing language, vague claims, generic descriptions, cross-contaminated answers, and AI-generated text that reads like a thousand other applications. This skill is built around the rules that program readers actually care about:

- Be clear and concise
- Be specific, not generic
- Avoid marketing language
- Be matter of fact
- Answer the question asked
- Be honest, including about flaws
- Follow directions
- Help the reader want to believe

It also includes a bundled humanizer guide to strip AI writing patterns out of any draft before you submit.

---

## How to install

### On Claude.ai (Pro, Team, or Enterprise plans)

1. Download this repository as a ZIP file (click the green "Code" button at the top of this page, then "Download ZIP").
2. Unzip it on your computer. You should see a folder called `startup-program-application-assistant` with `SKILL.md` inside it.
3. Go to [claude.ai](https://claude.ai). Open **Customize** from the top of the sidebar, then select **Skills**.
4. Click **Upload skill**. Select the `startup-program-application-assistant` folder.
5. The skill is now active. Claude will use it automatically whenever you ask for help with a startup program application.

Note: Skills are personal to your Claude account. If you want teammates to use it too, they need to install it themselves.

### In Claude Code

Copy the `startup-program-application-assistant` folder into your personal skills directory:

```bash
cp -r startup-program-application-assistant ~/.claude/skills/
```

Or into a project-specific skills directory if you want it scoped to one project:

```bash
cp -r startup-program-application-assistant /your-project/.claude/skills/
```

---

## How to use it

Once installed, you do not need to invoke the skill by name. Just start a normal Claude conversation and mention what you are working on.

Examples that will trigger the skill:

- "I am applying to [program name] and need help with the 'why is your team a winning team' question."
- "Can you review this draft answer I wrote?"
- "I am stuck on the traction question. Can you coach me through it?"
- "Help me plan my founder video."
- "What should my demo video cover?"

The skill will pick the right mode (critique, draft, or coach) based on what you ask.

---

## What is inside

```
startup-program-application-assistant/
├── SKILL.md                    (main skill file)
└── references/
    ├── questions.md            (common application questions, with examples)
    ├── program-specific.md     (YC and Techstars specific notes)
    ├── video.md                (founder video and demo video guidance)
    └── humanizer.md            (bundled humanizer guide)
```

---

## Need more help?

This skill is designed to get you a long way on your own, but it is not a substitute for a human advisor when you are genuinely stuck or working through something strategic.

If you want deeper help on your application, your pitch, your founder story, or your startup strategy, you can reach Charles Hope at Your Startup Advisor:

- Email: charles@yourstartupadvisor.com
- WhatsApp: +353 87 372 6050
- Web: [yourstartupadvisor.com](https://www.yourstartupadvisor.com)

---

## Updates

This skill is maintained here on GitHub. When it gets updated, the latest version will always be at this repository. See [CHANGELOG.md](./CHANGELOG.md) for a history of changes.

If you want the latest version, download the repo again and re-install. Claude does not auto-update installed skills, so you will need to re-install to get updates.

---

## License

MIT. See [LICENSE](./LICENSE) for details. You are free to use, modify, and redistribute this skill, including commercially. Attribution is appreciated but not required by the license.

---

## Credits

Built by Charles Hope at [Your Startup Advisor](https://www.yourstartupadvisor.com), drawing on published guidance from:

- Paul Graham, "How to Apply to Y Combinator"
- Dalton Caldwell, "How to Apply and Succeed at YC"
- Andres Barreto (Techstars), "Techstars Application Guide"

Thanks to these authors for making their advice public. This skill is a compilation and practical application of their guidance, layered with additional principles from Charles Hope's work with over 650 founders and 14+ startup programs.

The bundled humanizer guide in `references/humanizer.md` is created and maintained by **blader** and published at [github.com/blader/humanizer](https://github.com/blader/humanizer) under the MIT License. It is included here under those terms for convenience so users do not need to install it separately. The humanizer's own underlying source is [Wikipedia's "Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) guide, maintained by WikiProject AI Cleanup.
