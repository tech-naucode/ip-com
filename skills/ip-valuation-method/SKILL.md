---
name: ip-valuation-method
description: >
  The four standard IP valuation approaches (cost, market, income, real-options),
  when each applies, industry royalty benchmarks, and the common over- and
  under-valuation traps. Read this whenever asked "what's this IP worth?" — never
  pick a number from intuition. Cite the rule ID (V1.1, V2.3, etc.) when applying.
---

# IP Valuation Method

The discipline of putting honest numbers on intellectual property. Used by
all four agents in this company. Reject any artifact that quotes a value or
royalty rate without referencing a method below.

## V1 — The four standard approaches

### V1.1 Cost approach
Replicate-cost or replacement-cost. "What would it cost to recreate this IP
from scratch today?"

- **Use when:** early-stage IP with no commercial history, internal-use IP,
  IP being transferred between affiliated entities for tax purposes
- **Don't use when:** IP has demonstrated revenue (income approach is better),
  market has comparables (market approach is better)
- **Calculation:** sum of R&D hours × loaded engineering rate, plus filing
  costs, plus prosecution costs, plus opportunity cost premium (typically 20-40%)
- **Trap:** cost approach systematically undervalues IP that solves a high-value
  problem cheaply. Algorithm that took 2 weeks to invent might be worth $10M.

### V1.2 Market approach
Comparable transactions. "What did similar IP sell for in similar deals?"

- **Use when:** active comparables exist (most patent licensing has them),
  asset class is mainstream (software, life-sciences patents, brands)
- **Don't use when:** asset is genuinely novel category (no comparables exist),
  comparables are too thin or too dated (>3 years old)
- **Calculation:** weighted average of comparable deal terms, adjusted for
  scope differences (geography, exclusivity, field of use, term length)
- **Trap:** comparables are almost never apples-to-apples. Document every
  adjustment. "We adjusted X comparable down 30% because their field of use
  was broader" beats hand-waving "roughly comparable".

### V1.3 Income approach (DCF)
Discounted cash flow on royalty stream. "What's the present value of expected
royalty income?"

- **Use when:** asset has plausible commercial path, target market is sizeable
  enough that revenue projections aren't fantasy, deal duration > 3 years
- **Don't use when:** revenue projections require assumptions that are barely
  better than guessing (early-stage hardware in untested market)
- **Calculation:**
  - Project net sales of licensed product, year by year, for term length
  - Apply royalty rate (anchored on V2 industry benchmarks or V1.2 comparables)
  - Discount at appropriate rate (typically 15-25% for IP licensing — riskier
    than corporate WACC due to enforcement risk and obsolescence risk)
  - Sum present values
- **Trap:** sensitivity to royalty rate and discount rate. Always run 3
  scenarios (low / base / high) — single point estimates lie about confidence.

### V1.4 Real-options approach
Treats commercialization decisions as a sequence of options. "What's it worth
if we have the option but not obligation to license at each milestone?"

- **Use when:** IP has multiple commercialization paths, licensee will gate
  spending on milestones, biotech / pharma where stages matter enormously
- **Don't use when:** asset is a single straightforward license, or you don't
  have rigorous distribution data for option pricing
- **Calculation:** Black-Scholes or binomial tree on option-bearing decisions.
  In practice, most IP commercialization teams use a simplified milestone-DCF
  hybrid rather than rigorous Black-Scholes.
- **Trap:** can produce numbers that look mathematical but rest on volatility
  estimates pulled from thin air. Use sparingly; document every input.

## V2 — Industry royalty benchmarks (running royalty as % of net sales)

These are observed ranges from licensing surveys (Royalty Source, Licensing
Executives Society surveys, public 10-K disclosures). Use as anchors only —
specific deals always vary.

