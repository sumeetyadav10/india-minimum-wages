# Minimum wages in India — every state and UT, with the official order

A machine-readable table of the **minimum wage rates in force in each Indian state, union territory and the central sphere**, with the official order behind every figure (name, link) and the date it was last checked against that order.

- **File:** [`data/india-minimum-wages.csv`](data/india-minimum-wages.csv) — 35 jurisdictions, one row per category of work × skill level
- **Maintained by:** [msmetools.com](https://msmetools.com/in/payroll/minimum-wages) (edited by Sumeet Yadav, Goa). Rates are re-checked against the state labour departments' orders on a rolling schedule; a revision is added after the new order is read.
- **Updated:** this repository copies the published CSV once a day (see `.github/workflows/update.yml`), so the commit history is also a history of revisions.
- **Licence:** [CC BY 4.0](LICENSE). Please credit "msmetools.com — Minimum wages in India" with a link to https://msmetools.com/in/payroll/minimum-wages.

## Columns

| Column | Meaning |
|---|---|
| `state`, `state_code` | State/UT name and short code (`central` = central sphere) |
| `category` | Category of work / zone as named in the order |
| `skill_level` | Unskilled, semi-skilled, skilled, highly skilled, or the order's own grade |
| `monthly_inr`, `daily_inr` | Minimum wage in rupees |
| `monthly_basis`, `daily_basis` | `order` = printed in the order; otherwise how it was derived (e.g. `monthly rate / 26`) |
| `in_force_from`, `period_end` | Period the rates apply to (`period_end` empty when the order states none) |
| `revision_status` | `current`, `pending` (latest scheduled revision not yet notified) or `overdue` (two or more missed) |
| `next_revision_due` | Next scheduled revision date (or the missed one, for pending/overdue) |
| `official_order`, `official_order_url` | The order the rates come from, and where to read it |
| `last_verified` | Date the figures were last checked against that order |
| `page_url` | The state's page on msmetools.com with the full tables, worked examples and history |

## Notes

- Minimum wages apply by where the employee works. Many states fix several zones and dozens of scheduled employments; this file carries the categories shown on each state's page, not every schedule.
- Always pay at least the rate in the latest official order. If an order here is out of date, please [open an issue](../../issues) with a link to the newer order.
- This is not a government publication.
