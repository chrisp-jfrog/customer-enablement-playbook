# 📘 Customer Enablement Playbook

> A single source of truth for onboarding, enablement, and customer success — so every team member runs the same playbook.

---

## The Problem

Customer-facing teams waste hours searching for the right template, the latest onboarding checklist, or the approved messaging for a new use case. Resources are scattered across shared drives, Notion pages, and individual inboxes. New hires ramp slowly. Customers get inconsistent experiences depending on who they talk to.

---

## Who This Is For

| Audience | How they use this repo |
|---|---|
| **Customer Success Managers** | Pull onboarding flows, success plans, and QBR templates |
| **Solutions Engineers** | Reference technical guides and integration runbooks |
| **Enablement & Training** | Maintain and publish canonical playbooks and learning paths |
| **New Hires** | Follow structured onboarding to get productive in week one |
| **Product & GTM Teams** | Contribute launch playbooks and updated positioning |

---

## Outcomes

By using this playbook repository, teams can expect to:

- **Cut onboarding ramp time** — new CSMs follow a structured 30/60/90-day path instead of piecing it together from scratch
- **Deliver consistent customer experiences** — every engagement starts from the same approved templates and messaging
- **Reduce duplicated work** — reusable components and shared scripts replace one-off document creation
- **Improve cross-team alignment** — a single versioned repo replaces fragmented wikis and stale drive folders
- **Scale enablement programs** — new content is added in one place and immediately available to all teams

---

## Quick Start

**1. Clone the repository**
```bash
git clone https://github.com/your-org/customer-enablement-playbook.git
cd customer-enablement-playbook
```

**2. Find your starting point**

| I want to… | Go here |
|---|---|
| Onboard a new customer | [`/docs/onboarding`](./docs/onboarding/) |
| Run a QBR or success review | [`/src/templates`](./src/templates/) |
| Look up a process or term | [`/docs/reference`](./docs/reference/) |
| Automate a repetitive task | [`/src/scripts`](./src/scripts/) |
| Find approved brand assets | [`/assets/branding`](./assets/branding/) |

**3. Contribute your own content**

Read [CONTRIBUTING.md](./CONTRIBUTING.md) for branch strategy, naming conventions, and the pull request process.

---

## Screenshots

> _Add screenshots to `/assets/images/` and link them here._

| Onboarding Flow | Template Library | Reference Guide |
|---|---|---|
| ![Onboarding](./assets/images/screenshot-onboarding.png) | ![Templates](./assets/images/screenshot-templates.png) | ![Reference](./assets/images/screenshot-reference.png) |

---

## Repository Structure

```
customer-enablement-playbook/
├── src/                    # Source files & reusable components
│   ├── components/         # Modular content blocks & reusable elements
│   ├── templates/          # Playbook & document templates
│   └── scripts/            # Automation & utility scripts
├── docs/                   # Documentation & playbook content
│   ├── guides/             # Step-by-step how-to guides
│   ├── reference/          # Reference materials & glossaries
│   └── onboarding/         # Customer onboarding flows
└── assets/                 # Static assets
    ├── images/             # Screenshots, diagrams, visuals
    ├── icons/              # UI icons & symbols
    └── branding/           # Logos, brand guidelines, color palettes
```

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

---
*Maintained by the Customer Enablement Team · [Changelog](./CHANGELOG.md)*
