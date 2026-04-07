# codelog-ai ✏️

You stop mid-debug. You had the fix, a note for yourself. Now it’s gone—buried in Slack, a closed tab, your terminal history.

This is your private notebook for code. It runs where you deploy it, with only your keys.

**Live demo:** https://codelog-ai.casey-digennaro.workers.dev

---

## Why

Every developer loses debug notes. You shouldn’t keep them on someone else’s server or inside a paid tool. This runs on your Cloudflare account, period.

---

## Quick Start

1.  **Fork** this repository.
2.  **Deploy** to Cloudflare Workers with the “Deploy with Workers” button.
3.  Add your `AI_PROVIDER_KEY` as a Worker secret. Setup is done.

---

## What It Does

*   Log code snippets, debug steps, or ideas with tags from your editor or terminal.
*   Ask plain-language questions to find notes from weeks ago.
*   Paste error output for structured breakdowns.
*   Call it via a simple REST API from CLI, git hooks, or scripts.
*   Use in-memory storage by default; attach a KV namespace for persistence when you need it.

---

## One Honest Limitation

On Cloudflare Workers’ free tier, each request has a 10ms CPU time limit. Complex queries or large context windows may hit this limit unless you upgrade to a paid Workers plan.

---

## How It Works

A single Cloudflare Worker script. Zero npm dependencies. No external servers, no telemetry. Your API keys go directly from your Worker to your chosen LLM provider.

---

## What Makes It Different

1.  **No middleman.** It runs exclusively on your Cloudflare account.
2.  **No lock-in.** Your data is always yours and exportable.
3.  **No bloat.** No accounts, teams, onboarding, or upsells. It’s a notebook.

---

## Bring Your Own Keys

Use OpenAI, Anthropic, Groq, or any compatible LLM API. No keys are bundled or shared.

---

MIT License

Original work: Superinstance and Lucineer (DiGennaro et al.)

<div style="text-align:center;padding:16px;color:#64748b;font-size:.8rem"><a href="https://the-fleet.casey-digennaro.workers.dev" style="color:#64748b">The Fleet</a> &middot; <a href="https://cocapn.ai" style="color:#64748b">Cocapn</a></div>