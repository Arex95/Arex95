<h1 align="center">Arthur — Arex95</h1>

<p align="center">
  <strong>Software architect</strong> · Full-stack · AI agent workflows
</p>

<p align="center">
  <em>I build product systems end to end — the panel, the API behind it, and what runs them.<br/>Frontend architecture is where I go deepest.</em>
</p>

<p align="center">
  <a href="https://arexforge.com"><img src="https://img.shields.io/badge/Studio-arexforge.com-FF6321?style=flat-square&logo=googlechrome&logoColor=white" alt="Arex Forge" /></a>
  <a href="https://www.npmjs.com/~arex95"><img src="https://img.shields.io/badge/npm-arex95-CB3837?style=flat-square&logo=npm&logoColor=white" alt="npm" /></a>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=FF6321&center=true&vCenter=true&width=600&lines=Full-stack+%E2%80%94+panel%2C+API+and+what+runs+them;Frontend+architecture+is+where+I+go+deepest;Headless+frameworks+for+admin+panels;AI+agents+under+strict+workflows" alt="Typing SVG" />
</p>

---

### 📦 Phalanx — the headless framework for admin panels

[![npm](https://img.shields.io/npm/v/@arex95/phalanx?style=flat-square&color=FF6321&label=npm)](https://www.npmjs.com/package/@arex95/phalanx)
[![license](https://img.shields.io/npm/l/@arex95/phalanx?style=flat-square&color=555)](https://github.com/Arex95/phalanx/blob/main/LICENSE)
[![docs](https://img.shields.io/badge/docs-arex95.github.io-FF6321?style=flat-square)](https://arex95.github.io/phalanx/)

Everything an admin panel needs below the interface. Declare a resource once and
get its service, its TanStack queries and mutations, and its custom operations —
with session handling, realtime, encrypted storage and typed errors already
decided. It ships no components: the interface stays yours.

- **Services** — one class per resource, eleven inherited methods, custom operations alongside them.
- **Actions** — permission, confirmation, notification and cache invalidation declared as metadata rather than repeated in every view.
- **Session** — access token in memory, refresh in an `HttpOnly` cookie, one refresh in flight with concurrent 401s queued behind it.
- **Realtime** — a reconnection state machine with backoff and a circuit breaker, transport injected.
- **Encryption** — browser storage under a non-extractable key, and hybrid field encryption for data only the server should read.

> Design decisions are documented with their sources — [RFC 9700](https://datatracker.ietf.org/doc/html/rfc9700), OWASP, and the rest — in [Foundations](https://arex95.github.io/phalanx/concepts/foundations).

---

### 🦀 Atlas — several agents, one declared way of working

[![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)](https://github.com/Arex95/atlas)
[![license](https://img.shields.io/badge/license-PolyForm%20Noncommercial-555?style=flat-square)](https://github.com/Arex95/atlas/blob/main/LICENSE)
[![docs](https://img.shields.io/badge/docs-arex95.github.io-FF6321?style=flat-square)](https://arex95.github.io/atlas/)

An agent will tell you the task is done. **Atlas is built so that saying it is
not enough.** Self-hosted and local-first: no account, no cloud, and nothing
leaves the machine until you point it at a server you run yourself.

- **Gates the runtime executes.** A node declares its acceptance criteria — a
  command that must exit zero, a payload that must match a schema — and the run
  does not advance until they pass. On failure the reason is injected back into
  the agent's context and the node retries. Nothing is self-reported.
- **The workflow is a file in the repository**, re-read on every run, so a
  teammate who pulls your change is held to the same rules without registering
  anything. One declaration, every developer's agents.
- **48 MCP tools** over JSON-RPC 2.0 — sessions, terminals, memory, notes,
  messaging, workflow runs, project map, issue tracker — each resolving its
  caller from the credential it presented. No tool accepts an actor as an
  argument, which is what keeps identity from being something a client asserts.
- **Real PTYs and portable sessions.** A session records how to rehydrate
  itself, so a machine that has never seen the repository clones it and picks up
  where the last one left off.

> Where the boundary **is not**, written down rather than implied: tool scope
> narrows what a workflow hands an agent, but it is not containment. The only
> thing that contains an agent holding a real terminal is the operating system —
> and the [trust model](https://arex95.github.io/atlas/concepts/trust-model) says
> so on its own page.

---

### 🛠️ What I work with

<p align="center">
  <img src="https://skillicons.dev/icons?i=rust,ts,vue,nuxtjs,react,nextjs,tailwind,vite,pinia,nodejs,nestjs,java,spring,php,laravel,postgres,sqlite,redis,mongodb,supabase,flutter,electron,tauri,vitest,docker,nginx,linux,gitlab,githubactions,bash,git,pnpm,markdown&perline=11" alt="Stack" />
</p>

A logo says a name was typed once. What follows is what the name is actually
used for, and the parts that have no logo — usually the ones that decide how a
system behaves.

| | |
| :--- | :--- |
| **Frontend** | Vue 3 and Nuxt, React and Next.js, TypeScript, Tailwind, Vite. **Pinia** for state that is genuinely shared, **TanStack Query** for state that belongs to the server and should not be copied into a store, **Zod** at the boundary. `xterm.js`, Cytoscape and Chart.js when the interface is a terminal, a graph or a chart rather than a form. |
| **Backend** | NestJS, Spring Boot, Laravel — and Rust when a process has to hold something open. One response envelope for success and failure alike, **JSON-RPC 2.0** for MCP surfaces, **Server-Sent Events** and WebSockets for anything live. UUIDs in every public surface: a sequential key leaks table size and invites enumeration. |
| **Systems — Rust** | **Tokio** and **Axum**, `sqlx` over SQLite with one migration set per feature, `portable-pty` for terminals that are real rather than emulated, `tower`/`tower-http` for middleware, `tracing` for structured logs. **Argon2** for passwords, SHA-256 and BLAKE3 for digests — a stolen database should yield a digest, not a usable token. |
| **Data** | **PostgreSQL** by default: constraints, joins, transactions, and a recoverable cost when the model turns out wrong. **Redis** for what is genuinely ephemeral, **MongoDB** where documents are read whole and never joined, **Supabase** when the project justifies it, **SQLite** when the database belongs to one machine and travels with it. |
| **Testing & quality** | **Vitest** and **Playwright**; `cargo test` with `wiremock` at the HTTP edges. **Mutation testing**, because a suite that stays green after you break the code was testing nothing. Clippy at `-D warnings` on two toolchains — a lint that fires on only one of them fires in CI instead of on your machine. |
| **Delivery** | **Docker** multi-stage, non-root, configuration entirely from the environment so one artefact runs anywhere. **Nginx**, **Linux**, **GitLab CI** and **GitHub Actions**. Every gate reproducible locally with a single command, or it is a gate nobody runs until it blocks them. |
| **AI & agents** | **Model Context Protocol** servers, agent CLIs driving real terminals, and workflows whose acceptance criteria are executed instead of reported. The interesting part was never the model — it is what refuses to advance when the output is wrong. |
| **Cross-platform** | **Flutter**, **Electron**, **Tauri** — chosen by what the thing has to reach, not by preference. |

---

### 🏗️ What I build

Five systems in production or close to it: a booking platform, a CRM, an intake
product for messaging channels, an LMS, and Atlas. In each one I write the panel
**and** the API behind it — Vue or React on top, NestJS, Spring, Laravel or Rust
underneath — plus the containers, the pipelines and the servers they run on.

Frontend architecture is the part I have gone deepest into, and it is where
Phalanx came from. It is not the only part I do.

What makes them survive is not the code. It is having the decisions written
down before they are needed — architecture, API conventions, naming, quality
gates, how secrets are handled, how things ship — and workflows that hold agent
output to them. An agent that can write anything is not useful; one that has to
pass a gate is.

---

### 📫 Elsewhere

[![Arex Forge](https://img.shields.io/badge/arexforge.com-FF6321?style=flat-square&logo=googlechrome&logoColor=white)](https://arexforge.com)
[![npm](https://img.shields.io/badge/npm-arex95-CB3837?style=flat-square&logo=npm&logoColor=white)](https://www.npmjs.com/~arex95)
