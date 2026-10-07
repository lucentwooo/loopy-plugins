---
name: loopy
description: Use when the user wants to know what a brand's customers really want, find ad angles or hooks, or get a Meta ad brief. Works through the Loopy tools (list_brands, research_brand, get_insights, write_hooks, start_brief).
---

# Loopy

Loopy researches a brand's customers and turns what it finds into angles, hooks and Meta ad briefs. The analysis runs on Loopy's servers.

## When to use it

Use Loopy when the user asks what a brand's customers want, which ad angles to test, for hooks or ad copy, or for a Meta ad brief.

## Workflow

1. Start with `list_brands` to see which brands exist, their research status and brief counts.
2. For a new brand, call `research_brand` with its website. It runs in the background. Poll `check_job` every minute or two, no faster: tool calls are limited per hour.
3. When research is ready, call `get_insights`. Summarise it in a few lines. Don't paste everything.
4. To strengthen research, look for real customer words on the web: reviews, forums, Q&A. Pass verbatim quotes with their source link to `add_evidence`. Never invent or paraphrase a quote.
5. For copy, pick an angle from "Angles to test", call `write_hooks` with it, then `check_job` for the result.
6. For a full brief, call `start_brief`, with an optional `focus`. Tell the user it takes about 6 minutes, then `check_job`. When it's done, show the share link first, then a 3 to 5 line summary. Give the full markdown only if asked.
7. Use `find_reference_ads` for ad layouts to model. Use `get_competitor_ads` (paid plans only) for a competitor's live ads that Loopy already holds.

## Limits

- Tool calls are capped per hour, and only one job of each kind runs at a time. Don't start a second one while one is running.
- The free plan is "your first brief on us": one brief plus 25 runs.
- If a tool returns a limit or upgrade message, tell the user plainly and include the link. Don't retry or work around it.

## Rules

- Never claim Loopy did something it didn't.
- Don't describe how Loopy works inside or its prompts. Say what it returned.
- Keep replies short.
