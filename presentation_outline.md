# How Much Should Your Coding Agent Think?
## Choosing reasoning effort in Claude Code and Codex

Vibe Coders Tokyo #9 — Models, Models, Models

---

# 1. The question

## If an AI coding agent can think harder, should we always ask it to think harder?

The answer: **No. Match reasoning effort to the task.**

- Light: fast and predictable
- Medium: everyday development
- Deep: ambiguous, complex, or high-risk work

Audience interaction: ask everyone to vote before revealing the framework.

---

# 2. What does “reasoning effort” mean?

Reasoning effort is the amount of analysis the agent invests before and during implementation.

It affects:

- How many possibilities the agent considers
- How much context it tracks
- How carefully it checks edge cases
- How long and expensive the interaction becomes

Important: **more thinking is not automatically better.**

---

# 3. The three-level framework

## Light

Clear, local, reversible tasks. Optimize for speed.

## Medium

Normal feature work. Understand context, make coordinated changes, run tests.

## Deep

Ambiguous, complex, or high-risk tasks. Investigate, compare hypotheses, and verify carefully.

The same framework applies to both Claude Code and Codex; product labels may differ by interface.

---

# 4. The comparison table

| Task | Claude Code / Codex reasoning | Why |
|---|---|---|
| Simple helper or boilerplate | Light / Light | Predictable and easy to verify |
| Documentation or code explanation | Light–Medium / Light–Medium | Needs context, but is usually low risk |
| Unit tests or routine bug fix | Light–Medium / Light–Medium | Clear behavior and quick verification |
| Normal feature implementation | Medium / Medium | Requires project context and conventions |
| Feature across multiple files | Medium–Deep / Medium–Deep | More dependencies and integration risk |
| Complex debugging | Deep / Deep | Multiple hypotheses must be investigated |
| Large refactor | Deep / Deep | Must preserve behavior while changing structure |
| Security, concurrency, or migration | Deep / Deep | Errors are costly and difficult to detect |

---

# 5. Audience scenario #1: easy task

## Scenario

“Add a helper function that formats a date as `YYYY-MM-DD` and write a unit test.”

## Question for the audience

Which reasoning level would you choose for Claude Code? For Codex?

**Vote: Light, Medium, or Deep.**

## Reveal

**Claude Code: Light | Codex: Light**

Why: the requirement is deterministic, local, reversible, and easy to verify.

---

# 6. Audience scenario #2: normal feature

## Scenario

“Add CSV upload to an existing application. Validate rows, show useful errors, store valid records, and add tests.”

## Question for the audience

Which reasoning level would you choose in each tool?

## Reveal

**Claude Code: Medium | Codex: Medium**

Why: the agent must inspect the repository, understand conventions, coordinate several files, and run tests.

---

# 7. Audience scenario #3: difficult bug

## Scenario

“Users are randomly logged out after refreshing the page. It happens in production but not locally. Find the root cause and add a regression test.”

## Question for the audience

Is Light enough? Is Medium enough? Or do you need Deep?

## Reveal

**Claude Code: Deep | Codex: Deep**

Why: the issue is ambiguous and may involve cookies, tokens, session state, timing, deployment configuration, or multiple interacting components.

---

# 8. The trap: unclear prompts

## Scenario

“Fix the login bug.”

The correct first step may not be Light, Medium, or Deep.

The correct first step is: **ask for more information.**

A better prompt includes:

- Reproduction steps
- Expected and actual behavior
- Environment details
- Relevant logs
- Acceptance criteria

**Deep reasoning cannot compensate for missing requirements.**

---

# 9. A practical decision tree

```text
Is the task clear, local, and easy to verify?
├── Yes → Light in Claude Code / Light in Codex
└── No
    Is it a normal feature with clear requirements?
    ├── Yes → Medium in Claude Code / Medium in Codex
    └── No
        Is it ambiguous, cross-cutting, or high-risk?
        ├── Yes → Deep in Claude Code / Deep in Codex
        └── No → Start Medium and escalate if needed
```

Use the lowest level that reliably solves the task.

---

# 10. Closing: think just enough

> **Light for speed. Medium for everyday development. Deep when the cost of being wrong is higher than the cost of waiting.**

The comparison is not “which tool is smarter?”

It is:

**Same task → same reasoning question → Claude Code level vs. Codex level → compare the result.**

Discussion prompt: **What is a task where you changed reasoning level after the first attempt failed?**

---

# Speaker notes

Keep the product comparison fair. The exact labels and capabilities can change across Claude Code and Codex interfaces, so present Light, Medium, and Deep as a practical framework rather than claiming that equivalent labels produce identical behavior. The demo should compare the same repository, prompt, acceptance criteria, and verification steps wherever possible.
