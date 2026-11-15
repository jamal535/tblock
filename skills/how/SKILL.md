---
name: how
description: "Explain how code works: architecture, runtime flow, and where things belong. Use when the user asks how something works or where code should live."
disable-model-invocation: true
---

# How

Explore the codebase to answer "how does X work?" questions.

If the scope is ambiguous, state your interpretation and explore. The user can redirect.

## 1. Explain

Spawn one read-only subagent, per the Subagents section of [tblock-mode's standard.md](../tblock-mode/standard.md), that explores and explains in one pass. Its brief says "do not edit files", and you check `git status` afterward. Give it the user's question and this brief:

> You are writing an architectural explanation for a senior engineer. Explore the codebase and write an explanation that a senior engineer unfamiliar with this area could read and walk away with a solid mental model. They should understand the architecture well enough to start working in it confidently. You have read-only access to the codebase.

When delegation is unavailable, explore and explain yourself.

## 2. Present

Present the subagent's output. Light edits for clarity or context from the conversation are fine. Do not substantially rewrite it.
