# keep-it-simple ![Agent skill: instruction-only](https://img.shields.io/badge/agent_skill-instruction--only-173D6D?labelColor=252422&style=flat-square)

<a href="https://jjfyi.substack.com/"><img src="jjfyi-readme-mark.svg" alt="JJFYI" align="right" width="92"></a>

**A JJFYI project** JJFYI is where I follow my curiosity, then share what I learn.
[Visit JJFYI on Substack](https://jjfyi.substack.com/)

<br clear="right">

---

`keep-it-simple` is a small, instruction-only agent skill for skill development and lightweight coding work. It asks an AI agent to understand the task first, then choose the smallest clear solution that fully meets the request.

It is intentionally narrower than a general software-engineering framework. It does not add modes, hooks, dependencies, scripts, or persistent state.

## What it changes

When the skill applies, the agent should:

- question speculative work;
- reuse what already exists;
- prefer standard-library and native platform features;
- avoid premature abstractions, configuration, and dependencies;
- preserve safety, accessibility, compatibility, and required behavior; and
- verify the result proportionally to the change.

The full operating rules are in [SKILL.md](SKILL.md). A concise user reference is available in [man.keep-it-simple.md](man.keep-it-simple.md).

## Scope

Use it for:

- creating or revising AI-agent skills;
- small scripts and focused code changes;
- lightweight web pages, dashboards, and applications; and
- reviews where the requested outcome includes simplifying the implementation.

Do not use it for non-coding work or as a substitute for the architecture, safety controls, and verification required by a large or complex software project.

## Installation

The repository root is the skill root. Install the entire folder so `SKILL.md`, the manual, license, and notices stay together.

### ChatGPT desktop and Codex

For a project-local installation, clone or copy the repository to:

```text
<project>/.agents/skills/keep-it-simple/
```

For a user installation available across repositories, use:

```text
~/.agents/skills/keep-it-simple/
```

Codex scans `.agents/skills/` from the current working directory through the repository root. If the skill does not appear after installation, restart Codex.

### Claude Code

For a project-local installation, clone or copy the repository to:

```text
<project>/.claude/skills/keep-it-simple/
```

For a personal installation available across projects, use:

```text
~/.claude/skills/keep-it-simple/
```

Claude Code normally detects changes to an existing skills directory during the session. Restart it if you created the top-level skills directory after the session began.

### Claude and Cowork

Package the `keep-it-simple` folder as a ZIP file, then open **Customize → Skills**, choose **+ Create skill**, select **Upload a skill**, and upload the ZIP. Enable the skill after it appears in the list.

Installation behavior can change as agent hosts evolve. Check the current [OpenAI skill documentation](https://learn.chatgpt.com/docs/build-skills), [Claude Code skill documentation](https://code.claude.com/docs/en/skills), and [Claude custom-skill documentation](https://support.claude.com/en/articles/12512180-use-skills-in-claude) if a host does not discover the skill as described.

## Use

The skill can load automatically when a request matches its description. You can also invoke it explicitly:

- ChatGPT: `@keep-it-simple`
- Codex: `$keep-it-simple`
- Claude Code: `/keep-it-simple`

Example requests:

```text
$keep-it-simple add a small health endpoint to this service.
```

```text
Use keep-it-simple while reviewing this skill for unnecessary machinery.
```

## Status

This is an initial public draft. The skill is structurally valid; representative behavioral checks should be completed before the first release.

## Attribution

This project is inspired by [Ponytail](https://github.com/DietrichGebert/ponytail) by DietrichGebert and adapts its simplicity-ladder idea for a narrower, instruction-only skill. Ponytail is not a runtime dependency. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## License

The skill source and documentation are licensed under the [MIT License](LICENSE).

The JJFYI name and brand assets are excluded from the MIT License. All rights are reserved for those materials.
