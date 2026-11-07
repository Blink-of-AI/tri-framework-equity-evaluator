---
name: tri-framework-equity-evaluator
description: 'Evaluate and compare stocks with the Graham, Buffett, and Paul Tudor Jones tri-framework. Use for equity research, stock screening, valuation, moat and financial-quality analysis, technical trend and macro review, portfolio comparisons, or requests to rank a ticker.'
---

# Tri-Framework Equity Evaluator

Use this workflow to assess a stock through three complementary lenses: Benjamin Graham's value and balance-sheet safety, Warren Buffett's moat and capital compounding, and Paul Tudor Jones's macro and trend discipline. Apply the framework to the user's requested ticker(s), date, market, and comparison universe.

## Research standards

- Use the most recent reliable financial statements and market/price data available. State the data's as-of date and distinguish reported facts from estimates or interpretation.
- Cite sources for material financial, macroeconomic, and price-trend claims. Prefer company filings and investor relations materials for financial statements, and reputable market-data providers for current prices and moving averages.
- Do not invent missing values. If an input cannot be verified, label it unavailable, explain what is missing, and mark the affected test inconclusive rather than passing it.
- Keep units, currencies, share counts, and reporting periods consistent. Explain material adjustments and assumptions, especially maintenance capital expenditure used in owner earnings.
- This is a structured research framework, not personalized financial advice. Explain that results depend on data quality, assumptions, and the user's circumstances.

## Procedure

### 1. Establish the security and data

Confirm the company, ticker, exchange, share class, and reporting currency. Gather the current market price and the financial, historical earnings, dividends, price history, and macro data needed below. Note any unavailable or stale data before scoring.

### 2. Run the Graham value and safety screen

Calculate or assess:

- **Graham Number:** `sqrt(22.5 × GAAP EPS × BVPS)`. If GAAP EPS is negative, report the Graham Number as **N/A** and use the standalone asset floor instead; do not take a square root of a negative value.
- **Standalone Asset Floor:** `1.33 to 1.50 × BVPS`. State which multiplier is used and why.
- **Graham Ratio:** `current market price / Graham Number` when available; otherwise compare price to the stated asset-floor reference and label the denominator clearly.
- **Current Ratio:** `current assets / current liabilities`; required minimum is 2.0 for industrial/defensive stocks and 1.5 for retail/commercial businesses. Explain the sector classification.
- **Debt vs. Net Working Capital:** compare total long-term debt with `current assets − current liabilities`; the screen requires long-term debt to be less than net working capital.
- **Earnings Continuity:** check for 10 consecutive years of positive GAAP net earnings.
- **Dividend Record:** check for 20 consecutive years of uninterrupted dividends.

Use the source framework's valuation bands: below 1.00x is undervalued; 1.00x through 1.75x is fairly valued/moderately premium; above 1.75x is overvalued/speculative. The consensus matrix separately describes a Graham pass at 1.7x or less and a fail at above 2.0x. Preserve this distinction: report the phase classification and matrix result separately, and identify ratios above 1.7x through 2.0x as a threshold gap rather than silently forcing a pass or fail. A ratio above 2.0x is a matrix fail.

### 3. Assess Buffett's moat and compounding quality

- Identify evidence for brand/intangible pricing power, network effects, structural cost advantage/scale, and customer switching costs. Rate the overall moat as wide, narrow, or none and support the rating.
- Assess ROIC or RoTE consistency relative to the cost of capital; the framework's indicative quality threshold is greater than 15%. Show the metric, period, and calculation/source when available.
- Compare owner earnings—free cash flow using **maintenance** capex, not automatically all capex—with reported GAAP net income. Explain whether owner earnings track or exceed earnings and the durability of that relationship.
- Assess whether growth is self-funded or depends on recurring heavy debt/equity issuance.
- Explicitly consider the R&D/patent treadmill for pharmaceutical businesses and commodity hardware risk for non-differentiated cyclical hardware.

### 4. Apply the Paul Tudor Jones macro and momentum filter

