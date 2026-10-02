# CFO Dashboard — layout draft
Status: DRAFT (2 Oct 2026). Not written to any Sheet. Needs Founders' approval.
Sheet: "CFO Dashboard" in /MIRA/finance. Shared with: Virgo CFO, Founders.
Scope (ROLES.md): cash, AR/AP, margins, bank balances. Nothing else.

## Tabs
1. Summary      — the one screen the CFO opens
2. Cash         — bank balances and daily cash flow
3. Receivables  — what customers owe, by age
4. Payables     — what Virgo owes, by due date
5. Margins      — revenue, cost and gross margin
6. Checks       — reconciliation flags
7. Data         — raw imports (hidden, never edited by hand)

## 1. Summary
Top strip (8 tiles, 2 rows of 4):
- Cash in bank today (all accounts)
- Net cash flow, last 7 days
- Cash runway (days of payables covered)
- Receivables total
- Receivables > 60 days (% of total)
- Payables due next 7 days
- Gross margin, month to date
- Days sales outstanding (DSO)

Each tile: value · change vs last week · green/amber/red.
Below the tiles:
- Chart: cash balance, last 13 weeks (line)
- Chart: receivables by age bucket (bar)
- Chart: gross margin % by month, last 6 months (line)
- "Watch" box: up to 3 items MIRA flags
- Footer: data as of [date/time] · source files

## 2. Cash
Columns: Date · Bank · Account (last 4 digits only) · Opening · Inflows · Outflows · Closing
- One row per account per day
- Total row per day; closing must equal next day's opening (flag in Checks)

## 3. Receivables
Columns: Customer (company name) · Invoiced · Received · Outstanding ·
0–30 · 31–60 · 61–90 · 90+ · Oldest invoice date
- Company names only — no contact person, phone, email or address
- Totals row; DSO at top
- Collections column pulled from Sales Dashboard via IMPORTRANGE (totals only)

## 4. Payables
Columns: Supplier category · Supplier · Due this week · Due next week ·
Due 15–30 days · Overdue · Total
- Statutory dues (GST, TDS, PF etc.) as their own rows so they are never missed

## 5. Margins
Columns: Month · Product/line · Revenue · Cost of goods · Gross margin · GM %
- Cost of goods can use plant production cost from Plant Dashboard via
  IMPORTRANGE (totals only), once that Sheet exists

## 6. Checks (MIRA fills, CFO reviews)
- AR movement = invoices − collections? (difference shown)
- Bank closing = next day opening?
- Collections here = collections on Sales Dashboard?
- Any number older than 2 days → marked STALE
Each check: OK / FLAG + one-line reason.

## 7. Data (hidden)
- One block per export file from /MIRA/finance, pasted as-is
- Columns added: source file name, import date
- All other tabs read from here by formula — nobody types numbers into them

## Colour rules (proposed, CFO to confirm)
- Cash runway: red < 15 days, amber 15–30, green > 30
- Receivables > 60 days: red > 20%, amber 10–20%, green < 10%
- GM %: red if down > 3 points vs last month

## Needed from the CFO before building
1. Which system the exports come from (e.g. accounting software, bank statements)
2. Currency and number format (assumed INR, lakhs/crores?)
3. Real thresholds for the colour rules
4. Which product lines to show in Margins
