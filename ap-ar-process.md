# Accounts Payable & Accounts Receivable Process Flow

## Accounts Payable (AP) — Procure-to-Pay Perspective

1. **Purchase order created** in Materials Management (MM) — not FI, but the process starts here.
2. **Goods receipt posted** against the purchase order.
3. **Invoice verification** (`MIRO`) — the vendor invoice is matched against the PO and goods receipt (the "three-way match": PO, goods receipt, invoice).
4. **Invoice posted to FI** — this creates the vendor open item and updates the G/L (expense or stock account, plus the vendor payable account).
5. **Payment run or manual payment** (`F-53` or the automatic payment program `F110`) clears the vendor open item.
6. **Line item review** (`FBL1N`) shows open and cleared items for the vendor.

**Key idea:** AP in SAP is rarely FI-only — invoice verification usually flows in from MM, which is why FI/CO consultants need at least a working understanding of the procurement side.

## Accounts Receivable (AR) — Order-to-Cash Perspective

1. **Sales order created** in Sales and Distribution (SD).
2. **Goods delivered and billed** — billing document created in SD, which triggers an FI posting.
3. **Customer invoice posted to FI** — creates the customer open item (receivable) and revenue posting.
4. **Payment received** (`F-28`) — incoming payment is posted and matched against the open invoice.
5. **Line item review** (`FBL5N`) shows the customer's open and cleared items.
6. **Dunning** (if payment is late) — SAP's dunning program (`F150`) generates reminder letters based on configurable dunning levels.

**Key idea:** like AP, AR is fed by another module (SD), so postings in FI are often the downstream result of a process that started elsewhere.

## Why this matters for a consultant

A big part of FI/CO consulting is understanding these cross-module chains — knowing that an FI posting didn't necessarily start in FI helps when troubleshooting or designing a process, since the root cause of an issue in AP or AR can sit upstream in MM or SD.
