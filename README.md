# CodeLog.ai

You stop mid-debug. You had the fix, the note you wrote for yourself. And it's gone. Buried in Slack, a closed tab, your terminal history.

This is a local notebook for your code. It runs where you deploy it, with your keys.

**Live instance:** https://codelog-ai.casey-digennaro.workers.dev

---

## What it is
A Cloudflare Worker that gives you a personal API for logging and querying code snippets, debugging notes, and errors. It uses your AI provider keys to add context and search. You fork it, you own it, you modify it.

## How it works
- Deploys as a single Cloudflare Worker. No databases, no build steps, zero runtime npm dependencies.
- Follows a fork-first philosophy. You deploy your own copy in under a minute.
- Is Fleet-native, compatible with other agents in the Cocapn ecosystem.
- All logic runs on your worker; your API keys never leave your environment.

**One Limitation:** It's stateless by default. Snippets are stored in-memory and reset on each worker cold boot. For persistence, you need to add your own storage binding (like KV).

## Quick Start
1.  Fork this repository.
2.  Deploy it to Cloudflare Workers.
3.  Add your `AI_PROVIDER_KEY` as a Worker environment variable.

## What you can do
- **Log snippets:** Send code fragments with tags and notes via a simple POST request.
- **Query context:** Ask questions about your logged code to find past solutions.
- **Analyze errors:** Post error logs for structured root-cause analysis.
- **Call from anywhere:** Use its clean API from your editor, CLI, or CI.

## Bring your own keys
Set your `AI_PROVIDER_KEY` (e.g., from OpenAI, Anthropic, or Groq) as a secret in your Worker's environment variables. No model keys are bundled or shared.

## Contributing
Improve your own fork first. If you have a change that fits the zero-dependency, single-worker model, open a pull request.

MIT License · Superinstance & Lucineer (DiGennaro et al.)

---
<div align="center">
  <a href="https://the-fleet.casey-digennaro.workers.dev">The Fleet</a> · <a href="https://cocapn.ai">Cocapn</a>
</div>