# Finance Automation Engine — Operations Dashboard

**Live: https://tjaiyen.github.io/tcf-finance-dashboard/**

A single, self-contained operations dashboard covering 14 cost-accounting and finance-automation
tools built for food/beverage manufacturing — seasonal standard-cost validation, margin-leak
recovery, vendor performance scoring, borrowing-base inventory eligibility, FSMA traceability,
and more, all backed by a shared KPI registry and a common flagging engine.

Every figure on the page comes from a real, deterministic run of the underlying tool against
synthetic sample data — nothing on the page is invented for display. See the disclaimer footer
on the page itself for the full statement.

## What's here

- **One file.** The entire dashboard is `index.html` — no build step, no server, no external
  JS framework. It's readable directly in a browser or from a static host.
- **Dark-first UI** with a live palette (Nocturne/Vivid/Mono) and density (Comfortable/Compact)
  switcher, a command palette (`⌘K`) that jumps to any tool or finding, and an **Interview
  Mode** toggle that collapses the view down to a short guided walkthrough.
- **14 tools** spanning cost accounting, AP/procurement, compliance, and operational readiness —
  reachable from the sidebar, with an Overview panel that rolls every tool's status up into one
  screen.

## What this isn't

This is a standalone snapshot published for sharing — it does not include the underlying Python
tools, tests, dbt pipeline, or any other project documentation. All data shown is synthetic
sample data, disclosed as such in the page's own footer.
