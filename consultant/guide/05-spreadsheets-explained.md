# 05. The spreadsheets, explained

Rev 1 · 2026-11-04

You have four workbooks in `consultant/tools/`. This guide explains every sheet: what it is for, what you type, what it tells you, and how to read the warnings. Each one ships with a worked example (a bathroom renovation, job 2026-001) so you can see real numbers before you put in your own.

## Before you start: how to read any of these sheets

| You see | It means | What you do |
|---|---|---|
| **Blue text** | An input | Type over it |
| **Yellow fill** | A key assumption or a must-fill cell | Check it every time |
| **Black text** | A formula | Don't type over it. If you do, the sheet stops calculating. Undo (Ctrl+Z) |
| **Green text** | A number pulled from another sheet | Change it on the sheet it comes from |
| Red fill or a word in capitals (LATE, OVER BUDGET, EXPIRED) | A warning | Deal with it today |
| A little red triangle in a cell's corner | A note | Hover over it (on a computer) or tap it (on a phone) to read it |

**Dates:** type them as `2026-11-04` (year-month-day). That format works in every version of Excel and Google Sheets.

**Opening them:** Excel on a computer works best. Google Sheets works too: upload to Google Drive, then open with Google Sheets. On a phone use the Excel or Google Sheets app. Some example cells use `=TODAY()` so the example always looks recent; type real dates over them.

**One-time setup:** make a copy of each workbook before you put real numbers in. Keep the blank originals in `Company/Templates` (see SOP-15).

---

## 1. `estimator.xlsx`: price a job before you quote it

**Use it:** every time you price a job.

### Sheet: Assumptions
The settings the whole workbook uses.

| Cell | What it is | What to put |
|---|---|---|
| VAT rate | The Bahamas VAT rate, 10% | Leave it unless the law changes |
| VAT registered? | Are *you* registered for VAT? | **No** until you register. If No, the VAT you pay on materials counts as your cost |
| Target gross margin | The share of the price you keep to pay overhead and profit | 22% to start. Small jobs 30% to 40% (see Markup Margin sheet) |
| Contingency | Extra money for the unknown | 5% for clear work. 10% to 15% for renovation where you can't see inside walls |
| NIB rates, ceiling, minimum wage, overtime | Payroll rules | Leave them; check in January and July |
| Monthly overhead | What the business costs each month even with no job | Your real number: phone, fuel, insurance, software and so on |

### Sheet: Landed Cost
**What "landed cost" means:** the price of a thing once it is sitting on your site. That includes shipping it from Florida, insurance on the boat, customs duty, VAT charged at import, the customs broker, port fees, the truck to your site, and some breakage. A US$100 item can easily land at B$150 or more.

**How to use it:**
1. Top box, **Shipment cost:** type the freight quote for the whole shipment, the broker fee, port charges, trucking, and Family Island freight if any.
2. Item rows: type the item, quantity, unit, the Florida price per unit, and the **duty rate**. Get the duty rate from a licensed customs broker. The example rates are made up for illustration.
3. Type the local store's price per unit in "Local supplier price".
4. Read **"Cost per unit to you"** and **"Buy where?"**. It says Import or Local.
5. Read **"Landed cost as % above FOB"** at the bottom. In the example it's about 90%. That's why a Florida price on its own means nothing.

**Words:** FOB = the supplier's price before shipping. CIF = FOB plus freight plus insurance; customs duty is calculated on this. Duty = the tax on imports, set item by item.

**Example lesson:** the 24x24 tile lands at about B$3.88 a sq ft against B$5.25 locally, so you import it. Thinset lands at B$33.24 a bag against B$32 locally, so you buy it local. Heavy, cheap items rarely pay to import in small amounts.

### Sheet: Job Estimate
**Use it:** to build the price, line by line.

1. Type the project name and floor area at the top.
2. One row per work item: cost code, description, quantity, unit, then the cost per unit for material, labour or sub, and equipment or other. Get codes from `cost-code-book.xlsx`.
3. The sheet multiplies everything out and adds it up.
4. Read the summary on the right:

