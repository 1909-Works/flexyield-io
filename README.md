<p align="center">
  <img src="https://flexyield.io/icon.png" width="72" alt="FlexYield">
</p>

# FlexYield — the access layer for the machine economy on-chain

Software is starting to buy its own infrastructure. An AI agent that needs to
read a chain, resolve a name, price a token or watch a transaction should not
have to compare providers, hold credentials for each, and reconcile six
invoices — and neither should the human who runs it.

FlexYield is a **unified access layer for blockchain infrastructure built for
two kinds of customers at once: people and their agents.** One endpoint, one
key, one bill. Behind it, many providers, measured continuously, with the
traffic routed to whoever serves it best right now — and every number we act
on published on a public status page.

- **Try it live, no signup:** https://flexyield.io/toolbox
- **Docs:** https://flexyield.io/docs · **Measured status, public:** https://flexyield.io/status
- **Pricing:** https://flexyield.io/pricing · **Free tier:** https://flexyield.io/registration/new
- **For agents:** a key without signup — `POST https://flexyield.io/keys` (MCP `get_key`) ·
  pay per call with USDC on Base over x402 — `GET https://flexyield.io/x402` ·
  MCP server `io.flexyield/gateway` · skill: https://flexyield.io/skill.md ·
  agent card: https://flexyield.io/.well-known/agent-card.json · site summary: https://flexyield.io/llms.txt

## Agent-first, human-friendly

Every capability exists twice, from the same code: a page for a person and an
MCP tool for an agent. That is a design rule, not a feature list.

- **Agents are customers.** Three doors, nothing logs in: an agent gets a
  capability key with no signup, binds it to a wallet by signature for a
  persistent identity, pays per call in USDC, or hands its owner a claim code
  and inherits the owner's plan. Each key carries a budget and a service menu
  its owner sets; a robot may reach the charger, not the bank. The agent menu
  (`what_can_i_do`, `quote`, `pick_chain`, `pick_route`) prices its own volume
  on every lane and recommends from measured data.
- **Fences carry doorways.** Every limit answers with what to do next — a
  structured error with the path to the fix, never a bare 429. When a call
  fails, the error carries a `request_id`; an agent files it as a ticket and
  the evidence is attached automatically.
- **Honest by measurement.** Latency, uptime and reroutes are published as we
  measure them, per chain, in public. Claims we cannot measure we do not make.
- **No token required.** Card-billed SaaS today, with the domain deliberately
  shaped so the same access layer can settle on-chain later.

## What you get today

| | |
|---|---|
| One endpoint, six mainnets | Ethereum, Base, Arbitrum, Optimism, Polygon, Solana — JSON-RPC in, one key, one meter |
| Multi-provider routing | requests move to another provider when one degrades; you see it on /status |
| Toolbox | gas, token prices, name resolution, transaction status, contract ABI + decoding, EVM utilities — one call instead of many |
| Per-key control | budgets, service switches and spend caps per key — for people and for agents |
| Free tier | real traffic, no card, no wallet |

## Where this is going

Three horizons, in order, each gated by the one before it:

1. **Gateway** — the unified access layer with measured routing and card billing. Live.
2. **Marketplace** — supply onboarding and route tiers (cheap · balanced · fast), so every
   customer picks their own price/latency point per request.
3. **Protocol** — the same access layer settled on-chain, for agents that pay as they go.

We build in that order because demand should be proven before anything is
decentralised. Details of the roadmap live with the product; ask us.

## Who is behind it

FlexYield is founded and built by [JadeMind GmbH](https://jademind.com),
Austria — production software for regulated industries since 2010.
Contact: hello@flexyield.io.

## This repository

This is the public front door: the MCP registry manifest (`mcp/server.json`),
directory metadata (`glama.json`), and this README. The gateway itself is
closed source. Issues here are welcome for listing and metadata questions;
product support runs through the console at https://flexyield.io/support — every
ticket arrives with the failing call, your limits and the chain status attached;
hello@flexyield.io works too.

*Made in Austria.*
