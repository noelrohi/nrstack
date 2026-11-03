---
name: run-retro
description: Trigger this if the user says 'run retro'.
metadata:
  credits: Grew out of Matt Pocock's /retro.
---

# Run retro

Suggest changes to the agent's **environment** that would make future runs of this kind of session go better. Text the user wrote with the trigger names the session or asks a question: answer the question first, in two lines, then give the findings. Never ask for clarification: state your reading of the request in one line and go.

Do not edit files, switch branches, or run fixes during the retro. Fixes wait until the user picks them.

1. **Read the session.** Default to the current one. If the user names others, read those logs. If the session is too thin to judge, say so in one line and stop.
2. **Find what cost the most time or caused mistakes**, and the cheapest environment fix for each:
   - **Navigation:** the agent searched long for something; add a pointer in the file it read first.
   - **Checks:** a lint, type, test, hook, or CI job would have caught it. Read the repo's own check scripts and CI first; a check that exists but is unwired is the finding. No guardrail at all is a finding.
   - **Standards:** a mechanical rule becomes a check; a judgement call goes to the reviewer's standards.
   - **Steering files:** an AGENTS.md, CLAUDE.md, or skill line that is wrong, ignored, or a no-op.
   - **Tools:** an expensive or repeated tool call that a script, flag, or skill would cut.
   - **Information:** something the agent needed but could not see, such as logs, alerts, or read access.
3. **Keep only fixes the user controls**, in their repos, skills, and config. Merge findings where one fix covers another. Put the rest in one closing line.

Reply in this shape:
- A small text picture of where the time or mistakes went, such as a timeline or a bar per cause.
- At most five findings, most costly first, numbered, with no table: `1. <what happened, with its cost> → <the fix, naming the file or check>`
- "Reply with the numbers to apply." When applying a fix to a skill or steering file, load `writing-for-agents` first.
