# keep-it-simple(7)

## Name

`keep-it-simple` — guide an AI agent toward the smallest clear solution that fully meets a small coding or skill-development request.

## Synopsis

Invoke the skill explicitly or ask for a matching small implementation task:

```text
$keep-it-simple <request>
```

Invocation syntax varies by host: ChatGPT uses `@keep-it-simple`, Codex uses `$keep-it-simple`, and Claude Code uses `/keep-it-simple`.

## Description

The skill changes implementation judgment, not the user's requested outcome. The agent first reads enough requirements and existing files to understand the affected behavior. It then stops at the earliest sufficient option in this order:

1. Do not build speculative work.
2. Reuse an existing project capability.
3. Use the standard library.
4. Use a native platform feature.
5. Reuse an installed dependency.
6. Use one clear line when one line is genuinely sufficient.
7. Otherwise, write the minimum clear implementation.

"Sufficient" includes correctness, safety, maintainability, compatibility, and the user's actual requirements. Fewer lines are not a success when they hide intent or remove necessary behavior.

## When it applies

- Creating or modifying an AI-agent skill.
- Implementing a small script or focused code change.
- Building a lightweight page, dashboard, or application.
- Simplifying an implementation when the request includes making changes.

It does not apply to ordinary prose, general knowledge requests, or large and complex software projects.

## Working rules

- Preserve the requested outcome and chosen tools.
- Prefer reuse and deletion over new machinery.
- Avoid speculative abstractions, configuration, extensibility, and dependencies.
- Prefer clear conventional code over clever compression.
- Choose the safer and more maintainable option when alternatives are equally small.
- Run the smallest meaningful verification appropriate to the impact and uncertainty.
- Report material limitations without building unused upgrade paths.

## Skill-development rules

When the artifact is another skill:

- preserve its existing structure and reusable resources;
- keep routing metadata narrow and discriminating;
- add scripts, references, or assets only for a demonstrated reusable need; and
- retain required metadata, safety rules, permission boundaries, and essential workflow details.

## Guardrails

The skill must not simplify away required behavior, security or privacy controls, trust-boundary validation, data-loss protection, accessibility, compatibility requirements, or necessary error handling.

## Examples

Good matches:

```text
Use keep-it-simple to add CSV export to this small dashboard.
```

```text
Review and simplify this agent skill, then make the justified edits.
```

Poor matches:

```text
Summarize this article.
```

```text
Redesign the architecture of this distributed payments platform.
```

## Files

- `SKILL.md` — authoritative agent instructions.
- `README.md` — installation and user overview.
- `THIRD_PARTY_NOTICES.md` — Ponytail attribution and upstream license.

No configuration, scripts, state, or runtime dependencies are required.

## Attribution

Inspired by [Ponytail](https://github.com/DietrichGebert/ponytail) by DietrichGebert. See `THIRD_PARTY_NOTICES.md`.

## License

MIT. See `LICENSE`.
