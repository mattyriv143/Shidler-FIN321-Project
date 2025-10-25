# **Managing FX Exposure on EUR Receivable, Hedding Memo: U.S. Aerospace Manufacture**

**Created by:** Matthew Rivera

**Updated by:** Matthew Rivera

**Date Created:** October 14, 2025

**Date Updated:** October 24, 2025

**Version:** 1.0

**LLM Used:** GPT-5

---

## Executive Summary 

Our Company expects to receive **€20,000,000 in one year** from a European aerospace client. Looking at the current **EUR/USD spot rate of 1.16**, this payment is worth around **$23.2 million** today. However, looking at the current **1-year forward rate of 1.0935,** it signals potential downside for the euro over the next 12 months. If the euro unfortunately weakens, our USD proceeds will fall, which is a negative for next year's revenue. This memo highlights the exposure, key risks, and three main hedging strategies to protect our value.

---

## Background & Objectives 

As we invoice in euros but report in dollars, the resulting **FX exposure** leaves us vulnerable to euro depreciation. For example, a 5% decline in EUR/USD would reduce our value by around **1.1 million**. Our primary objectives should be **stablizing cash inflows** and **protecting profit margins** from unfavorable exchange rate movements, establishing forseeable finacial performance.

---

## Mehtods: Heding Strategies Overview

We will evaluate three common hedge families:

**Forward Contract** - Agree now to exchange €20 million for USD in one year at 1.0935.
- *Pros:* Playing it safe, eliminates FX uncertainty with no upfront premium.
- *Cons:* Forfeits the upside if the euro decides to strengthen.

**Money Market Hedge** - Borrow euros and invest USD now to lcok in the forward rate.
- *Pros:* Mechanically replicates forward rate
- *Cons:* Affects liquidity

**Options Hedge (Put on EUR)** - Buy a put option with strike near 1.16, premium = $0.019/€.
- *Pros:* Gives downside protection and allows upside gain
- *Cons:* Requires premium payment of around $380,000

---

Limitations & Next Steps

Key assumptions include that the interest rate will remain stable and euro will be collected in full. Option pricing and volatility may also shift before execution. In **Stages 2-3**, we will: 

- Develop a **technical specification** for an Excel model to simulate the payoffs for forward, money market, and option hedging.
- **Implement** the spec to compare dollar outcomes under varying EUR/USD rates.
- Use **prompt engineering** to automate an Excel spreadsheet from the inputs (spot/forward rates, premiums).
- Deliver a **final recommendation** of the most optimal hedge based on my data on risk tolerance and expected value.

## References 

- Investing.com. “EUR/USD – Euro/US Dollar.” Investing.com, https://www.investing.com/currencies/eur-usd?utm_source=chatgpt.com
- Investopedia. (2024). Foreign Exchange Hedging Techniques. 
