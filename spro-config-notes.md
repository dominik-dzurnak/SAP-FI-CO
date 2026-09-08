# Navigating SPRO/IMG for FI/CO Configuration

## What SPRO is

`SPRO` opens the **Implementation Guide (IMG)**, SAP's structured tree of configuration activities. Rather than one big settings screen, the IMG organizes configuration hierarchically by module and sub-process — a functional consultant spends a large share of their time navigating this tree.

## How the FI/CO section is structured (high level)

```
SPRO
└── SAP Reference IMG
    ├── Financial Accounting (FI)
    │   ├── Financial Accounting Global Settings
    │   │   ├── Company Code (definition, global parameters)
    │   │   ├── Fiscal Year Variant
    │   │   └── Posting Periods
    │   ├── General Ledger Accounting
    │   │   ├── Master Data (chart of accounts, G/L account creation)
    │   │   └── Business Transactions
    │   ├── Accounts Receivable and Payable
    │   │   ├── Customer/Vendor Account Groups
    │   │   └── Payment Terms
    │   └── ...
    └── Controlling (CO)
        ├── General Controlling
        │   └── Controlling Area (definition, assignment to company codes)
        ├── Cost Center Accounting
        │   ├── Master Data
        │   └── Planning
        └── ...
```

## Key global settings a consultant configures early

- **Company code** (`OBY6`) — the legal entity for which financial statements are drawn up; almost everything else references it.
- **Controlling area** — links to one or more company codes and defines the scope for cost accounting.
- **Fiscal year variant** — defines how the fiscal year is split into posting periods (calendar year, non-calendar, or 4-4-5 patterns).
- **Chart of accounts** — the list of G/L accounts available, assigned to a company code.

## Practical note

Configuration in SPRO is typically transported through a landscape (Development → Quality → Production) rather than made directly in a live system. Understanding this transport concept is as important as knowing where a given setting lives in the IMG tree.
