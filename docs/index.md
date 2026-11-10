# **Regulated Industry with IBM Bob**

---

## **i. Regulated industries raise the bar for AI-assisted engineering**

![type:video](./_videos/Introduction [Bob Regulated L3].mp4)
!!! note ""
    Christopher Bienko *(AI Enablement GTM Product Manager)* introduces the *Regulated Industry with IBM Bob* curriculum for hands-on enablement. **<a href="https://ibm.seismic.com/Link/Content/DCRJq22fphHj98WMfCTq9G2qTV7d" target="_blank">[4 min]</a>**

Banking and insurance run on software that must satisfy an auditor as well as a user. Each capability has to be explainable. Each rule that governs money has to hold without exception. Each change has to leave a record of what was altered and by whom. These obligations shape how engineering teams in regulated sectors operate. They also define what an AI engineering partner must be able to do before it belongs in the workflow.

This hands-on lab puts IBM Bob to work inside that setting. The application is **GFM Bank**, a demonstration core-banking system with a FastAPI backend. Role-based access control separates tellers from back-office staff, and a transaction engine enforces overdraft limits and reversal rules. Across three modules you will use Bob to build a documented understanding of that system. You will then generate a production-style teller interface on top of it. Finally you will find and remediate the security vulnerabilities hiding in its code. Each module produces the kind of durable, reviewable artifact a regulated environment expects.

This lab is designed for the IBM sellers, partners, and technical practitioners who demonstrate Bob to clients in regulated sectors. Anyone comfortable with an IDE and a terminal can follow along.

---

## **ii. What is IBM Bob?**

**IBM Bob is an AI-powered software engineering partner that supports the entire development lifecycle.** Where a traditional code-completion tool is anchored to the moment of writing code, Bob is designed to support the lifecycle around it. In this lab, Bob will:

- Analyze an unfamiliar codebase and explain its architecture, roles, and business rules
- Produce reference documentation, requirements, and invariants as persistent files
- Generate a complete React front-end from a single specification, grounded in local design-system references
- Diagnose runtime failures from a screenshot and a plain-language description
- Audit code for security vulnerabilities, remediate them, and verify the result

!!! note "RECOMMENDED PREREQUISITE: *CLIMBING THE AI MATURITY CURVE WITH IBM BOB LEVEL 3*"
    This course is best taken after the <a href="https://ibm.github.io/bob-l3/" target="_blank">**Climbing the AI Maturity Curve with IBM Bob**</a> Level 3 curriculum. It assumes those concepts are familiar ground: the Agentic Sidebar and its modes, the approval gates that keep the developer in control, and the review-before-trust habit that carried through every stage of that course. The material ahead builds directly upon that foundation.

Bob operates directly within the development environment, so you keep complete visibility into every stage of the process. Bob does the work throughout this lab. Your job is to steer it with prompts and to judge the results before they are trusted.

---

## **iii. Environment: the GFM Bank demo application**

The lab workspace is delivered as a single archive and opened directly in the Bob IDE. It contains four folders, each with a role in the modules ahead.

| Folder | Responsibility |
|--------|----------------|
| `.bob` | Bob's workspace configuration, with the custom Modes, Skills, and rules pre-configured for this lab |
| `bob-banking-lab` | The GFM Bank demo application codebase and lab assets, including the Python `teller_client.py` and `backoffice_client.py` clients |
| `carbon-offline-reference` | Offline copies of IBM Carbon Design System component definitions (TypeScript `.d.ts` files), which Bob reads to generate accurate, API-correct Carbon code |
| `scripts` | Helper scripts used to set up the lab environment |

The GFM Bank backend itself runs remotely on IBM Cloud Code Engine, and the lab's clients and the front-end you build all connect to it over HTTPS. The system exercises the patterns that dominate real banking software:

- OAuth2 authentication with **TELLER** and **BACKOFFICE** roles that differ in their permissions
- A transfer engine with balance verification, overdraft handling, and a two-transaction debit/credit pattern
- A data model that relates users and customers to their accounts and transactions
- An audit trail of what is logged and stored for compliance

