# Ko Htun (Htun Htun Win)

### Operations & Workflow Architect | AI-Orchestrated Product Builder | MBA

I design the operating models behind SME software — the workflows, roles, data boundaries, and approval paths — then use AI coding agents (Claude Code, Codex, Cursor, Gemini) to turn those designs into working products.

My background is **10+ years in hospitality and business operations management**, not traditional manual coding. I work as a workflow architect and product builder: I map how a business actually runs, define the rules and exceptions, and direct AI agents to implement, test, and harden the system.

Based in Myanmar, building for Myanmar SME realities: MMK currency, local payment methods, shared tablets, low-connectivity sites, and audit-heavy operations.

[LinkedIn](https://www.linkedin.com/in/ko-htun-htun-win-146970102/) · [Email](mailto:kohtunhtun386@gmail.com) · [GitHub](https://github.com/kohtun386)

---

## What I Do

- **Workflow architecture** — model roles, handoffs, approvals, exceptions, and audit requirements before writing code.
- **Product building** — turn operator knowledge into scoped, testable SaaS for real business constraints.
- **AI-orchestrated delivery** — use Claude Code, Codex, Cursor, and Gemini to accelerate implementation, migrations, tests, and documentation; review and verify the output.
- **Governance-first design** — Row Level Security, RBAC, immutable audit trails, and RPC-only approval paths.
- **Domain focus** — manufacturing ERP, retail/POS, workforce and HR automation, and AI-assisted sales workflows.

---

## Tech & Tools

| Area | Tools |
|---|---|
| **Product & workflow** | Process mapping, role/permission design, state machines, acceptance criteria |
| **Frontend** | React, TypeScript, Vite, Next.js, Tailwind CSS, MUI |
| **Data & backend** | PostgreSQL, Supabase (Auth, RLS, RPC, Edge Functions), Firebase (Auth, Firestore, Cloud Functions), pgvector |
| **AI** | Gemini, OpenAI, RAG, tool/function calling, Claude Code, Codex, Cursor |
| **Delivery** | Docker, GitHub Actions, Vercel, Google Cloud Run, Supabase CLI |

---

## Flagship Project

### Factory ERP V4 — `Lean-ERP`

**Status:** Active · **Type:** Solo project, own idea, private repo

A multi-tenant ERP for Myanmar textile and weaving mills. I own the product direction, workflow architecture, and AI-orchestrated delivery.

**Problem it solves:** factory operations run on shared tablets, paper logs, and spreadsheet payroll. Factory ERP V4 brings production, piece-rate payroll, subcontracting, inventory, sales, and financial control into one governed system.

**Scope:**

- Production logging and work orders
- Piece-rate payroll
- Subcontracting
- Inventory and master data
- Sales/POS and financials
- Reporting and audit trails
- Role-based supervisor, operator, and owner workflows

**Architecture:**

- Tenant isolation enforced with PostgreSQL Row Level Security
- RPC-only approvals; no direct client writes to governed records
- Immutable approved production records and append-only audit trails
- Process gates that enforce valid state transitions
- Mobile-first UX for shared factory tablets

**Stack:** React 18 · Vite · TypeScript · MUI 7 · Supabase (PostgreSQL, Auth, RLS, RPC)

**Scale:** 1,000+ commits · 250+ migrations · 11 domain modules

**Repo:** `kohtun386/Lean-ERP` *(private — walkthrough available on request)*

---

## Commercial Build

### CoffeeShop POS — Paused

**Status:** Paused · **Type:** Private commercial build, derived from an MIT-licensed base

A multi-tenant point-of-sale platform for coffee and tea shops in Myanmar. Started from the MIT-licensed `POS-system` base used in **Vibe Code Tours**, then evolved into a private commercial product with deeper tenancy, payments, inventory, and reporting.

Development is paused while I focus on Factory ERP V4. The Supabase backend is also paused, so no live demo is linked here.

**Scope:**

- Multi-tenant shops, memberships, and role-based access
- 9 payment methods, including KBZPay, WavePay, AYAPay, CBPay, and MPU
- Split payments, credit sales, and customer credit limits
- Inventory, purchasing, and CSV import/export
- Discount engine and sales reports
- Installable PWA for iPad and Android

**Stack:** React 18 · Vite · TypeScript · Tailwind CSS · Supabase (PostgreSQL, Auth, Edge Functions)

**Scale:** 450+ commits · 90+ migrations · 13 Edge Functions

**Repo:** `kohtun386/coffeeshop-pos-commercial` *(private)*

**Upstream credit:** built on the MIT-licensed `POS-system` base.

---

## AI Prototypes

Smaller experiments used to test AI workflows, retrieval, and agent patterns. These are prototypes, not production systems.

### AuraFit Coach

**Repo:** [kohtun386/aurafit](https://github.com/kohtun386/aurafit) · **Status:** Prototype / Google Cloud Gen AI Academy entry

A personal AI athletic coach and recovery journal. Athletes log training volume, RPE, sleep, and soreness; Gemini generates a recovery score, coaching feedback, and actionable recovery habits. Includes a multi-turn coach chat and a bilingual English/Myanmar interface.

**Stack:** React 19 · Vite · TypeScript · Tailwind CSS · Express · Gemini API · Firebase Auth/Firestore · Google Cloud Run

### Single-Merchant AI Sales MVP

**Repo:** `kohtun386/Single-Merchant-AI-Assisted-Sales-MVP` *(private)* · **Status:** Prototype / pilot architecture

An AI sales and customer-service prototype for a single clothing and fabric merchant. It combines product discovery, live variant stock checks, FAQ retrieval, order drafting, payment verification, and human staff handoff.

**Stack:** Next.js 14 · React · TypeScript · Supabase PostgreSQL · pgvector · Gemini · OpenAI · Zod

**Note:** this is a prototype, not a hosted production application.

---

## Team & Hackathon Projects

Work built with other people. Credit is shared; my role is stated explicitly.

### HR Chronicle AI

**Live:** [myanmardev.web.app](https://myanmardev.web.app) · **Repo:** [vibecode-ting/hr_chronicle_ai](https://github.com/vibecode-ting/hr_chronicle_ai) · **Event:** AI Builder Cup 2026

An employee milestone and recognition platform for distributed teams across Asia Pacific. It handles birthdays and work anniversaries, AI-personalized multilingual greetings, roster OCR, email/Teams/Telegram delivery, gift budgeting, and an HR copilot.

**My role:** **Team Member / Contributor**

- Contributed the HR Copilot function-calling implementation
- Set up the local Firebase emulator configuration for team development

**Team:** [Htet Aung Hlaing](https://github.com/vibecode-ting) (Lead Architect & Full-Stack Developer) and [Myo Set Paing](https://github.com/Mark3172) (Core Contributor & UI/UX Specialist)

**Stack:** React 19 · Vite · TypeScript · Firebase · Gemini · Three.js · Cloud Functions

### ARGUS

**Repo:** [kohtun386/ARGUS](https://github.com/kohtun386/ARGUS) · **Event:** Vibe Code Tours, Team-07

A decentralized security framework for detecting **Shadow AI** across enterprise endpoints. Lightweight Linux, macOS, and Windows agents scan for unauthorized AI tools and report findings to a central backend and dashboard.

**My role:** **Team Member / Team Lead**

**Stack:** Python agents · FastAPI · SQLite · HTML/JS dashboard · API-key authentication

**Note:** public fork of the [Team-07 project repository](https://github.com/vibecode-team7/ARGUS).

---

## How I Work

1. **Operations before code.** Map the real workflow, roles, exceptions, and failure modes first.
2. **Governance by design.** Put tenant isolation, permissions, approvals, and audit trails at the database boundary — not just in the UI.
3. **AI-orchestrated delivery.** Use coding agents for speed, then review, test, and verify every critical path.
4. **Local-first constraints.** Design for MMK, local payment methods, shared devices, and real connectivity conditions.

---

## Background

- **10+ years** in hospitality and business operations management
- **MBA**
- Based in Myanmar
- Currently building **Factory ERP V4**
- Open to global remote roles in operations coordination, project management, and AI-assisted product delivery, as well as select SME software collaborations.

---

## Connect

[LinkedIn](https://www.linkedin.com/in/ko-htun-htun-win-146970102/) · [Email](mailto:kohtunhtun386@gmail.com) · [GitHub](https://github.com/kohtun386)

<p align="center">
  <i>Operations-first product building, delivered with AI agents.</i><br>
  <sub>Last updated: November 2026</sub>
</p>
