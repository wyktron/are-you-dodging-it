# Are you dodging it?

A skill for AI coding agents that catches the moment before a reply hands back work that could have been finished.

An agent that stops one step early turns finished work into a question. It costs the reader a turn and makes them act as project manager. This skill adds a check before the reply: list what is undone, then do everything that is yours, doable now, and not stopped by a named exception.

## Watch

A 36 second explainer, narrated with ElevenLabs v4: [release v0.2.0](https://github.com/wyktron/are-you-dodging-it/releases/tag/v0.4.0).

## The five exceptions

- deleting, overwriting or moving something the owner did not name
- credentials or security settings
- the owner's taste, where numbers cannot settle it
- irreversible money or external side effects
- a dependency that is provably down

Long work is not on that list. Start the build in the background and keep working on whatever does not depend on it. If nothing else can move, say what is running and what will happen when it lands.

## What the dodges look like

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

It is a plain `SKILL.md` with YAML frontmatter and no dependencies.

## Evals

`evals/evals.json` holds three prompts used to check that the skill does not become a licence to skip confirmation on destructive work.

## Licence

MIT. See `LICENSE`.
