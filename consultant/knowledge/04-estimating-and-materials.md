# 04. Estimating and materials

As of 2026-11-03. Prices here are illustrations. Your prices come from your own quotes, logged in your own cost book.

## First principle

An estimate is a prediction of what the job will cost you. Price comes after. If the cost prediction is wrong, no markup saves you. Most bad estimates fail by **missing items**, not by wrong unit prices. So the method is built to catch missing items.

## The method, in order

1. **Read everything.** Drawings, scope, client's notes. Write questions.
2. **Walk the site.** Access for trucks, where materials go, power and water, neighbours, slope, existing damage, photos of everything.
3. **Break the job into work items** in construction sequence (demolition, foundation, walls, roof, openings, MEP, finishes, cleanup). Use the sequence in `05-field-playbook.md` as your checklist.
4. **Take off quantities** for each item. Show the math.
5. **Price each item:** materials (landed and delivered), labour or sub quote, equipment.
6. **Add general conditions:** the cost of running the job (list below).
7. **Add contingency:** 3% to 5% for clear scope, 10% to 15% for renovation with unknowns.
8. **Add overhead and profit** (see `06-money.md`).
9. **Add VAT** if you are registered.
10. **Write the scope, inclusions and exclusions** into the quote.
11. **Check:** compare cost per square foot or per room against your past jobs. If it is far off, find out why before sending.

## Takeoff rules of thumb (check against drawings)

| Item | Rule |
|---|---|
| Concrete volume | Length x width x depth in feet / 27 = cubic yards. Add 5% to 10% waste. |
| 8 x 8 x 16 concrete block | 1.125 blocks per square foot of wall (112.5 per 100 sq ft). Deduct openings. Add 5% waste. |
| Block wall area | Wall length x height, minus window and door openings |
| Grouted cores | Cores at every vertical bar location per drawings (corners, openings, at spacing shown). Volume per filled core of 8 inch block is roughly 0.22 to 0.25 cu ft per foot of height; get the exact figure for the block you buy. Add 10% to 15% for waste and blowout. |
| Rebar | Count bars per drawing; add lap lengths as specified by the engineer (often 40 to 48 bar diameters); add 5% to 10% waste |
| Plaster or stucco | Wall area both faces where specified; sand and cement by mix ratio; add 10% |
| Paint | Area / coverage per gallon (often 350 to 400 sq ft per coat) x number of coats. Primer separate. |
| Tile | Floor or wall area + 10% to 15% (more for diagonal or large-format) |
| Drywall | Area / 32 for 4 x 8 sheets + 10% |
| Roof sheathing | Roof area (plan area x slope factor) / 32 + 10% |
| Shingles | Roof area / 100 = squares; + 10% to 15% for hips, valleys, waste |
| Lumber | Count members from framing plan; + 10% |

## Landed cost: the Bahamian reality

Almost all building materials are imported, mostly from Florida. The shelf price is not your cost. The landed, delivered price is.

```
FOB price (supplier in Florida)
+ freight to Nassau (or Freeport)
+ marine insurance
= CIF value

Customs duty = CIF x duty rate (set by the Tariff Act, varies by item)
Import VAT  = (CIF + duty) x 10%    (confirm the base with your broker)
+ customs broker fee
+ port, wharfage and handling charges
+ trucking from port to site
+ Family Island freight (mailboat or barge) if applicable
+ breakage and loss allowance (2% to 5%)
= LANDED COST, delivered to site
```

Use the **Landed Cost** sheet in `consultant/tools/estimator.xlsx`.

**When to buy local, when to import:**
- Small quantities, stock items, urgent: buy local. Local suppliers have already paid freight, duty and VAT; their margin is often less than your small-shipment costs.
- Big packages (windows and doors, cabinets, tile for a whole house, roofing for a whole house, full container): get a Florida quote, land it on paper, compare with the local quote. Use whichever is cheaper landed, after counting lead time and risk.
- Always ask the client if they have a duty concession (first-time homeowner, hotel or resort encouragement act, Freeport Port Authority licensee, Family Island development concession). Their concession can make materials cheaper. The paperwork must be in their name and done right.

