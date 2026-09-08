# Cost Center Accounting (CO-CCA)

## What a cost center represents

A cost center is an organizational unit within Controlling that represents where costs are incurred — a department, a team, a function (e.g. "IT Support", "Production Line 1", "Marketing"). It answers the question: *where did this cost happen?*, as opposed to a cost element, which answers *what kind of cost is this?*

## Core master data

- **Cost center** (`KS01`/`KS02`/`KS03`) — the organizational unit itself, assigned to a controlling area and company code, with a validity period.
- **Cost element** — the CO-side counterpart to a G/L account; primary cost elements mirror expense accounts from FI, secondary cost elements exist only in CO (used for internal allocations).
- **Cost center group** — a hierarchical grouping of cost centers for reporting (e.g. all cost centers under "Administration").

## Typical postings that hit a cost center

- Primary postings from FI (e.g. a vendor invoice posted against a cost center as the "account assignment")
- Internal allocations between cost centers (assessments, distributions)
- Activity allocations (e.g. machine hours or labor hours charged from one cost center to another)

## Actual vs. Plan

Cost Center Accounting is built around comparing **actual costs** (what was really spent, from postings) against **planned costs** (budgeted or forecasted amounts entered via planning transactions). The report `KSU5` and similar reports show this actual/plan comparison, which is one of the most common outputs a controller reviews.

## Why this matters for FI/CO integration

Every relevant FI posting (an invoice, a goods issue, a payroll cost) can carry a CO account assignment — most commonly a cost center. This is what links the "financial" side (what was posted, in which G/L account) to the "management accounting" side (which department or function is responsible for that cost). Understanding this link is central to FI/CO consulting, since it's the mechanism that makes internal cost reporting possible.