| Industry | Patent licenses | Software | Brand / trademark |
|---|---|---|---|
| Software (B2B SaaS) | 5–15% | 8–25% | 2–5% |
| Software (consumer apps) | 2–8% | 5–15% | 5–12% |
| Pharmaceuticals (small molecule) | 2–8% (post-launch) | n/a | n/a |
| Biotech (pre-commercial) | upfront-heavy + milestones; running royalty 0.5–4% | n/a | n/a |
| Medical devices | 3–8% | 5–10% | 2–5% |
| Consumer electronics | 1–5% | 3–8% | 3–8% |
| Industrial / manufacturing | 1–5% | 3–8% | 1–4% |
| Automotive | 0.5–3% | 1–5% | n/a |
| Apparel / consumer goods | 5–15% | n/a | 5–15% |
| Food / beverage | 2–8% | n/a | 4–10% |

**Always cite the source** when using these in an artifact. "Per
ip-valuation-method §V2, B2B SaaS patent licenses typically run 5–15%; we're
recommending 8% based on V1.2 comparables 1 and 3."

## V3 — When to use which approach (decision matrix)

| Asset stage / type | Primary method | Cross-check with |
|---|---|---|
| Early-stage patent, no commercial history | Cost (V1.1) | Market (V1.2) if comparables exist |
| Patent with commercial track record | Income (V1.3) | Market (V1.2) |
| Software with revenue | Income (V1.3) | Market (V1.2) |
| Software, internal-use, no revenue | Cost (V1.1) | — |
| Trademark / brand with revenue | Income (V1.3) | Market (V1.2) |
| Trade secret | Income (V1.3, conservative) — confidentiality limits market data | Cost (V1.1) for floor |
| Biotech preclinical | Real options (V1.4) | Income with milestones |
| Patent portfolio (mixed) | Income on top patents + cost floor on rest | Market for portfolio comparables |

## V4 — The over-valuation traps (auto-flag in review)

Patterns that consistently overstate value. Reject artifacts that hit these.

- **V4.1 Linear extrapolation of TAM × % market share × royalty %.** Even at
  0.1% market share assumptions, this produces fantasy. Anchor in real
  comparable deals' first-3-year revenues.
- **V4.2 Counting strategic value as financial value.** "This patent gives us
  market position" is a strategic argument. Don't add a strategic premium
  unless you can cite a comparable that paid for similar strategic positioning.
- **V4.3 Ignoring discount rate.** A $10M royalty 10 years from now isn't
  worth $10M. At 20% IP discount rate, it's worth ~$1.6M.
- **V4.4 Counting all named claims as separately valuable.** A patent with 20
  claims doesn't have 20 × the value of a patent with 1 claim. Independent
  claims drive value; dependent claims just narrow.
- **V4.5 Using listed comparables uncritically.** Press releases overstate
  deal value (lump sum announced often includes equity + research funding,
  not just IP value). Always check 10-K for actual breakdown.

## V5 — The under-valuation traps (also auto-flag)

- **V5.1 Cost-only valuation when commercial path exists.** Don't anchor on
  R&D cost if the IP solves a real customer problem with willingness to pay.
- **V5.2 Ignoring strategic licensee premium.** A licensee for whom the IP is
  strategically critical (defensive moat, regulatory shortcut) pays more than
  a financial-only licensee. This is real and citable from comparable deals.
- **V5.3 Discount rate too high.** 30%+ discount rates effectively zero the
  asset. Use industry-standard 15-25% unless specific evidence justifies higher.

## V6 — Required documentation in any valuation

Every valuation artifact must include:

- **Approach chosen** (V1.1 / V1.2 / V1.3 / V1.4) with reason from V3 matrix
- **Inputs** (numbers, assumptions, data sources)
- **Range** (low / base / high), not a point estimate
- **Sensitivity** (what changes the number most)
- **Confidence** (high / medium / low) with one-paragraph reason
- **Recommended cross-check method** (per V3) and its result
- **Disclaimer:** "Valuation is for commercialization planning purposes;
  formal valuation for tax, financial reporting, or litigation requires a
  licensed appraiser."
