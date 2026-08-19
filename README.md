# Revises

<p align="center">
  <strong>Developer infrastructure for working with AI.</strong>
</p>

<p align="center">
  We build small, focused tools that make AI infrastructure easier to use from the tools developers already live in.
</p>

<p align="center">
  <a href="https://github.com/revises-org">GitHub</a>
  ·
  <a href="https://revises.org">Website</a>
</p>

---

## What we're building

AI development tooling is moving fast, but the infrastructure underneath it is still full of friction.

Authentication differs across providers. Coding agents expect simple OpenAI-compatible interfaces. Cloud platforms often require short-lived credentials, request signing, or provider-specific protocols.

**Revises builds the missing pieces in between.**

Our focus is practical developer infrastructure:

* **Local AI gateways** that let editors and coding agents talk to cloud AI providers
* **Provider adapters** that handle authentication and protocol differences
* **Observability tools** that make AI requests, latency, usage, and failures easier to understand
* **Small, self-contained developer tools** that stay fast, predictable, and easy to run

---

## 🚀 Featured project

### [cram](https://github.com/revises-org/cram)

**A local AI gateway for developers.**

`cram` sits between your editor or coding agent and the cloud AI platform, translating a simple static bearer token into the authentication the upstream provider actually expects.

Today, that means **Vertex AI**.

It also solves a particularly annoying problem with **Gemini 3 tool calling**: carrying thought signatures across turns so tool-enabled conversations continue to work with clients that would otherwise drop the required metadata.

```text
Editor / Coding Agent
        │
        │ OpenAI-compatible API
        ▼
   ┌───────────┐
   │   cram    │
   │ localhost │
   └─────┬─────┘
         │
         │ provider-native auth
         ▼
     Cloud AI
```

### Why `cram`?

* ⚡ **Tiny footprint** — one small native binary, roughly 3 MB
* 🧠 **Gemini 3 tool calling** with thought-signature preservation
* 📊 **Live request dashboard** for latency, status, tokens, caching, and model usage
* 🔌 **OpenAI-compatible endpoint** for editors and clients
* 🔐 **Local-first security model** — binds to `127.0.0.1`, doesn't log request bodies, and redacts authorization headers
* 🦀 **Rust-native** — no Python, Node.js, or separate runtime required

> The goal is simple: **make cloud AI feel local to the developer.**

---

## 🧭 Our philosophy

We care less about building giant platforms and more about removing sharp edges.

A good tool should be:

**Small enough to understand.**
**Fast enough to disappear.**
**Useful enough to keep running.**

We prefer focused projects over layers of abstraction, and infrastructure that solves the awkward problems developers shouldn't have to think about.

---

## 🔭 What's next

`cram` currently focuses on Vertex AI, with the project roadmap extending toward other platforms and capabilities such as Amazon Bedrock, Azure AI Foundry, richer request history, and additional editor integrations.

The broader direction stays the same:

> **Make AI infrastructure work with the developer tools people already use.**

---

## 🤝 Open source

Revises projects are built in the open.

Issues, ideas, documentation improvements, bug reports, and pull requests are all welcome.

Start with [`cram`](https://github.com/revises-org/cram), or explore the repositories in this organization.

---

<p align="center">
  <sub>Built by Revises · Open source · Developer-first</sub>
</p>
