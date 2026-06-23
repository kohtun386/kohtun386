# Ko Htun (Htun Htun Win)

![Status](https://img.shields.io/badge/Status-Actively%20Building-success)
![Focus](https://img.shields.io/badge/Focus-SaaS%20%7C%20ERP%20%7C%20Payroll-1f6feb)
![Region](https://img.shields.io/badge/Region-Myanmar-3fcf8e)

> **Product-focused full-stack developer** building governed, deterministic SaaS platforms for manufacturing, academic automation, and POS systems. I design systems where data integrity is non-negotiable and audit trails are sealed at the database level.

---

## What I Build

- **Factory ERP** — Multi-tenant workforce intelligence for garment/textile manufacturing
- **Academic Automation** — AI-powered thesis generation with multi-agent orchestration and HITL quality gates
- **POS Systems** — In-browser point-of-sale with payments and inventory workflows
- **Payroll Automation** — Piece-rate payroll engines for textile mills with deterministic calculation

**Core Principles:**
- 🏛️ **Governance First** — RBAC, audit trails, immutable logs
- 📱 **Mobile-First** — Owner and supervisor workflows on the go
- 🔒 **Data Integrity** — RLS-enforced tenant isolation, RPC-only approvals
- 🌏 **Local-First** — Built for Myanmar market realities

---

## Tech Stack

| Layer | Technologies |
|-------|--------------|
| **Frontend** | React 18 · Vite · TypeScript · MUI v7 |
| **Backend** | Supabase (Postgres · Auth · RLS · RPCs) · Firebase |
| **Architecture** | React Context API · Service-layer mutations · Deterministic flows |
| **Deployment** | Vercel · GitHub Actions |
| **Mobile** | Flutter · Dart |
| **Tools** | Claude Code · n8n · Docker |

---

## Featured Projects

### 🏭 Factory ERP V4

**Governed, enterprise-ready workforce intelligence SaaS for garment factories.**

![Status](https://img.shields.io/badge/Status-Active-success)
![Stack](https://img.shields.io/badge/Stack-React%20%2B%20Supabase-1f6feb)

- **Repo:** [kohtun386/factory-erp-supabase](https://github.com/kohtun386/factory-erp-supabase) *(private)*
- **Stack:** React + Vite · Supabase · MUI v7 · TypeScript
- **Status:** Active Development (Phase 2 — Onboarding & Governance)
- **Key Features:**
  - Multi-tenant architecture with Row Level Security
  - Deterministic production log approvals (RPC-only)
  - Immutable audit trails
  - Invite-only self-serve onboarding
  - Mobile-first UX for supervisors and operators

**Architecture Invariants:**
- Approvals via `SECURITY DEFINER` RPCs only
- Approved records are immutable (no UPDATE, no DELETE)
- Process gates enforce valid state transitions
- Audit trails are append-only

> *"Approval is RPC-only. Immutability is enforced at the database level. No client bug can violate boundary invariants."*

---

### 🎓 Shadow Thesis Factory

**B2B SaaS platform for automated thesis generation using Event-Driven Multi-Agent Orchestration.**

![Status](https://img.shields.io/badge/Status-Active-success)
![Stack](https://img.shields.io/badge/Stack-FastAPI%20%2B%20n8n%20%2B%20Supabase-3fcf8e)

- **Repo:** [kohtun386/shadow-thesis-factory-poc](https://github.com/kohtun386/shadow-thesis-factory-poc) *(private)*
- **Stack:** FastAPI · n8n · Supabase (PostgreSQL, pgvector) · Python · React
- **Status:** Active Development

**Architecture Highlights:**
- **Human-in-the-Loop (HITL)** — Quality control and approval gating at every stage
- **Citation Hard Validation** — Law 4 enforcement for verified scholarly sourcing
- **Deterministic Data Parsing** — SPSS exports: numeric extraction separated from AI narrative generation
- **Event-Driven Orchestration** — n8n workflow engine with centralized error handling

**Key Components:**
- FastAPI Backend-for-Frontend (BFF)
- n8n workflow orchestration (`wf_05_chapter_writer`, `wf_error_handler`)
- Supabase with pgvector for semantic search
- CONCURRENTLY indexed for performance (`drafts`, `thesis_framework`)

---

### 💳 POS-system

**Web-based point-of-sale system with payments and inventory UI.**

![License](https://img.shields.io/badge/License-MIT-green)
![Stars](https://img.shields.io/github/stars/kohtun386/POS-system)

- **Repo:** [kohtun386/POS-system](https://github.com/kohtun386/POS-system)
- **Stack:** TypeScript · React · Vercel
- **Demo:** [pos-system-gilt-mu.vercel.app](https://pos-system-gilt-mu.vercel.app/)
- **Status:** In Development
- **Highlights:** In-browser POS, payment workflows, inventory management

---

### 🌐 Vibe Code Tours

**Public bilingual landing site for Vibe Code Tours.**

- **Repo:** [kohtun386/vibe-code-tours.github.io](https://github.com/kohtun386/vibe-code-tours.github.io)
- **Stack:** Static Site · HTML/CSS
- **Live:** [vibecode.tours](https://vibecode.tours)

---

## Architecture Philosophy

My systems follow **deterministic flow design**:

```
┌─────────────────────────────────────────────────────────────┐
│                    GOVERNANCE LAYER                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │ RBAC/Auth   │  │ Audit Logs  │  │ Tenant Isolation    │ │
│  │ (Supabase)  │  │ (Immutable) │  │ (RLS Policies)      │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                   BUSINESS LOGIC                            │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │ RPC-Only    │  │ Service     │  │ Deterministic       │ │
│  │ Approvals   │  │ Layer       │  │ State Transitions   │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                     PRESENTATION                            │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │ Mobile-First│  │ React       │  │ MUI v7              │ │
│  │ UX          │  │ Context API │  │ Components          │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
└─────────────────────────────────────────────────────────────┘
```

---

## Let's Connect

![GitHub](https://img.shields.io/badge/GitHub-kohtun386-12100E?style=flat&logo=github)
![Email](https://img.shields.io/badge/Email-Contact%20Me-1f6feb?style=flat&logo=mail.ru)

**Open to:** Collaboration on SaaS ERP systems, AI-powered automation, manufacturing workflows, and Myanmar-focused tech products.

---

<p align="center">
  <i>Building governed, deterministic, enterprise-ready SaaS platforms.</i><br>
  <sub>Last updated: June 2026</sub>
</p>