- Compare the current price with its 200-day moving average and describe whether the average and broader trend are rising. State the observation date.
- Mark the trend pass only when price is above a rising 200-day trend. Mark below the 200-day moving average as a fail/falling-knife warning; do not recommend averaging down under this framework.
- Comment on liquidity and whether an institutional position could reasonably be exited. Avoid treating high volatility as inherently positive; explain any structural catalyst that could justify it.
- Identify relevant macro tailwinds or headwinds, with evidence and time horizon.
- Evaluate whether a plausible setup offers the framework's 5:1 target risk/reward. Show the proposed entry/reference, invalidation or stop level, target, and arithmetic when sufficient data exists. Otherwise label the setup unverified, not a pass. Do not promise returns.

### 5. Synthesize and rank

For each lens, assign **Pass**, **Neutral**, or **Fail**, and summarize the evidence:

- **Graham:** consider valuation alongside current ratio and debt versus working capital. Report earnings continuity and dividend record as separate checks; do not hide failed checks behind an aggregate label.
- **Buffett:** consider ROIC/RoTE, moat evidence, owner-earnings durability, and capital intensity together.
- **PTJ:** consider the 200-day trend, liquidity, macro catalyst, and risk/reward setup together.

Apply the framework's tiers transparently:

1. **Tier 1 — Unanimous Consensus Champion:** three passes.
2. **Tier 2 — Quality Fortress:** two passes and one neutral.
3. **Tier 3 — Single-Lens Play:** one pass and two neutral/fail results; name the lens driving the case (pure value, moat-led growth, or momentum).
4. **Tier 4 — Speculative / High Volatility:** early-stage or binary-risk cases, such as unproven technology or biotech; explain the specific risk. Use this tier when its risk profile best describes the security, rather than implying the other tiers cover it.
5. **Tier 5 — Unanimous Veto:** three fails.

If a result does not fit one of the defined combinations (for example, two passes and one fail), do not force a tier. State that the source framework leaves that combination undefined, report the three lens scores, and give a clearly labeled qualitative synthesis. Do not equate missing data with a pass.

For multiple securities, use the same as-of date and consistent assumptions where possible. Provide a comparison matrix, state how ties or unavailable data affect the ranking, and avoid a ranking when the evidence is not comparable.

## Output format

For a single security, use:

### [Company Name] ([Ticker]) Evaluation

**Data as of:** [date]

#### 1. Quantitative Valuation (Graham)
- **Book Value / Share:** [value, currency, period/source]
- **Graham Number / Asset Floor:** [value or N/A; include method]
- **Valuation Multiple:** [X.XXx] (phase status: [status]; matrix result: [Pass/Neutral/Fail])
- **Balance Sheet Check:** Current Ratio = [X.XX] | Long-Term Debt vs. Net Working Capital = [Pass/Fail/Unavailable]
- **Earnings Continuity:** [result for 10-year test]
- **Dividend Record:** [result for 20-year test]

#### 2. Moat & Quality (Buffett)
- **Economic Moat:** [Wide / Narrow / None, with evidence]
- **ROIC / RoTE:** [value and period, or unavailable]
- **Owner Earnings Durability:** [High / Medium / Low, with evidence]
- **Capital Allocation / Red Flags:** [summary]

#### 3. Macro & Momentum (PTJ)
- **200-Day Moving Average Trend:** [Above / Below / Unavailable; trend direction and as-of date]
- **Liquidity:** [assessment]
- **Macro Catalysts:** [evidence-based summary]
- **Risk/Reward Setup:** [5:1 Setup / Neutral / Poor / Unverified; show inputs if calculable]

#### 4. Consensus
| Dimension | Score | Evidence |
|---|---|---|
| Graham | [Pass / Neutral / Fail] | [brief rationale] |
| Buffett | [Pass / Neutral / Fail] | [brief rationale] |
| PTJ | [Pass / Neutral / Fail] | [brief rationale] |

**Final Consensus Rating:** [Tier 1 to Tier 5, or Undefined by source framework]

[Concise synthesis explaining the strongest evidence, key failure risks, data gaps, and why the tier or undefined status follows from the criteria.]

**Sources:** [link or identify cited sources]

For portfolio or multi-stock requests, retain the per-company evidence and scores, then add a consistent comparison/ranking table and explain any comparability limits.
