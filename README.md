# FSP — DevSecOps Practice

> **Agentic DevOps with Microsoft Azure and GitHub.** Repeatable, secure, evidence-first software delivery — by Foundation Specialist Partner (FSP).

[![Microsoft Solutions Partner](https://img.shields.io/badge/Microsoft-Solutions%20Partner-0078D4?logo=microsoft&logoColor=white)](https://partner.microsoft.com/)
[![Specialisation: Agentic DevOps](https://img.shields.io/badge/Azure%20Specialisation-Agentic%20DevOps%20(v2.6)-0078D4)](https://partner.microsoft.com/)
[![GitHub Enterprise](https://img.shields.io/badge/GitHub-Enterprise-181717?logo=github)](https://github.com/enterprise)
[![GHAS](https://img.shields.io/badge/GitHub-Advanced%20Security-2EA44F?logo=github)](https://github.com/security/advanced-security)
[![Copilot](https://img.shields.io/badge/GitHub-Copilot-8957E5?logo=githubcopilot)](https://github.com/features/copilot)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

---

## Table of contents

- [What we do](#what-we-do)
- [Why this matters](#why-this-matters)
- [Capability matrix](#capability-matrix)
- [Operating principles](#operating-principles)
- [Reference architecture](#reference-architecture)
- [Engagement model](#engagement-model)
- [Certifications](#certifications)
- [Get in touch](#get-in-touch)

---

## What we do

We help organisations adopt **secure, automated software delivery on Microsoft Azure** using the GitHub platform — Enterprise, Actions, Advanced Security (GHAS) and Copilot. Our practice is operated against the Microsoft Azure Specialisation **Agentic DevOps with Microsoft Azure and GitHub (v2.6)** as our internal quality bar — even where engagements do not require formal certification.

> **Core promise:** every customer outcome is **measurable, auditable, and reproducible**. If we cannot evidence it from a pipeline run or an exported artefact, we treat it as not done.

---

## Why this matters

Most cloud-delivery problems are not technology problems — they are **operating-model** problems. Teams that ship safely on Azure share four traits, and our engagements are designed around them:

1. **Single source of truth** for infrastructure, pipelines, and policy — version-controlled, reviewable, reversible.
2. **Security woven into CI**, not bolted on at release — dependency scanning, CodeQL, secret scanning before promotion.
3. **Copilot used deliberately** as an accelerator with explicit governance, not as an autonomous developer.
4. **Evidence over assertion** — auditors, regulators, and customers can re-trace any decision back to a run ID.

---

## Capability matrix

| Phase | What we deliver | Key outputs |
|---|---|---|
| **Assess** | Current-state architecture review · FinOps baseline · security posture (Defender for Cloud + Cloud Adoption Security Review) · DevOps capability assessment | Assessment report · readiness scorecard · target-state options |
| **Design** | Azure Landing Zone design (hub-spoke) · workload-specific solution design with Copilot-assisted IaC · Well-Architected Review (Operational Excellence) | ALZ design pack · solution design doc · WAR export |
| **Build** | Bicep "Gold Build" templates (parameterised) · GitHub Actions CI/CD with built-in CodeQL + dependency scanning + secret scanning · Copilot-accelerated developer workflows | Repo + pipelines · IaC modules · live deploy with run ID |
| **Operate** | Azure Monitor + Log Analytics observability · Azure Policy compliance · automated patching · GHAS alert triage SLAs | Runbooks · dashboards · alert routing |
| **Optimise** | Cost optimisation reviews (Azure Advisor + custom telemetry) · continuous WAR cadence · DORA metrics tracking | Optimisation report · DORA dashboard · quarterly review minutes |

---

## Operating principles

These six principles govern every engagement — they are non-negotiable:

| # | Principle | What it means in practice |
|---|---|---|
| 1 | **Everything as Code** | Repos, pipelines, infrastructure, and policy are version-controlled. Manual portal changes are the exception. |
| 2 | **No untracked production changes** | Deployments originate from pipelines. Emergency portal changes are ticketed, approved, and retrospectively codified. |
| 3 | **Security integrated into CI** | Every eligible repo runs dependency scanning, CodeQL, and secret scanning before any artefact is promoted. |
| 4 | **Evidence over assertion** | Pipeline logs, run IDs, and tool exports are primary evidence. Screenshots are supporting only. |
| 5 | **Least privilege by default** | RBAC, repo permissions, and secret access are minimal and reviewed periodically. |
| 6 | **Repeatability over customisation** | Standard templates and reusable modules are preferred over per-customer bespoke builds. |

---

## Reference architecture

```mermaid
flowchart LR
    subgraph GH["GitHub Enterprise"]
        Repo["Application repo<br/>(IaC + app code)"]
        Actions["GitHub Actions CI/CD"]
        GHAS["GHAS<br/>CodeQL · Dependabot · Secret Scanning"]
        Copilot["GitHub Copilot<br/>(IDE + Chat)"]
    end
    subgraph AZ["Microsoft Azure"]
        ALZ["Azure Landing Zone<br/>(hub-spoke · Bicep)"]
        Workload["Workload subscription"]
        Monitor["Azure Monitor + Log Analytics"]
        Defender["Microsoft Defender for Cloud"]
    end
    Copilot -.assists.-> Repo
    Repo --> Actions
    GHAS --> Repo
    Actions -->|"deploy via OIDC + UAMI"| ALZ
    ALZ --> Workload
    Workload --> Monitor
    Workload --> Defender
```

Every customer engagement follows this reference. Workload-specific patterns (e.g. AI Apps on Azure, Analytics on Azure, SAP on Azure) **extend** it; they do not replace it.

---

## Engagement model

We engage in three shapes:

- 🟢 **Greenfield** — new workload, new landing zone, GitHub-native from day one.
- 🟡 **Greyfield** — existing Azure estate with maturity gaps; uplifted in-place using the same Gold Build patterns.
- 🔵 **Migration** — Azure DevOps to GitHub (or hybrid), guided by a defined enablement plan.

Every engagement starts with a **one-day assessment workshop** and produces a written readiness plan **before any code is written**.

---

## Certifications

The practice maintains the following GitHub certifications across active practitioners:

- ✅ **GitHub Copilot** certification
- ✅ **GitHub Advanced Security** certification
- ✅ **GitHub Administration** certification

Each certification is held by a separate practising consultant. Independently verifiable on request.

---

## Get in touch

For an engagement enquiry, capability deck, or a copy of the FSP DevSecOps Practice Operating Playbook (NDA may apply):

📧 **info@foundation-sp.com**

---

<sub>© Foundation Specialist Partner (FSP) · Microsoft Solutions Partner · Pursuing the Azure Specialisation in Agentic DevOps with Microsoft Azure and GitHub (v2.6) · Content licensed under [Apache 2.0](LICENSE)</sub>