| Line | Means |
|---|---|
| Direct cost subtotal | What the work costs you |
| Contingency | Extra for unknowns (from Assumptions) |
| Total cost | Your full cost |
| Price before VAT = cost / (1 - margin) | The price that gives you your target margin. **Not** cost x 1.22; that's a common mistake (see Markup Margin) |
| Gross profit | Price minus cost |
| Equivalent markup | The same thing said as "% added to cost" |
| VAT | Only if you're registered |
| PRICE TO CLIENT | What goes on the quote |
| Price per sq ft | Compare with your past jobs. If it's way off, find out why before sending |
| Materials share | How much of the cost is materials. High means your deposit must be high |

**Example:** the bathroom costs B$8,872.50. At 22% margin the price is B$11,375 and the gross profit is B$2,502.50.

### Sheet: Markup Margin
**Markup** is a % added to cost. **Margin** is the % of the price you keep. They are different numbers:
- Cost B$100, add 25% markup, price B$125. You keep B$25, which is 20% of B$125. So **25% markup = 20% margin.**
- If you want a 20% margin and you only add 20%, you get 16.7%. Do that on every job and you lose a sixth of your profit without noticing.

**Bottom section:** type your salary, expected monthly revenue and profit target. It tells you the margin you actually need and warns if the Assumptions margin is too low. The example shows that 22% only covers overhead and salary at about B$22,700 a month of revenue, with nothing left as profit. That's why small jobs need 30% or more.

**Break-even revenue** is the sales you need each month just to stand still.

### Sheet: Cash Flow
**The question it answers:** does the payment schedule make you pay for the client's job out of your own pocket?

1. Price and cost come from Job Estimate automatically.
2. Type the payment stages and the % of price paid at each one. They must add up to 100%.
3. Type the % of total cost you'll have spent by the end of each stage. Materials are bought early, so the first stage is usually high.
4. Read **Cash position.** If any stage shows NEGATIVE, you're financing the client. Raise the deposit, add a stage, or have the client pay the supplier directly. Fix it **before** you sign.

### Sheet: Labour Cost
**Only for your own employees** (not subs). An employee costs more than their wage: you pay employer NIB of 6.65% on wages up to B$810 a week.
1. Type each person's hourly rate, normal hours and overtime hours.
2. Read "Your total weekly cost" and "Loaded cost per hour". Use the loaded rate, not the wage, when you price your own crew's work.
3. "Minimum wage check" warns if a rate is below B$6.50 an hour.

---

## 2. `cost-code-book.xlsx`: your filing system for costs

**What a cost code is:** a short number for a type of work, like `09-30` for tile. You put the same code on the estimate, the purchase, the sub's invoice and the receipt. Then you can see, line by line, whether you spent what you planned. Without codes you only find out at the end that you lost money, and you won't know where.

**How a code is written:** `09-30-S` means division 09 (Finishes), item 30 (tile), type S (subcontract). The types are M material, L your own labour, S subcontract, E equipment, O other.

### Sheet: Cost Codes
The full list, 123 codes in 15 divisions, each with its unit, what it includes, and a Bahamian "watch out". Read the whole list once. It doubles as a checklist of things you might forget to price.

### Sheet: Unit Cost Book
**Your own price database.** This is how you stop guessing.
1. Every time you get a written quote or pay a real price, add a row: code, specific item, unit, cost type, price, whether it includes VAT, supplier, island, quote date, valid-until date.
2. "Name" fills in from the code. "Age" counts days since the quote.
3. **Status:** OK, STALE (older than 90 days; change the limit in cell I2), EXPIRED (past valid-until date), or NO DATE.
4. When you estimate, look up the item here first. Use only OK prices. Re-quote anything STALE or EXPIRED.

After about 10 jobs, most of your estimate prices come from this sheet, and your estimates become fast and accurate.

### Sheets: Cost Types and Overhead Codes
**Overhead codes** (OH-10 to OH-99) are for company costs that belong to no single job: phone, insurance, licences, your salary. They go in `office-tracker.xlsx`, Monthly Money. Never put overhead on a job code, or your job profits will look worse than they are and your overhead will look smaller than it is.

---

## 3. `job-cost-tracker.xlsx`: is this job making money? (one copy per job)

**Make a copy for each job**, named like `2026-001 Smith Bathroom.xlsx`, and save it in that job's folder.

