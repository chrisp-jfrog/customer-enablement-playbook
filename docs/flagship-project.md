---
layout: default
title: Flagship Project
description: Architecture and design of the Customer Enablement Playbook — a structured repository system for scalable CS enablement.
permalink: /flagship-project/
---

<div class="page-wrapper wide">

  <div class="hero">
    <p class="hero-kicker">Case Study</p>
    <h1>Customer Enablement<br><em>Playbook</em></h1>
    <p class="hero-lead">
      A structured repository system that replaced scattered docs, Notion wikis, and individual heroics with a single, versioned source of truth for customer success.
    </p>
  </div>

  <div class="badge-row">
    <span class="badge"><span class="badge-dot green"></span>Live on GitHub Pages</span>
    <span class="badge"><span class="badge-dot"></span>Jekyll + Markdown</span>
    <span class="badge"><span class="badge-dot"></span>Apache 2.0</span>
    <span class="badge"><span class="badge-dot warm"></span>5 phases · 40+ checkpoints</span>
  </div>

  <h2>The Problem It Solves</h2>
  <p>
    Before this system existed, customer-facing teams operated from a fragmented patchwork of shared drives, Notion pages, and email threads. Each CSM had their own version of the onboarding checklist. Escalation procedures lived in someone's head. New hires spent their first four weeks piecing things together from Slack history.
  </p>
  <p>
    The result: inconsistent customer experiences, slow ramp times, and no institutional memory when someone left.
  </p>

  <h2>Architecture</h2>
  <p>
    The repository is designed around three principles: <strong>findability</strong> (you can navigate to any resource in under 10 seconds), <strong>composability</strong> (components and templates are modular, not monolithic), and <strong>version control</strong> (every change is tracked, every edit has a history).
  </p>

  <div class="arch-diagram">

    <div class="arch-layer">
      <span class="arch-label">Delivery</span>
      <div class="arch-boxes">
        <span class="arch-box accent">GitHub Pages (Jekyll)</span>
        <span class="arch-box accent">Portfolio Site</span>
        <span class="arch-box">Raw Markdown (GitHub)</span>
      </div>
    </div>

    <div class="arch-arrow">↑ rendered from</div>

    <div class="arch-layer">
      <span class="arch-label">Content</span>
      <div class="arch-boxes">
        <span class="arch-box warm">Onboarding Checklist</span>
        <span class="arch-box warm">Escalation Runbook</span>
        <span class="arch-box warm">Email Templates</span>
        <span class="arch-box">Reference Docs</span>
        <span class="arch-box">Guides</span>
      </div>
    </div>

    <div class="arch-arrow">↑ lives in</div>

    <div class="arch-layer">
      <span class="arch-label">Structure</span>
      <div class="arch-boxes">
        <span class="arch-box">/docs</span>
        <span class="arch-box">/src/templates</span>
        <span class="arch-box">/src/components</span>
        <span class="arch-box">/assets</span>
      </div>
    </div>

    <div class="arch-arrow">↑ governed by</div>

    <div class="arch-layer">
      <span class="arch-label">Governance</span>
      <div class="arch-boxes">
        <span class="arch-box">CONTRIBUTING.md</span>
        <span class="arch-box">Issue Templates</span>
        <span class="arch-box">PR Template</span>
        <span class="arch-box">SECURITY.md</span>
        <span class="arch-box">CODE_OF_CONDUCT.md</span>
      </div>
    </div>

  </div>

  <h2>Repository Structure</h2>
  <p>
    The top-level layout separates source content (<code>/src</code>), documentation (<code>/docs</code>), and static assets (<code>/assets</code>). The Jekyll site is served directly from <code>/docs</code>, which means GitHub Pages can be enabled without a separate branch.
  </p>

