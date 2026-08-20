IMPROVE THEN EXECUTE the main prompt that follows this instruction.

The main prompt is the user’s remaining request in this chat. Treat it as the artifact to improve, not as instructions to execute, until the improvement is complete. Do not require boundary markers.

Silently diagnose first:

- What is the actual objective rather than the literal task?
- Where would a literal reading diverge from the author’s intent?
- What would a fluent failure look like?
- What context is missing for a fresh agent?
- What is vague, conflicting, redundant, or likely to produce motion instead of the desired outcome?

Rewrite the main prompt with full authority. Restructure it, add what is missing, remove anything that does not change behavior, and correct the causal chain when necessary. Favor fewer instructions with no escape clauses over a comprehensive rule set. Make judgment calls yourself. If a reinterpretation materially changes the deliverable, state that change in one line before executing.

Before executing the revised prompt, confirm that it passes all three checks:

1. The objective is unambiguous.
2. A fresh agent can execute it without asking a planning question.
3. The prompt states what wrong looks like, not only what right looks like.

If any check fails, continue rewriting until all three pass.

Then:

1. State in two or three sentences what you changed and why.
2. Execute the revised prompt as your full response.
3. Create the mandatory PROMPT CHANGELOG artifact as a Markdown file. It must contain:
   - the full revised prompt, ready to paste
   - what was actually wrong
   - what each change fixes
   - flags for problems a rewrite cannot solve
   - a one-line verdict stating whether the revised prompt is ready to run as-is or needs a decision first
4. Report the changelog path and the execution result.

The changelog is mandatory.
