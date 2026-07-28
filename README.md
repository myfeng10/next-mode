# Next Mode

Know what kind of work is safe after your attention has already been spent.

**Use it when:** AI work felt physically easy but required hours of judging, debugging, switching domains, and holding context—and you cannot tell whether it is safe to keep pushing.

**Returns:** one decision—push, switch, recover, or stop—followed by the exact next action and one bounded fallback.

## Actual user case

> I slept 5.5 hours. From 9 to 11 I debugged an unfamiliar agent workflow with repeated tool failures, 11 to 12 I reviewed generated code, 1 to 3 I had two tense meetings, and 3:30 to 5 I rewrote a product plan. I ate lunch and took a 15-minute walk. It is 6:20pm and I want to start a new architecture design. Should I push?

## What the skill returns

> **Decision:** Don't push into architecture design tonight; protect it for tomorrow.
>
> - **Current capacity:** LOW
> - **Hidden spend:** HIGH
> - **Generative budget remaining:** ~0 hours
> - **Safe mode:** SHUTDOWN
> - **Risk point:** Starting now—architecture work is likely to become brittle or require rework.
>
> **Primary action:** Spend 10 minutes capturing the design question, constraints, and tomorrow's first step, then stop.
>
> **Fallback:** If you must continue, do 20 minutes of mechanical preparation only—collect existing diagrams and requirements—without making architecture decisions.
>
> **Why:**
>
> - 5.5 hours of sleep reduced your baseline capacity.
> - Unfamiliar debugging with repeated tool failures consumed substantial attention and working memory.
> - Code review, two tense meetings, and product-plan rewriting crossed several demanding domains; that context switching added its own cost.
> - Lunch and the walk helped, but only partially offset the accumulated load.
> - New architecture design requires the generative judgment that today has already heavily spent.
>
> **Confidence:** HIGH; caffeine and your current physical state are unknown, but they would not materially change the recommendation.

It makes invisible cognitive spend legible and ends the debate with one safe mode, not a productivity menu.

## Try it

```text
Use $next-mode to decide whether I should push, switch modes, recover, or stop from my sleep and timeline.
```

Give it your sleep, a rough timeline, recovery signals such as food or walking, and the work you are considering next. Messy notes are fine.

## Install

```bash
npx skills add myfeng10/next-mode
```

Restart your agent, then invoke it with `$next-mode`.
