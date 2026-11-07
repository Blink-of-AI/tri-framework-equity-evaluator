---
name: tri-framework-equity-evaluator
description: Evaluate equity securities using a synthesized 3-way framework of Benjamin Graham (Defensive Value & Balance Sheet Safety), Warren Buffett (Economic Moat & Capital Compounding), and Paul Tudor Jones (Global Macro, Trend Momentum & Risk-Reward Asymmetry).
---

# Tri-Framework Equity Evaluator

An institutional-grade analysis framework for screening, evaluating, and ranking stocks by combining three distinct investment philosophies: **Benjamin Graham's** quantitative margin of safety, **Warren Buffett's** durable economic moats, and **Paul Tudor Jones's** macro trend momentum.

---

## Workflow Overview

1. **Phase 1: Benjamin Graham Screen (Quantitative Safety Floor)**
2. **Phase 2: Warren Buffett Analysis (Qualitative Moat & Owner Earnings)**
3. **Phase 3: Paul Tudor Jones Filter (Macro Catalysts & Trend Momentum)**
4. **Phase 4: Synthesis & Consensus Scoring**
5. **Phase 5: Output Matrix & Portfolio Decisioning**

---

## Phase 1: Benjamin Graham Screen (Quantitative Margin of Safety)

Evaluate the target security against strict quantitative balance sheet, asset backing, and earnings criteria derived from *The Intelligent Investor*.

### 1. Key Formulas & Metrics
- **Graham Number Ceiling**:
  $$\text{Graham Number} = \sqrt{22.5 \times \text{EPS} \times \text{BVPS}}$$
  *(Note: For negative GAAP EPS, state **N/A** and default to the Standalone Asset Floor).*
- **Standalone Net Asset Floor**:
  $$\text{Asset Floor} = 1.33\text{x} \text{ to } 1.50\text{x} \times \text{Book Value Per Share (BVPS)}$$
- **Valuation Ratio**:
  $$\text{Graham Ratio} = \frac{\text{Current Market Price}}{\text{Graham Number (or Asset Floor)}}$$

### 2. Balance Sheet & Solvency Rules
- **Current Ratio**: Must be $\ge 2.0$ for industrial/defensive stocks ($\ge 1.5$ for retail/commercial).
- **Long-Term Debt Solvency**: Total Long-Term Debt must be less than Net Working Capital ($\text{Current Assets} - \text{Current Liabilities}$).
- **Earnings Continuity**: 10 consecutive years of positive GAAP net earnings.
- **Dividend Record**: 20 consecutive years of uninterrupted dividend distributions.

### 3. Classification
- **Undervalued**: $\text{Graham Ratio} < 1.00x$ (Trades below intrinsic valuation ceiling).
- **Fairly Valued / Moderate Premium**: $1.00x \le \text{Graham Ratio} \le 1.75x$.
- **Overvalued / Speculative**: $\text{Graham Ratio} > 1.75x$.

---

## Phase 2: Warren Buffett Analysis (Moat & Capital Compounding)

Evaluate whether the enterprise possesses an enduring economic moat that allows it to compound capital at high Return on Invested Capital (ROIC) over 10–20+ years.

### 1. Moat Identification & Assessment
- **Intangibles & Brand Power**: Can the firm raise prices without losing customer volume?
- **Network Effects**: Does each additional user make the platform more valuable for all users?
- **Cost Advantage / Scale**: Does the firm enjoy structural cost superiority over competitors?
- **Switching Costs**: Is it painfully expensive or risky for customers to switch to a rival?

### 2. Capital Allocation & Financial Quality
- **ROIC / RoTE**: Consistently exceeds cost of capital (typically $>15\%$).
- **Owner Earnings**: Free Cash Flow ($\text{Operating Cash Flow} - \text{Maintenance CapEx}$) tracks or exceeds reported GAAP Net Income.
- **Capital Intensity Check**: Does the company require continuous heavy debt/equity issuance to stay competitive, or does it self-fund growth?
- **Red Flags**:
  - *The R&D / Patent Treadmill*: High reliance on binary drug trial readouts or expiring patents (pharma).
  - *Commodity Hardware*: Highly cyclical, non-differentiated hardware lacking pricing power (chip foundries, flash memory).