Although GFM Bank is a demonstration system, it carries the same invariants and access rules that real core-banking platforms enforce. That is what makes it a credible stage for showing clients how Bob behaves under regulated-industry expectations.

---

## **iv. The lab journey**

!!! note "AI MATURITY CURVE"
    The three modules follow the same arc as the previous course. *Analyze* has Bob build durable understanding of an unfamiliar system and save it into the workspace, which is the persistent-artifact pattern from **Module 4 | Scale & Extend**. *Build* is **Module 2 | Delegate** at project scale: one specification produces a whole application, and an approval gate precedes every consequential step. *Secure* makes Bob its own reviewer, and the reports it writes are the record a regulated environment requires. The discipline is the one you already practiced, now applied where the stakes are higher.

| Module | Focus | What You'll Do |
|--------|-------|----------------|
| **<a href="https://bienko.github.io/bob-regulated-industry/1-1/" target="_blank">Module 1 - Analyze</a>** | Understand the application | Direct Bob through a read-only analysis of the codebase, then have it produce an architecture document, a data-pipeline analysis, a functional requirements document, and a catalogue of system invariants. |
| **<a href="https://bienko.github.io/bob-regulated-industry/2-1/" target="_blank">Module 2 - Build</a>** | Generate and iterate | Prove the existing teller client against the live backend, generate a complete Carbon-based React teller portal from one specification, then run it and work through the debug loop with screenshots and plain-language prompts. |
| **<a href="https://bienko.github.io/bob-regulated-industry/3-1/" target="_blank">Module 3 - Secure</a>** | Find and fix | Run an OWASP and CWE vulnerability scan, produce a security audit report and a deep dive on the most critical findings, apply the remediations, and verify them. |

---

## **v. What you will build**

!!! note "**A WORD ON WORKING WITH GENERATIVE AI**"

    IBM Bob is powered by generative AI and LLMs, and a defining trait of these systems is that they are *non-deterministic* — unlike the *deterministic* tools most developers are accustomed to. In practice, that means the same prompt can produce different code from one run to the next. This is both a strength and a quirk of the technology, and it is something to work *with* rather than against.

    **Precision is what tips the odds in your favor.** The more clearly you describe what you want, the more closely Bob's output will mirror your intent; conversely, the smallest change in wording can meaningfully change the generated code. Throughout this lab, your results may differ from the solutions shown — and that is expected, not a defect. Whenever an output diverges, you have three good options: refine the prompt and try again, edit the generated code by hand, or simply proceed if the variation still compiles and runs. Human review remains essential at every step, and never more so than while you are still learning the tool.

**The understanding (<a href="https://bienko.github.io/bob-regulated-industry/1-1/" target="_blank">Module 1 | Analyze</a>).** Using Agent mode with read-only tasks, you will have Bob produce four documents:

- `ARCHITECTURE.md`
- `DATA_PIPELINE.md`
- `FUNCTIONAL_REQUIREMENTS.md`
- An invariants document

Together they describe the system's components and its request lifecycle. They also record every supported business operation and the rules that must never be violated.

**The application (<a href="https://bienko.github.io/bob-regulated-industry/2-1/" target="_blank">Module 2 | Build</a>).** Using a single specification, Bob will generate a React teller portal built on the IBM Carbon Design System. It covers login and a dashboard with a live backend status indicator. It also covers the full set of teller operations, from balance inquiry to transfers. You will run it and sign in. You will then resolve the issues that surface with a screenshot and a sentence, reviewing Bob's fix each time.

**The assurance (<a href="https://bienko.github.io/bob-regulated-industry/3-1/" target="_blank">Module 3 | Secure</a>).** Bob will scan the codebase for vulnerabilities and rank them by severity. It will document the five most critical with exploit scenarios and secure fixes. It will then apply the remediations and produce a verification report. A final run of the application confirms that the patches broke nothing.

---

## **vi. Next steps**

Proceed to the [Setup](setup.md){:target="_blank"} page to download the workspace and sign in to Bob, then continue to [Module 1 | Analyze](1-1.md){:target="_blank"} to begin with the codebase analysis.

---
