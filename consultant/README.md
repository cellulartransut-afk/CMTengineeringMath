# Bahamas Contracting Consultant

An AI consultant with the experience of a 50-year Bahamian superintendent and project manager, set up to build one business from zero: a paper contracting company started at 18, grown into a general contractor, then into a business that owns assets.

## What's here

| Path | What it is |
|---|---|
| `../.claude/agents/bahamas-contracting-consultant.md` | The consultant: who it is, how it talks, the rules it works by |
| `knowledge/01-roadmap.md` | The plan: stages from paper contractor to owner, with gates and money math |
| `knowledge/02-bahamas-rules.md` | Licensing (Contractors Act status), company setup, business licence, VAT, NIB, labour, permits, code, procurement, funding, sources |
| `knowledge/03-contracts.md` | Contract types, clause checklist, exclusions, change orders, subcontracts, red flags |
| `knowledge/04-estimating-and-materials.md` | Estimating method, takeoff rules, landed cost, shipping, lead times, specs for salt, wind and termites |
| `knowledge/05-field-playbook.md` | PM and super systems: sequence, quality hold points, daily routine, safety, hurricane plan, closeout |
| `knowledge/06-money.md` | Markup vs margin, overhead, cash flow, books, insurance, bonds, turning profit into assets |
| `knowledge/07-cost-codes.md` | The cost code book: 123 job codes in 15 divisions, cost types, overhead codes |
| `operations-manual/` | **The SOPs your company runs on**, 16 of them. `00-index.md` explains the system and how long each document lasts before it needs rewording |
| `templates/` | Contracts (short form, small works, time and materials, maintenance service, subcontract), `contract-guide.md` (which to use when), change order, proposal, invoice, notice letters, receipts and releases, daily report, checklists |
| `guide/` | **The beginner's guide.** Start at `guide/00-start-here.md`. Glossary, every checklist explained, how a house gets built, business setup, spreadsheets, contracts, a job start to finish |
| `tools/estimator.xlsx` | Landed cost, job estimate, markup/margin, cash flow and labour cost (NIB) |
| `tools/cost-code-book.xlsx` | Cost codes plus your unit cost book (your own dated prices; old ones flagged) |
| `tools/job-cost-tracker.xlsx` | One copy per job: budget vs actual vs forecast, POs and subcontracts, receipts, change orders, billing, sub bid comparison, 3-week look-ahead |
| `tools/office-tracker.xlsx` | Leads and win rate, who owes you, monthly profit, VAT threshold warning, sub document expiry |
| `my-business/` | Your business profile, sub bench and job log. The consultant reads these first and keeps them updated |

## How to use it

### In Claude Code (this repository)
Ask normally. Claude hands construction business questions to the consultant automatically. To call it directly, type `@` and pick `bahamas-contracting-consultant`, or say "Use the contracting consultant to ...". In Claude Code it can read the knowledge files, search the web for current rates, draft documents and save them into `my-business/`.

Examples:
- "Price a 12 x 14 ft block addition in Carmichael, with a shingle roof."
- "Draft a subcontract for a tile setter on the Smith bathroom job, B$2,800 lump sum."
- "A client wants to pay 10% deposit. What do I do?"
- "Build me a 3-week look-ahead for a slab-to-roof sequence."
- "Should I register for VAT now?"

### In the Claude app (phone or web), as a Project
1. Create a new Project called "Contracting Consultant".
2. Open `../.claude/agents/bahamas-contracting-consultant.md`. Copy everything from `# Who you are` to the end. Paste it into the Project's instructions.
3. Upload to the Project's knowledge: everything in `knowledge/`, `operations-manual/`, `templates/`, `guide/` and `my-business/`. Keep the `.xlsx` files on your phone or computer to use in Excel or Google Sheets.
4. Ask questions in chats inside that Project.
5. In a Project the consultant can't save files. When it gives you an update for `my-business/profile.md`, paste it in and re-upload the file.

## Keep it current
- Rates and laws in `knowledge/02-bahamas-rules.md` are as of 2026-11-03. The big ones to watch: the Construction Contractors Board being appointed, NIB rates (new rates were expected from 1 July 2026), the 2025 VAT changes on B$1M+ construction, and the Building Code 4th edition.
- Every 6 months, ask the consultant: "Check every rate and law in 02-bahamas-rules.md against current sources and update it."

## Limits
The consultant drafts contracts and gives full working answers, then tells you what a Bahamian attorney, accountant or engineer must check. Have an attorney review the small works contract and subcontract templates once before first use. Structural design comes from stamped drawings.