**The core idea, in four words:**
- **Budget:** what you planned to spend, from your estimate.
- **Committed:** what you've agreed to pay subs and suppliers (signed subcontracts and purchase orders).
- **Actual:** what has actually been invoiced or spent so far.
- **Forecast:** what the job will cost by the end = actual so far + cost to complete.

If Forecast is more than Budget on a line, you're losing money on that line. The tracker shows you the week it happens, while you can still do something.

### Sheet: Job Info
Type the job number, name, client, site, contract type, original price, dates, whether the client holds retention, and whether you're VAT registered.

The **Results** section updates itself. Read it every Friday:

| Result | How to read it |
|---|---|
| Forecast final cost | What the job will really cost |
| Forecast gross margin vs Estimated margin at bid | Did you keep the margin you priced? |
| Margin fade | Negative means the job is getting worse than you priced. Find the line on Budget & Cost Report |
| Billed / Paid / Owed | Money side of the job |
| Cash position on this job | Paid by client minus costs you've paid. **Negative = you're financing the job** |
| Billing check | Warns if you've spent more of the cost than you've billed. Send an invoice |

**Example:** forecast cost B$9,302.50 against a revised price of B$11,895, so the forecast margin is 21.8% against 22% at bid. Cash position is +B$750, so the job is paying for itself. One invoice is late.

### Sheet: Budget & Cost Report
1. One line per cost code on the job. Type the code; the name fills in.
2. **Original budget:** the cost (not the price) for that line from your estimate.
3. Approved change order budget, Committed and Actual fill in from the other sheets.
4. **Cost to complete:** every Friday, type your honest estimate of what's left to spend on that line. This is the only weekly typing on this sheet, and the most important.
5. Read **Forecast**, **Variance** and **Status**. OVER BUDGET lines are red.
6. The two checks at the bottom must show zero. If not, a receipt or PO has a code that isn't on the list; add that code as a line.

**Example lesson:** demolition (02-20) was budgeted at B$600 and cost B$650. It's over by B$50. Small, but it tells you to price demolition higher next time.

**Why forecast is never less than committed:** if you've signed a B$1,650 plumbing subcontract, that line will cost at least B$1,650, whatever you type as cost to complete.

### Sheet: Commitments
Every purchase order (PO-001, PO-002...) and subcontract (SC-001, SC-002...) the day you sign it: date, who, type, code, description, amount.

"Invoiced to date" fills in from Actual Costs (match the commitment number). "Remaining" is what's left to pay on it.

**Retention:** for subs, type 10% in Retention %. The sheet shows how much you're holding back. You release it when the work is accepted and the warranty period is clean (SOP-11).

