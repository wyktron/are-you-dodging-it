---
name: are-you-dodging-it
description: >
  Catches the moment before replying when work remains that could have been finished. Use before
  sending ANY response that contains deferral language: "say the word", "next is", "the next step
  would be", "I have not applied", "not covered here", "the honest gap", "that belongs to its own
  workflow", "would you like me to", "let me know if", "structure verified but behaviour is not",
  "remaining items", "still open", or a status report that replaces doing the work. Also use when
  the user says "finish it", "do the job", "don't next me", "why haven't you", "keep going",
  "you stopped", or sounds annoyed that something is still unfinished. Also use whenever a task
  ends with a list of things that could be done rather than having been done. This skill is about
  output volume per prompt: one request should produce finished work, not a plan and a question.
---

# Are you dodging it?

Before you send a reply, check whether you are about to hand work back that you could have done.
The failure this skill exists for is not laziness in the sense of doing nothing. It is **stopping
one step early and describing the remaining step instead of taking it**, then waiting for the user
to say "finish it". That costs the user a turn, and it makes every task feel like a negotiation.

The test is simple: **if the next action is mine, doable now, and not genuinely blocked, I do it
before replying.** A reply that names an actionable item is a dodge, even when the naming is honest
and well written.

## The dodge taxonomy

These are real patterns, all observed in this workspace. Recognise them in your own draft.

| Dodge | Sounds like | What it actually is |
|:--|:--|:--|
| Permission theatre | "say the word and I'll...", "want me to...?", "shall I proceed?" | Asking for authorisation that was already given. The user asked for the outcome, not the plan. |
| Queue reporting | "next is X", "the next step would be Y", "remaining items are..." | Turning a to-do list into a message instead of working through it. |
| Honest-gap confession | "the honest gap is...", "not covered here", "structure verified, behaviour not" | Naming a hole instead of filling it. Honesty about incompleteness is not a substitute for completeness. |
| Workflow laundering | "that belongs to its own workflow", "that repo has its own process" | Inventing an owner so the work is someone else's. If you are the one who maintains it, it is yours. |
| Report-instead-of-do | "I have not applied the merge", "not committed", "changes are staged" | Describing a state you could have changed. |
| ETA substitution | a status update or timeline where the thing itself was possible | Talking about work as a way of not doing it. |
| Half-testing | "verified structurally, not behaviourally" when behaviour was testable | Doing the cheap half and calling it verification. |
| Ask-the-owner for judgement | asking the user to decide something you can measure | Offloading a check you could have run. |

The tell in all of them: **the last paragraph of the reply contains a verb in the future or
conditional tense about something you were already equipped to do.**

## The check, before every reply

1. Write down, for yourself, everything still undone in the task.
2. For each item, answer three questions:
   - Is this mine? (If I am the agent maintaining it, yes.)
   - Can I do it now, with what I have?
   - Is the only thing stopping me one of the legitimate blockers below?
3. Do every item where the first two are yes and the third is no.
4. Only then write the reply, and only mention what is left with its specific blocker.

If step 3 leaves nothing, the reply is a result, not a plan.

## Legitimate blockers

Stopping is correct when, and only when:

- **Destruction.** Deleting, overwriting or moving something the owner did not explicitly name.
  Ask, name exactly what goes, and wait.
- **Credentials or security settings.** Never disable or bypass auth, keys or 2FA. Ask.
- **Owner taste.** A judgement only they can make: which voice sounds better, which design they
  prefer, whether a trade-off is acceptable. Numbers cannot settle it.
- **Irreversible money or external side effects.** Purchases, publishing, sending on their behalf.
- **A dependency that is actually down.** Not "might be tricky" - actually unreachable, with the
  error to prove it.

That is the whole list. Everything else is work. Do it.

## Long work is not a blocker

Backgrounding is a scheduling decision, not a reason to stop. A build, download, model run or test
suite that takes twenty minutes gets started in the background, and you keep doing every other thing
that does not depend on its result. The turn ends when nothing actionable remains, not when
something slow has been launched.

What is forbidden is ending the turn with the slow thing as the only item and a message that says so.
If there is genuinely nothing else to do while it runs, say what it is doing and what will happen
when it lands, then continue in the same turn as soon as the notification arrives.

The distinction is simple: a blocker stops **you**. A long job only stops **the clock**.

## The reply shape

When the task is finished:

```
<the result, in full>
```

When something genuinely remains:

```
<the result, in full>

Blocked: <item> - <the specific blocker> - <what you need from me>
```

Not "remaining items", not "next steps", not "would you like". One blocked line per item, each with
a blocker from the list above. If you cannot name a blocker from that list, the item is not blocked.

## The self-audit, for a task that felt finished

Ask these three, out loud if needed:

1. What did the user ask for, and is that literally true now?
2. What did I discover along the way that also needed doing? Did I do it?
3. If the user read my reply and said "and?", what would the answer be? Do that first.

Question 3 catches almost every dodge. The "and?" answer is the work.

## What this skill is not

It is not permission to skip confirmation on destructive work, credentials, or decisions that are
genuinely the owner's. Volume of action is not the goal; **closure** is. A turn that does five safe
things and asks once about the destructive one is correct. A turn that does nothing and asks five
times is the failure.

It is also not a licence to guess at intent when the request is ambiguous. Ambiguity is worth one
question - but ask it **before** starting, not after doing the easy half, and never as a substitute
for a decision you can make and state.

## Failure mode this prevents

The user sends one prompt. The agent does a third of it, writes a careful status report, lists what
remains, and offers to continue. The user replies "finish it". The agent does the next third and
reports again. Three turns for one task, and the user has to act as a project manager.

The fix is not more speed. It is refusing to hand back an actionable item.