---

## Phase 3: Paul Tudor Jones Filter (Macro Catalysts & Trend Momentum)

Evaluate technical price structure, macro tailwinds, and asymmetric risk/reward to avoid catching "falling knives."

### 1. Technical & Trend Rules
- **The 200-Day Moving Average Rule**: 
  - **Pass**: Stock trades *above* its 200-day MA with a rising trend structure.
  - **Fail ("Falling Knife")**: Stock trades *below* its 200-day MA. Never average down into declining price trends ("Losers average losers").
- **Volatility & Liquidity**:
  - Avoid illiquid micro-caps where large institutional positions cannot be exited instantly.
  - Embrace high-beta, high-volatility leaders when backed by structural catalysts.

### 2. Macro Catalysts & Asymmetry
- **Macro Tailwinds**: Liquidity expansion, central bank interest rate shifts, AI supercycles, or commodity volume spikes.
- **Asymmetric Risk/Reward Ratio**: Targets a **5:1 Risk/Reward Ratio** (Risking \$1 to gain \$5).
- **Execution Discipline**: Uses tight stop-loss orders; cuts underperforming positions quickly if trend confirmation fails.

---

## Phase 4: Tri-Framework Consensus Matrix

Grade the security across all three dimensions using the matrix below:

| Dimension | Graham (Value & Safety) | Buffett (Moat & Compounding) | PTJ (Macro & Momentum) |
| :--- | :--- | :--- | :--- |
| **Pass Criteria** | $\text{Ratio} \le 1.7x$, Current Ratio $\ge 2.0$, Debt < Working Cap | ROIC $>15\%$, High Moat, Predictable Cash Flow | Price $>200$-day MA, Asymmetric Macro Catalyst |
| **Neutral / Hold** | Fairly valued ($1.0x-1.7x$), strong balance sheet | Average Moat, cyclical industry | Rangebound technical consolidation |
| **Fail / Veto** | Ratio $>2.0x$, high debt overhang, negative equity | No Moat, R&D treadmill, capital-intensive commodity | Downtrending below 200-day MA, illiquid micro-cap |

### Tier Scoring System
1. **Tier 1: Unanimous Consensus Champion (3 Passes)** — Rare triple-threat security. Excellent balance sheet safety, strong moat, and upward macro momentum.
2. **Tier 2: Quality Fortress (2 Passes, 1 Neutral)** — High-quality compounder with solid safety metrics trading at a reasonable multiple.
3. **Tier 3: Single-Lens Play (1 Pass, 2 Neutrals/Fails)** — Pure value bargain (Graham only), high-moat growth (Buffett only), or momentum trade (PTJ only).
4. **Tier 4: Speculative / High Volatility** — Early-stage biotech or unproven tech with binary risks.
5. **Tier 5: Unanimous Veto (3 Fails)** — Overvalued, debt-laden, downtrending, or moatless assets. Avoid or short.

---

## Phase 5: Output Deliverable Template

When asked to evaluate a single stock or portfolio, render the results in the following standard output format:

```markdown
### [Company Name] ([Ticker]) Evaluation

#### 1. Quantitative Valuation (Graham)
- **Book Value / Share**: $[Value]
- **Graham Number / Asset Floor**: $[Value]
- **Valuation Multiple**: [X.XX]x (Status: [Undervalued / Overvalued])
- **Balance Sheet Check**: Current Ratio = [X.XX] | Debt vs. Working Capital = [Pass/Fail]

#### 2. Moat & Quality (Buffett)
- **Economic Moat**: [Wide / Narrow / None]
- **ROIC / RoTE**: [XX.X]%
- **Owner Earnings Durability**: [High / Medium / Low]

#### 3. Macro & Momentum (PTJ)
- **200-Day Moving Average Trend**: [Above / Below]
- **Macro Catalyst**: [Description]
- **Asymmetric Risk/Reward Setup**: [5:1 Setup / Neutral / Poor]

#### Final Consensus Rating: [Tier 1 to Tier 5 Classification]
[1-paragraph summary of why the stock fits or fails the combined consensus.]
```
