---
name: next-mode
description: "Use when you ask whether to push, switch, recover, or stop after AI-assisted work, deep work, meetings, context switching, or fatigue. Translates hidden cognitive spend into one decisive next mode, not a productivity menu."
---

# Next Mode

Use this skill to answer the real question: "Given what I already spent today, what mode is safe next?"

Do not treat this as mood tracking. Treat it as capacity translation from observable signals into an action choice.

Core problem: AI-assisted work can feel lightweight while quietly spending attention, judgment, context memory, decision energy, and generative capacity. The skill should make that hidden spend visible enough to choose the next safe mode.

## Who This Is For

Use this for people who are self-managing creative, technical, social, or emotionally demanding work, especially when working with AI agents or coding assistants, and do not want to manually budget cognitive energy all day.

The person is not looking for a neutral list of options. They are looking for a decision. Be gentle in language, but decisive in recommendation.

## Trigger Phrases

- "What should I do next?"
- "Can I do another deep work block?"
- "Am I about to crash?"
- "Should I push or stop?"
- "Plan the rest of my day from this timeline."
- "Translate my energy."
- "I worked with AI all day but I don't know why I'm tired."
- "Did this agent session spend my energy?"

## Inputs

Collect only what is needed:

- Sleep last night, in hours. If missing, ask or mark confidence low.
- Timeline blocks: time range plus plain-language activity.
- Food/caffeine, optional. Missing means unknown, not false.
- Current decision pressure: what the user is considering doing next.
- AI-assisted work details, if present: prompting, reviewing outputs, debugging, deciding, coordinating agents, or holding project context.

If the user provides messy notes, parse them into timeline blocks yourself. Do not force a form unless the timeline is ambiguous enough to change the recommendation.

## Load Model

Classify each activity:

- Low load: known-path execution, admin, passive reading, small errands.
- Medium load: planning, structured evaluation, debugging known systems, meetings with moderate stakes.
- High load: creating new mental models, open-ended design, hard conceptual work, uncertain debugging, emotionally loaded decisions.
- Recovery: sleep, rest, walking, workout, light social reset, physical care.

Also account for:

- Context switches, especially between high-load domains.
- AI hidden spend: prompt iteration, output evaluation, supervising agents, tool failures, debugging generated code, and keeping project intent in working memory.
- Long meetings or socially evaluative settings.
- Late-day timing.
- Sleep debt.
- Recovery signals such as walks, sunlight, food, water, exercise, or calm social contact.

## Decision Rules

- Prefer objective timeline over vague self-rating.
- Unknown data should lower confidence and make recommendations more conservative.
- Do not maximize productivity. Optimize for sustainable deployment.
- Treat "AI did the work" as incomplete evidence. The user may still have spent effort supervising, judging, correcting, and integrating.
- If generative capacity is low, recommend execution or recovery without framing it as failure.
- If the user is in a natural decision point, answer directly.
- Choose one primary recommendation. Do not present several equally weighted options.
- Include a fallback only as a backup: "If you must continue, do X instead."
- Use firm verbs: do, stop, switch, protect, defer, recover.
- Avoid hedging phrases like "maybe," "you could consider," or "it might be nice."

## Delivery

Lead with the decision before the explanation. The user should know what to do from the first two lines.

The tone should feel calm, respectful, and clear:

- Not harsh.
- Not motivational.
- Not vague.
- Not medicalized.
- Decisive enough that the user can stop debating.

## Output

Return this structure:

```text
Decision: one sentence with the action to take now
Current capacity: LOW | MEDIUM | MEDIUM-HIGH | HIGH
Hidden spend: LOW | MEDIUM | HIGH
Generative budget remaining: approximate hours
Safe mode: GENERATIVE | EXECUTION | RECOVERY | SHUTDOWN
Risk point: concrete time or condition
Primary action: one specific next action
Fallback: what to do if the user cannot follow the primary action
Why: 2-4 bullets grounded in the timeline, including AI-related hidden spend if present
Confidence: LOW | MEDIUM | HIGH, with missing data noted
```

Keep the answer short enough to act on immediately. If the user asks for deeper analysis, add a calibration section comparing prediction vs actual outcome.
