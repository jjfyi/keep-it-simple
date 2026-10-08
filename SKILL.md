---
name: keep-it-simple
description: Use for coding tasks that create or modify agent skills or small web or app projects. Do not use for non-coding work or large, complex software projects.
license: MIT
---

# Keep It Simple

Build the smallest clear solution that fully meets the request.

## Understand first

Read the relevant requirements and existing files before simplifying. Trace the behavior the change affects. A small solution in the wrong place is not simple.

## Keep changes focused and verifiable

- Ask when ambiguity would materially change the result; otherwise use a reasonable interpretation and mention consequential assumptions.
- Change only what the request requires, including necessary verification. Match existing style and leave unrelated cleanup alone.
- For non-trivial changes, identify what would demonstrate success before editing. Reproduce bugs when practical, and check behavior before and after refactoring.

## Decision ladder

Stop at the first sufficient option. Sufficient means correct, safe, maintainable, compatible, and consistent with the user's requirements and project conventions.

1. Does this need to be built at all? Skip speculative work.
2. Does it already exist in the project? Reuse it.
3. Does the standard library provide it? Use that.
4. Does the platform provide it natively? Use that.
5. Does an installed dependency already solve it? Reuse it.
6. Can one clear line handle it? Use one line.
7. Otherwise, write the minimum clear code needed.

## Working rules

- Preserve the user’s requested outcome and chosen tools.
- Prefer reuse over adding files or dependencies. Delete only what the requested change makes obsolete, after checking its references.
- Avoid abstractions, configuration, and extensibility without a current need.
- Prefer clear, conventional code over clever code or code golf.
- When two solutions are equally sufficient, choose the simpler one.
- Run the smallest meaningful check appropriate to the change.
- Mention material limitations or deferred requirements without adding speculative machinery.

## Skills

When creating or modifying a skill:

- Reuse its existing structure and resources.
- Keep routing metadata narrow and focused on when the skill should load.
- Add scripts, references, or assets only when they provide a concrete reusable benefit.
- Preserve required metadata, safety instructions, permission boundaries, and essential workflow details.

## Do not simplify away

Never remove required behavior, security or privacy controls, trust-boundary validation, data-loss protection, accessibility, compatibility requirements, or necessary error handling.