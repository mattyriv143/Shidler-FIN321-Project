# Quantitative Specification - FX Hedging Model (U.S. Aerospace Manufacturer)

**Created by:** Matthew Rivera  

**Updated by:** Matthew Rivera

**Date Created:** November 7, 2025  

**Date Updated:** November 27, 2025 

**Version:** 2.0

**LLM Used:"" GPT-5

**Role:** Financial Analyst 

**Audience:** CFO   

**Purpose:** Provide a professional, quantitative specification outlining the analytical structure for evaluating FX hedging alternatives.

---

## 1. Problem Statement

Our firm, an aerospace manfacturer based in the U.S., expects to receive **€20,000,000 in 12 months** from a European customer. Because our financial statments and operating costs are designated in **USD**, this receivable creates risk of **foreign exhange exposure** to fluctuations in the **EUR/USD** rate. At today's **spot rate of 1.16**, the receivable is worth approximately **23.2 million**. However, the **1-year forward rate of 1.0890** shows that the market expects the euro to weaken. The objective of this analysis is to quantify, compare, and evaluate alternative hedging strategies to stabilize dollar proceeds. This specification details the structure of a spreadsheet model that supports decisions at the Treasury and CFO levels.


---

## 2. Inputs (Known Variables)


| Variable | Description | Unit | Example | Source |
|-----------|-------------|------|----------|--------|
| `FC_AMT` | Foreign-currency receivable | EUR | 20,000,000 | Company data |
| `S₀` | Current EURUSD spot rate | USD/EUR | 1.1600 | Market data |
| `F₀` | 1-year EURUSD forward rate | USD/EUR | 1.0890 | Provided |
| `r_USD` | USD 1-year interest rate | % | 3.87% | Market data |
| `r_EUR` | EUR 1-year interest rate | % | 2.12% | Market data |
| `t` | Time to maturity | Years | 1 | Derived |
| `K_put` | EUR Put strike | USD/EUR | 1.16 | Analyst choice |
| `K_call` | EUR Call strike | USD/EUR | 1.16 | Analyst choice |
| `Premium_put` | Put premium | USD per contract | 0.019 | Scenario |
| `Premium_call` | Call premium | USD per contract | 0.024 | Scenario |


---

## 3. Assumptions & Constraints

1. Interest rates are annualized on a simple basis
2. Forward rate represents one-year maturity / no transaction fees
3. Option premiums are paid upfront in USD
4. No credit / default risk; receivable collected in full
5. Exchange rates are quoted as **USD per EUR**.
6. Tax implications and margin requirements are excluded

---

## 4. Calculation Flow

This model will follow a structured sequence to evaluate each hedge family.

### Step 1: Forward Hedge
1. Lock in conversion at forward rate **F₀**.
2. Compute USD proceeds: **USD_forward = FC_AMT × F₀**
- This serves as a baseline

### Step 2: Money Market Hedge
1. Discount EUR receivable by **r_EUR** to find the present EUR value.  
2. Convert that EUR to USD today at **S₀**.  
3. Invest USD proceeds for one year at **r_USD**.
4. Compute the results of the USD amount and verify that it aligns with **F₀**.

### Step 3: Option Hedge
1. Simulate EUR/USD spot rates at maturity (**S_T**) 1.00 ± 10%.
2. For each S_T, compute:
   - **Put hedge:** If S_T < K_put → exercise put; else use default market rate.
   - **Call hedge:** If S_T > K_call → exercise call; else use defualt market rate.
3. Subtract premiums from gross proceeds.
4. Record net USD outcomes for each hedge type.

### Step 4: Sensitivity & Comparison 
- Arrange USD outcomdx under each strategy across S_T values.
- Generate a line chart comparing hedge payoffs vs S_T.
- Identify breakeven points and expected outcome values.

### Step 5: Summarize
- Expected / Minimum / Maximum USD proceeds
- Standard deviation of outcomes (risk)
- Hedge cost as % of exposure 

---

## 5. Outputs

| Output | Description | Format | Purpose |
|---------|--------------|---------|----------|
| `USD_forward` | USD proceeds from forward hedge | Numeric | Certainty baseline |
| `USD_mm` | USD proceeds from money market hedge | Numeric | Cross-check |
| `USD_put` | USD proceeds from EUR put hedge | Table | Downside protection |
| `USD_call` | USD proceeds from EUR call hedge | Table | Upside Participation |
| `Chart_1` | Hedge outcomes vs. S_T | Line chart | Visual comparison |
| `Summary` | Written conclusion, Key metrics, and interpretation | 1–2 paragraphs | CFO-ready insight |


---

## 6. Sensitivity Plan

The model will simulate FX outcomes across a realistic range of future EUR/USD rates.

- Range: **1.10 to 1.22**
- Increment **0.01**
- For each rate:
  - Compute USD proceeds for each hedge.
  - Identify breakeven and indifference zones.
  - Present results as a comparison table and line chart. 

---

## 7. Limitations & Next Steps

### Limitations 
- Excludes implied volatility
- Assumes flat interest rates and ignores forward bid-ask spreads
- Excludes hedge-effectiveness tests.

### Next Steps 
1. **Stage 3 - Excel Model Build:** Implement input variables and calculation flow in Excel
2. **Stage 4 - Prompt Engineering:** Develop AI instructions to generate the spreadsheet using these specifications
3. **Stage 5 - Final Recommendation:** Compare hedge outcomes and recommend a preferred strategy