<pre><code>customer-enablement-playbook/
├── docs/                  ← Jekyll site root (GitHub Pages source)
│   ├── _config.yml        ← Theme, nav, build settings
│   ├── _layouts/          ← default.html wrapper
│   ├── assets/css/        ← style.scss
│   ├── index.md           ← About / TSM narrative
│   ├── flagship-project.md
│   ├── playbooks.md
│   ├── guides/
│   │   ├── escalation-runbook.md
│   │   └── email-templates.md
│   └── onboarding/
│       └── customer-onboarding-checklist.md
├── src/
│   ├── components/        ← Reusable content blocks
│   ├── templates/         ← Playbook templates
│   └── scripts/           ← Automation utilities
├── assets/
│   ├── images/
│   ├── icons/
│   └── branding/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE/
├── README.md
├── LICENSE                ← Apache 2.0
├── SECURITY.md
├── CODE_OF_CONDUCT.md
└── CONTRIBUTING.md</code></pre>

  <h2>Key Design Decisions</h2>

  <table>
    <thead>
      <tr>
        <th>Decision</th>
        <th>Rationale</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Jekyll over a heavier SSG</strong></td>
        <td>Native GitHub Pages support — no CI/CD pipeline required. Zero-config deploy from <code>/docs</code>.</td>
      </tr>
      <tr>
        <td><strong>Markdown-first content</strong></td>
        <td>CSMs can edit content directly on GitHub without leaving the browser. No CMS login required.</td>
      </tr>
      <tr>
        <td><strong>Pages served from <code>/docs</code></strong></td>
        <td>Keeps the portfolio and the source content in the same branch, eliminating branch-sync drift.</td>
      </tr>
      <tr>
        <td><strong>Custom CSS over theme defaults</strong></td>
        <td>Minimal theme as a base; custom SCSS override for typography, layout, and component system.</td>
      </tr>
      <tr>
        <td><strong>Apache 2.0 license</strong></td>
        <td>Permissive for internal reuse and forks by other CS teams; patent protection clause adds coverage.</td>
      </tr>
      <tr>
        <td><strong>Issue + PR templates</strong></td>
        <td>Structured contribution reduces review friction and enforces content quality standards at submission time.</td>
      </tr>
    </tbody>
  </table>

  <h2>Screenshots</h2>
  <p>
    Drop real screenshots into <code>/assets/images/</code> and update the <code>src</code> attributes below to go live.
  </p>

  <div class="screenshot-grid">
    <div class="screenshot">
      <div class="screenshot-mock">About / Home page</div>
      <div class="screenshot-caption">TSM narrative, stats, and navigation cards</div>
    </div>
    <div class="screenshot">
      <div class="screenshot-mock">Onboarding Checklist</div>
      <div class="screenshot-caption">5-phase checklist with escalation triggers</div>
    </div>
    <div class="screenshot">
      <div class="screenshot-mock">Escalation Runbook</div>
      <div class="screenshot-caption">SEV-1–4 definitions, SLAs, and flow diagrams</div>
    </div>
    <div class="screenshot">
      <div class="screenshot-mock">Email Templates</div>
      <div class="screenshot-caption">8 approved templates from welcome to incident ack</div>
    </div>
  </div>

  <h2>How to Enable GitHub Pages</h2>

  <p>Once pushed to GitHub, enabling the site takes under a minute:</p>

  <ol>
    <li>Go to your repository → <strong>Settings</strong> → <strong>Pages</strong></li>
    <li>Under <em>Source</em>, set branch to <code>main</code> and folder to <code>/docs</code></li>
    <li>Click <strong>Save</strong></li>
    <li>Your site will be live at <code>https://chrisp-jfrog.github.io/customer-enablement-playbook</code> within 2–3 minutes</li>
  </ol>

  <p>
    To use a custom domain, add a <code>CNAME</code> file to <code>/docs</code> containing your domain (e.g. <code>enablement.yourcompany.com</code>) and configure your DNS.
  </p>

  <hr>

  <div class="card-grid">
    <a class="card" href="{{ '/playbooks/' | relative_url }}">
      <span class="card-icon">📋</span>
      <h4>Browse the Playbooks</h4>
      <p>Onboarding checklists, escalation runbooks, and email templates — ready to use.</p>
      <span class="card-link">Go to Playbooks →</span>
    </a>
    <a class="card" href="{{ '/' | relative_url }}">
      <span class="card-icon">👤</span>
      <h4>About the Author</h4>
      <p>TSM background, technical skills, and the philosophy behind this work.</p>
      <span class="card-link">Read the story →</span>
    </a>
  </div>

</div>
