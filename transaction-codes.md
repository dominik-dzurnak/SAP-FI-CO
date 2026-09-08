# FI/CO Transaction Codes Reference

A grouped overview of the transaction codes most commonly used in FI/CO functional work.

## General Ledger (FI-GL)

| T-Code | Description |
|---|---|
| `FB50` | Enter G/L account document (single screen) |
| `FB01` | Post a general ledger document |
| `FB03` | Display a posted document |
| `FBL1N` | Vendor line item display |
| `FBL3N` | G/L account line item display |
| `FBL5N` | Customer line item display |
| `F-02` | General posting (classic transaction) |

## Accounts Payable (FI-AP)

| T-Code | Description |
|---|---|
| `FK01` | Create vendor master record |
| `FK02` | Change vendor master record |
| `FK03` | Display vendor master record |
| `MIRO` | Enter incoming invoice (Logistics Invoice Verification) |
| `MIR4` | Display invoice document |
| `MIR7` | Park invoice (for later verification) |
| `F-53` | Post outgoing payment |

## Accounts Receivable (FI-AR)

| T-Code | Description |
|---|---|
| `FD01` | Create customer master record (accounting view) |
| `FD02` | Change customer master record |
| `F-28` | Post incoming payment |
| `FBL5N` | Customer line item display |

## Controlling (CO)

| T-Code | Description |
|---|---|
| `KS01` | Create cost center |
| `KS02` | Change cost center |
| `KS03` | Display cost center |
| `KSB1` | Display cost center actual line items |
| `KSU5` | Cost center report — actual/plan comparison |

## Configuration

| T-Code | Description |
|---|---|
| `SPRO` | Access the Implementation Guide (IMG) |
| `OB08` | Maintain exchange rates |
| `OBY6` | Maintain company code global parameters |

## 💡 Tips

- `FBL1N`, `FBL3N`, and `FBL5N` follow a consistent naming pattern: the letter after "FBL" indicates the account type (1 = vendor, 3 = G/L, 5 = customer).
- The `MIRO` family handles invoice verification against purchase orders, linking FI to Materials Management (MM).
- Most master data transactions follow the `01/02/03` pattern: create, change, display.