### Sheet: Actual Costs
Every receipt and invoice, **the day you get it.** Date, supplier, invoice number, code, cost type, description, amount before VAT, VAT, commitment number (if it's against a PO or subcontract), and whether you've paid it.

"Job cost" works out VAT for you: if you're not VAT registered, the VAT you paid counts as cost.

Write the cost code on the paper receipt too, before you file it.

### Sheet: Change Orders
Every change, even ones not yet approved: number, date, description, status (Pending, Approved, Rejected), code, price to the client, your cost, days added.

Only **Approved** lines count toward the contract price and the budget. "Pending" turns yellow: it's not money until it's signed. Don't do the work until it's Approved (SOP-09).

If one change affects two codes, use two lines with the same CO number.

### Sheet: Billing
Every invoice you send the client: number, date, stage, amount before VAT, due date, and the paid amount and date when it comes in. VAT and retention fill in from Job Info.

Status shows Paid, Open, or **LATE: chase today**. Late means SOP-10 starts today, not next week.

Also copy each invoice into `office-tracker.xlsx` Receivables, so you see every client's debt in one place.

### Sheet: Sub Bids (bid leveling)
**What bid leveling is:** making three sub quotes comparable. Subs leave things out to look cheaper. If you pick the lowest number without checking, you pay for the missing pieces later.

1. Type the trade.
2. List every scope item the sub must do.
3. For each item, type what it would cost **you** to get it done if a bidder left it out.
4. For each bidder, type Y or N for every item, plus their base bid.
5. Type whether each bidder's documents are OK (business licence, NIB letter, insurance) and whether you checked references.
6. Read **Adjusted bid** and **Result**.

**Example:** Bidder 2 looks cheapest at B$1,050 but left out B$570 of work and has no documents. Bidder 1 comes out as the real low bid at B$1,410 adjusted. The cheapest number is not the cheapest job.

### Sheet: Look-Ahead
**What a look-ahead is:** a plan of the next three weeks, day by day, so subs, deliveries and inspections arrive in the right order.

1. Type the Monday the plan starts (cell D3).
2. One row per activity: what, who, code, start date, number of days. Saturdays count.
3. Orange bars fill in across the calendar.
4. Every Friday, update it and send a screenshot to every sub on the job.

Put inspections and deliveries on their own rows. They're the things that hold the job up.

---

## 4. `office-tracker.xlsx`: the business side (one file for the whole company)

### Sheet: Settings
Business name, the first month you track (type the first day of that month), VAT threshold (B$100,000), the warning level, how many months of overhead you keep in reserve, how old a sub's NIB letter can be, how many days before you follow up a quote, and whether you're VAT registered.

### Sheet: Leads & Quotes
**A lead** is anyone who might hire you. Log every one the day they contact you, even small jobs: date, name, phone, **source** (how they found you), area, job type, site visit date, quote number, quote date, amount, status, next follow-up.

The **Action** column says FOLLOW UP when a quote has waited 5 days (change this in Settings) or the follow-up date has arrived. Most jobs go to the contractor who follows up, not the cheapest one.

**Summary** (right side):
- **Win rate:** quotes won divided by quotes decided. 25% to 40% is healthy. Winning almost everything usually means you're too cheap.
- **Leads by source:** where your work actually comes from. Spend your marketing time there.

### Sheet: Receivables
**Receivables** = money owed to you. Every invoice, all jobs: number, client, job, client type (Private, Commercial, Government), dates, amount, paid to date.

"Bucket" sorts each invoice by how late it is: Current, 1-30 late, 31-60, 61-90, 90+. The summary shows the total in each bucket and how much of it is government.

**Example lesson:** B$8,400 of the B$11,243.75 owed is from government, 75% of it. Government pays slowly. If too much of your money is stuck there, you can't pay subs. Keep it under about a third.

### Sheet: Monthly Money
24 months side by side. At each month end type:
- Revenue invoiced that month (before VAT)
- Job costs that month
- Each overhead line by OH code
- Cash in the bank at month end, tax account balance, and what you're owed

It works out gross profit, total overhead, **net profit**, and whether your cash covers the reserve target (overhead x 3 months).

**Example lesson:** the example business earns B$1,550 to B$2,475 of gross profit a month but spends B$2,555 to B$3,435 on overhead, so it **loses money every month** while it looks busy. The fix is not "work harder". It's raise margins, cut overhead, or do more volume at the same overhead. This sheet is where you see that.

### Sheet: VAT Threshold
Pulls revenue from Monthly Money and adds up every **rolling 12 months**: this month plus the 11 before it. That's how the B$100,000 VAT registration test works.

Status says "Getting close" at 80% and "OVER THRESHOLD: register now" above B$100,000. Confirm the exact test and timing with the Department of Inland Revenue.

**Why it matters:** if you pass the threshold and don't register, you can end up owing VAT you never charged. That comes straight out of your profit.

### Sheet: Subs & Documents
Every sub: trade, contact, island, and the **dates** on their business licence, NIB letter and insurance, when you last checked their crew are legally allowed to work, and whether a subcontract is signed.

Status says OK, MISSING DOCUMENTS, EXPIRED: do not use or pay, NIB letter too old, Expiring within 30 days, or No signed subcontract.

**Check it before every new job and every payment** (SOP-04 and SOP-11). If a sub with expired insurance has an accident on your job, it becomes your problem.

---

## Weekly and monthly rhythm

| When | Do |
|---|---|
| Every day on a job | Actual Costs: enter receipts |
| Monday | Leads & Quotes: do every FOLLOW UP. Receivables: chase anything late |
| Friday | Job tracker: Cost to complete, read Job Info results, update Look-Ahead and send it. Billing: invoice any milestone reached |
| Month end | Monthly Money, VAT Threshold, Subs & Documents. Move tax money to the tax account (SOP-14) |
| Every quote | Unit Cost Book: log new prices; re-quote STALE ones |
| January and July | Estimator Assumptions: check VAT, NIB and minimum wage are still right |
