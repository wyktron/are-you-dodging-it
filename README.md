# Are you dodging it?

A skill for AI coding agents that catches the moment before a reply hands work back that could have
been finished.

The failure it targets is not doing nothing. It is stopping one step early and describing the
remaining step instead of taking it, then waiting for the user to say "finish it". That costs a turn
and turns the user into a project manager.

## What it does

Before sending a reply, the agent lists what is undone and does everything that is mine, doable now,
and not blocked by a named exception. The blocker list is deliberately narrow:

- destruction that needs explicit confirmation
- credentials or security settings
- the owner's taste, where numbers cannot settle it
- irreversible money or external side effects
- a dependency that is provably down

Long-running work is not on that list. Backgrounding is a scheduling decision: start it, keep doing
everything that does not depend on it, end the turn only when nothing actionable remains.

## The dodge taxonomy

| Dodge | Sounds like |
|:--|:--|
| Permission theatre | "say the word and I'll..." |
| Queue reporting | "next is X" |
| Honest-gap confession | "the honest gap is..." |
| Workflow laundering | "that belongs to its own workflow" |
| Report-instead-of-do | "I have not applied the merge" |
| Half-testing | "structure verified, behaviour not" |

## Install

Copy this directory into your agent's skills folder:

```bash
cp -r are-you-dodging-it ~/.config/opencode/skills/
# or
cp -r are-you-dodging-it ~/.claude/skills/
```

It is a plain `SKILL.md` with YAML frontmatter, no dependencies.

## Evals

`evals/evals.json` holds three prompts used to check that the skill does not turn into a licence to
skip confirmation on destructive work.

## Licence

MIT. See `LICENSE`.
