# Next Mode

An agent skill that decides whether the user should push, switch modes, recover, or stop.

Most productivity tools give menus. This skill gives one decision from the user's sleep, timeline, meetings, food, context switching, and fatigue signals.

## What It Helps With

- Deciding whether another deep-work block is safe
- Switching from generative work to execution before depletion
- Avoiding late-day crashes
- Giving users with scattered attention one clear next mode

## Install

```bash
npx skills add myfeng10/next-mode
```

Then restart your agent.

## Example Prompt

```text
Use $next-mode to decide whether I should push, switch modes, recover, or stop from my sleep and timeline.
```

## Core Idea

The user is not asking for a productivity menu. They want a calm, decisive recommendation they can act on immediately.
