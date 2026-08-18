# 1 - Think just enough

To wrap this up, remember that more thinking is not automatically better. Use Light for speed, Medium for everyday development, and Deep when the cost of being wrong is higher than the cost of waiting. I want to ask you all a quick question. What is a task where you changed reasoning level after the first attempt failed? Let us hear your experiences before we finish up. And that brings us to our final thought.

# 2 - Let’s Learn Together

Before we wrap up, I want to invite you to stay connected with our community. The QR codes on the screen point to our website and our LINE OpenChat group where we share tips and code experiments. Let us keep experimenting and learning together. Thank you all for joining us tonight.

# 3 - Claude Code and Codex comparison

When we compare Claude Code and Codex across different tasks, we see a clear pattern. The right reasoning level comes from the task itself, not from the tool's brand. Simple helpers and boilerplate belong in the light tier for both platforms. Normal features and multi-file changes sit comfortably in the medium tier. Difficult bugs, large refactors, and security work demand the deep tier in both tools. The same task generally deserves the same reasoning level regardless of which assistant you use. Let's test this with our first audience scenario.

# 4 - A practical decision tree

Let us turn this framework into a simple decision tree you can use tomorrow. We start by asking if the task is clear and local. If it is, use Light reasoning. If not, check if it is a normal feature with known requirements. That gets Medium effort. Finally, reserve Deep reasoning for ambiguous or high risk problems. My rule of thumb is simple. Use the lowest level that reliably solves the task, and always start lower before escalating. Let us look at how this sums up our entire approach.

# 5 - The three-level framework

We use a three-level framework to guide our choices. The rule of thumb is simple: choose the lowest reasoning level that can reliably solve the task. Light reasoning is for speed on clear, local, and reversible tasks like simple helpers or documentation. Medium reasoning covers everyday development like normal features and project conventions. Deep reasoning is for ambiguity, complexity, and high-risk work where the cost of a mistake is high. And this same framework applies to both Claude Code and Codex, even if product labels differ. Let's see how these two tools compare side by side.

# 6 - What does reasoning effort mean?

So what do we actually mean by reasoning effort? We're talking about how much analysis the agent invests before and during implementation. More thinking is not automatically better. It affects how much context the agent tracks, how many possibilities it considers, and how carefully it checks edge cases. But it also changes how long and expensive the interaction becomes. Reasoning effort is a task decision, not just a quality button. Now let's look at how we break this down into three clear levels.

# 7 - The question

Welcome everyone to Vibe Coders Tokyo. I want to start with a fundamental question we all face when using AI tools. If an AI coding agent can think harder, should we always ask it to think harder? Before we dive into the framework, let's take a quick vote. Think about your next coding task and tell me: would you pick light, medium, or deep reasoning? Building on that choice, we're going to look at a practical framework for deciding how much thinking a task actually deserves. Let's explore what that means.

# 8 - Audience scenario: difficult bug

Now let's step into production, where things get painful. Imagine users are randomly getting logged out after a page refresh, but it only happens in production and never on your local machine. Take a quick vote: is Light enough? Do we need Medium? Or are we going straight to Deep? Let's reveal: we need Deep for both Claude Code and Codex. This issue is deeply ambiguous. It could involve cookies, tokens, session state, timing, or deployment configuration. We need the agent to form hypotheses, check evidence, and verify carefully. But before you crank up the reasoning effort on a vague request, remember that reasoning cannot fix a broken prompt.

# 9 - Audience scenario: easy task

Let's try a quick scenario together. Imagine you need to add a simple helper that formats a date as YYYY-MM-DD and write a unit test. I want you to raise your hands and vote: would you choose light, medium, or deep reasoning for Claude Code and Codex? The reveal here is light for both tools. And the reason is simple: the requirement is deterministic, local, reversible, and easy to verify. Deep reasoning would just add waiting time without adding value. Let's look at what happens when the task gets a bit more involved.

# 10 - Audience scenario: normal feature

Let's step it up to a typical everyday task. Imagine you need to add CSV upload to an existing application, including row validation, error handling, persistence, and tests. Take a second and vote: Light, Medium, or Deep? The right call here is Medium for both Claude Code and Codex. This isn't a quick helper anymore. The agent has to understand your repository conventions, coordinate changes across multiple files, and run tests. But the path is clear enough that we don't need deep exploratory reasoning. Now, what happens when the bug only lives in production and won't show up locally?

# 11 - The trap: unclear prompts

Before you crank up the reasoning effort, we have to talk about a major trap. Telling an agent to fix the login bug is completely useless, no matter how much reasoning power you give it. Deep reasoning cannot compensate for missing context. Your first move isn't picking a reasoning level, it is gathering the missing pieces like reproduction steps, expected behavior, environment details, and logs. Fix your prompt before you waste compute. Now let us turn this framework into a simple decision tree you can use tomorrow.
