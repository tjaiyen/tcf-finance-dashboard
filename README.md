# Finance Automation Engine — Operations Dashboard

**Live: https://tjaiyen.github.io/tcf-finance-dashboard/**

A single, self-contained operations dashboard covering 23 cost-accounting and finance-automation
tools built for food/beverage manufacturing — seasonal standard-cost validation, margin-leak
recovery, vendor performance scoring, borrowing-base inventory eligibility, FSMA traceability,
a cross-tool AI insight synthesizer, a sub-ledger-to-GL variance tie-out, and more, all backed by
a shared KPI registry and a common flagging engine.

Every figure on the page comes from a real, deterministic run of the underlying tool against
synthetic sample data — nothing on the page is invented for display. See the disclaimer footer
on the page itself for the full statement.

## Getting started

Open the live link above. Click **Interview Mode** (top right) for a simplified view down to
5 tools, or explore the full sidebar — every tool has an Overview-panel summary, and `⌘K`
searches across all tools and findings.

## What's here

- **One file.** The entire dashboard is `index.html` — no build step, no server, no external
  JS framework. It's readable directly in a browser or from a static host.
- **Dark-first UI** with a live palette (Nocturne/Vivid/Mono) and density (Comfortable/Compact)
  switcher, a command palette (`⌘K`) that jumps to any tool or finding, and an **Interview
  Mode** toggle that collapses the view down to a short guided walkthrough.
- **23 tools** spanning cost accounting, AP/procurement, compliance, and operational readiness —
  reachable from the sidebar, with an Overview panel that rolls every tool's status up into one
  screen. Includes a bounded research pilot (Carbon-Adjusted Throughput) that's explicit about
  its own limits — see that tab's own disclosure, not a polished "finished feature." The two
  newest: GAAP Cost Compliance Checker (ASC 330-10-30-3 abnormal idle-capacity/spoilage
  disposition + ASC 330-10-35 lower-of-cost-or-NRV inventory valuation — checks whether a
  variance was disposed of correctly under GAAP, not just whether it's material) and Data
  Provenance Auditor (audits a claims manifest against real CSV rows, making this repo's own
  no-fabrication discipline runnable — distinguishing value-mismatch, no-matching-row, and
  missing-file as three separate failure modes).
- **Live threshold sliders** on 8 of the tools — drag a materiality band or price-variance
  ceiling and watch which rows flag change in real time, always paired with a "reset to the
  real value" button so the actual production threshold is never lost.
- **A guardrail sandbox** on the Cross-Tool Synthesis tab — build a hypothetical AI-generated
  recommendation from the real findings feed and watch it run through the same hallucination/
  coverage/priority-consistency checks the underlying tool's guardrails actually enforce.
- **A traceable architecture diagram** — click any data source or shared-layer box to highlight
  its exact data-flow path through the pipeline.

## What this isn't

This is a standalone snapshot published for sharing — it does not include the underlying Python
tools, tests, dbt pipeline, or any other project documentation. All data shown is synthetic
sample data, disclosed as such in the page's own footer. 18 of the 23 tools have an optional dbt
layer in the source repo (`tcf-engine-prep`, private); `gl_variance_tie_out`,
`carbon_adjusted_throughput_analyzer`, `ai_automation_cost_governor`,
`gaap_cost_compliance_checker`, and `data_provenance_auditor` are file-based only, no dbt layer
yet — a named follow-up, disclosed on their own tabs, not an oversight.
