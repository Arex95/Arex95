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

### 🦀 Atlas — terminal orchestrator for humans and AI agents

[![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)](https://github.com/Arex95/atlas)
[![license](https://img.shields.io/badge/license-MIT-555?style=flat-square)](https://github.com/Arex95/atlas/blob/main/LICENSE)

PTY-backed terminals in the browser that AI agents can inhabit. **The terminal is
the unit of interaction; the agent is a layer that plugs in** — not the other way
round.

- An **MCP server** (JSON-RPC 2.0) exposing 29 tools: projects, sessions, memory,
  tasks, documents, skills, filesystem, global context.
- **Project isolation** — an agent cannot read or write another project's
  resources — with path-traversal protection on every filesystem endpoint.
- **Shared context** — memory, skills and prompts an agent can reach across
  sessions, so work survives the terminal that started it.

The problem it exists for: an agent that can write anything is not useful. One
that works inside boundaries, against shared context, and leaves a trail is.

---

### 🛠️ What I work with

| | |
| :--- | :--- |
| **Frontend** | ![Vue](https://img.shields.io/badge/Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white) ![Nuxt](https://img.shields.io/badge/Nuxt-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=nextdotjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) |
| **Client state** | ![TanStack Query](https://img.shields.io/badge/TanStack%20Query-FF4154?style=flat-square&logo=reactquery&logoColor=white) ![Pinia](https://img.shields.io/badge/Pinia-FFD859?style=flat-square&logo=pinia&logoColor=black) ![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white) |
| **Backend** | ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white) ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white) |
| **Systems** | ![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white) ![Tokio](https://img.shields.io/badge/Tokio-000000?style=flat-square&logo=rust&logoColor=white) |
| **Cross-platform** | ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white) ![Electron](https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white) ![Tauri](https://img.shields.io/badge/Tauri-24C8DB?style=flat-square&logo=tauri&logoColor=black) |
| **Testing** | ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white) |
| **Delivery** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) |

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
