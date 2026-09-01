# keep-it-simple ![Agent skill: instruction-only](https://img.shields.io/badge/agent_skill-instruction--only-173D6D?labelColor=252422&style=flat-square)

---

<a href="https://jjfyi.substack.com/"><img src="jjfyi-readme-mark.svg" alt="JJFYI" align="right" width="56"></a>

**A JJFYI project**<br />
JJFYI is where I follow my curiosity, then share what I learn. [Visit JJFYI on Substack](https://jjfyi.substack.com/)
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

The full operating rules will be included in `SKILL.md` when the repository is finalized.

## Status

This is an initial public draft. The complete skill package will replace this preview once the repository treatment is settled.
