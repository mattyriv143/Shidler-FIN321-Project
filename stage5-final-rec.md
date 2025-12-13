# **FX Hedging Project**
**Author:** Matthew Rivera

**Date:** December 12, 2025

---

## **A. Exposure Summary**

Our company expects to receive **€20,000,000 in 12 months**. Since our finacials are reported in USD, this creates **foreign exchange risk**. If the Euro becomes weaker against the USD the amount of dollars we receive will deplete, which could affect our **cash flow**, **budgeting**, and **financial planning**. 

The purpose of this analysis was to decide which hedge (Forward, Money Market, Put, or Call) best protects the USD value of the receivable.

---

## **B. Summary of Hedge Outcomes**

Using the inputs from our Stage 4 Excel model (Spot = **1.16**, Forward = **1.089**, USD rate = **3.87%**, EUR rate = **2.12%**):

### **1. Forward Hedge** 
- **USD Proceeds:**
  **UD_forward = €20,000,000 × 1.089 = ~$21.78 million**
- Locks in a guaranteed USD value for the EUR receivable.

### **2. Money Market Hedge**
- Borrow EUR → convert to USD → invest USD for 1 year.  
- Because of interest-rate parity, this hedge returns **almost exactly the same** USD amount as the forward hedge.

### **3. Option Hedges**
#### **Put Option (protective hedge for receivable)**
- Strike = **1.16**, Premium = **0.019 USD/EUR**  
- Provides downside protection if EUR drops.  
- Allows upside if EUR rises, *but* the premium cost reduces the net payoff.

#### **Call Option**
- Not appropriate for a receivable because call options hedge **payables**
- Strategy **not recommended**

## **C. Sensitivity Interpretation**

The model varies EURUSD from **0.95×S₀** to **1.05×S₀**.

### **If EUR Depreciates (EUR falls)**
- **Forward hedge** stays fixed at ~$21.78M → highest stability.
- **Money market hedge** also stays stable.
- **Put option** protects the downside but net proceeds are lower due to the premium.

### **If EUR Appreciates (EUR rises)**
- **Forward/MM hedges** do not benefit, results stay locked.
- **Put option** can benefit from appreciation after covering the premium.  
- Still generally lower than the forward unless EUR continues to rise

**Takeaway**
Forward and Money Market hedges give certainty and no cost. The put option gives flexibility, but it is more expensive and only pays off when EUR appreciation is strong.

---

## **D. Strategic Recommendation**

### **Recommended Hedge: Forward Contract**

Reasons: 
- **No premium upfront**
- **Guaranteed USD amount**
- **Easier to plan and budget under management**
- Best balance of cost and risk reduction

---

## **E. Executive Justification**

From a CFO perspective, the forward hedge is the best option because:

- It stabilizes **future cash inflows**  
- It supports **budget accuracy**  
- It avoids using cash to pay option premiums  
- It removes FX uncertainty completely  
- It aligns with the company's focus on **predictable financial outcomes**