**Duty:** rates come from the First Schedule of the Tariff Act and vary by item. Some building materials were cut in 2022 (roofing, plumbing, electrical). Customs' 2018 frequently imported list showed Portland cement duty-free. Check the Bahamas Customs duty calculator or ask a licensed broker before every import estimate. Do not use a single "building materials" rate.

## Shipping

- **Florida to Nassau and Freeport:** several sailings a week from South Florida ports (Port Everglades, Miami, Palm Beach) and Jacksonville. Carriers that run the route include Tropical Shipping, Crowley and Seaboard Marine. Florida consolidators take less-than-container (LCL) loads. Get two quotes per shipment.
- **Family Islands:** mailboats from Potter's Cay, Bahamas Ferries freight, or a chartered barge or landing craft for large loads. Schedules depend on weather and the boat. Plan for delays, breakage and double handling.
- **Customs broker:** use a licensed broker. Their fee is cheap insurance against wrong classification, delays and penalties.

## Lead times (typical; confirm every time)

| Item | Typical lead time to Nassau |
|---|---|
| Stock materials at a local yard | Same day to 3 days |
| Special order from a Florida supplier | 2 to 4 weeks |
| Roof trusses | 2 to 6 weeks |
| Impact-rated windows and doors | 8 to 16 weeks |
| AC equipment, generators | 2 to 8 weeks (longer before hurricane season) |
| Custom cabinets and countertops | 4 to 10 weeks |
| Family Islands | Add 1 to 3 weeks to any of the above |

Order long-lead items the week the contract is signed and the deposit clears. Put lead times on the schedule.

## Buying from local suppliers

- Open trade accounts with two or three lumber yards and hardware suppliers on your island (directories list many in Nassau, for example Kelly's, Western Hardware and Lumber, Commonwealth Building Supplies, Cartwright Building Supplies; Freeport and the Family Islands have their own). Ask for contractor pricing and delivery terms.
- Get quotes in writing with validity dates (often 7 to 30 days). If your quote to the client lasts 30 days, your supplier quote must too, or add an escalation clause.
- Confirm stock before you promise a date.
- Check every delivery against the delivery note before you sign. Note damage on the note.

## Spec for Bahamian conditions

| Threat | What to specify and check |
|---|---|
| Salt air | Hot-dip galvanised or stainless fasteners, straps and connectors near the coast; stainless or coated hardware outside; adequate concrete cover over rebar per the engineer |
| Hurricanes | Hurricane straps or clips on every truss or rafter, anchored as drawn; ring-shank nails at the spacing on the drawings; impact-rated openings or code-compliant shutters; roofing rated for high wind and installed to the manufacturer's high-wind pattern |
| Termites | Soil treatment before slab; pressure-treated lumber where specified; no wood in contact with soil |
| Sun and heat | UV-rated sealants and exterior paint; hot-weather concreting (pour early, keep wet, cure 7 days) |
| Humidity and mould | Moisture-resistant board in wet areas; waterproofing membranes in showers; proper AC sizing and drainage |
| Sand and water for concrete | Washed sand, never beach sand (salt corrodes steel); clean potable mixing water |
| Water supply on Family Islands | Cisterns, wells, pumps, septic and soak-away distances per health rules |
| Theft | Just-in-time deliveries; lockable container; don't leave copper, tools or fixtures overnight unsecured |

## General conditions checklist (the costs of running the job)

Supervision time, travel and fuel, temporary toilet, skip bins and dump fees, temporary water, temporary power or generator, scaffolding, small tools and consumables, PPE and first aid, permits and inspections (if included), insurance for the job, site security, final clean, protection of existing finishes, hurricane prep allowance (June to November), photos and documentation, and for Family Islands: crew travel, housing, food, per diem, vehicle hire.

## Family Island pricing

Price Family Island work as a separate cost line, not as a percentage guess:
- Freight both ways for materials and equipment
- Crew flights or ferry, housing, food, per diem, local vehicle
- Weather and boat delays (add days to the schedule and cost)
- Double handling and breakage
- Higher supervision cost because you can't drive by daily
If you can't make the numbers work at a price the client accepts, don't take the job.

## Build your own cost book

After every job, log the real cost of each item in `consultant/my-business/jobs.md` and a cost book (item, unit, real cost, date, supplier, island). After 10 jobs your estimates come from your own data, not guesses. That is the single biggest estimating upgrade you can make.
