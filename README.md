# Asset Growth and Stock Returns

## Overview

This project explores a simple investment question:

> **Do companies that grow their assets quickly perform differently in the stock market from companies that grow more slowly?**

Previous finance research has found an interesting pattern: companies with **lower asset growth often earn higher future stock returns**, while companies expanding their assets aggressively tend to earn lower returns.

This is known as the **asset growth anomaly**.

Using historical U.S. stock and company financial data, we tested whether this pattern still exists and explored what might explain it.

---

## What is Asset Growth?

Asset growth measures how much a company's total assets change from one year to the next.

For example:

- A company opening new factories, acquiring businesses, or making large investments may have **high asset growth**.
- A company growing more slowly or reducing its investments may have **low asset growth**.

The main idea behind this project is to test whether these differences in company investment behavior are related to future stock performance.

---

## Data

The analysis combines two major financial datasets:

**Compustat**
- Company financial information
- Used to calculate annual asset growth

**CRSP**
- Historical U.S. stock prices and returns
- Used to measure how the companies performed in the stock market

The final analysis covers stock returns from **July 1981 to June 2024** and includes **23,412 unique stocks**.

---

## 1. Creating Asset Growth Portfolios

Each year, companies were ranked based on their asset growth and divided into five groups:

- **Q1:** Lowest asset growth
- **Q2:** Low asset growth
- **Q3:** Medium asset growth
- **Q4:** High asset growth
- **Q5:** Highest asset growth

We then compared the future stock returns of these groups.

### What Did We Find?

Average annual returns decreased as asset growth increased.

- **Low Asset Growth (Q1): 13.59%**
- **High Asset Growth (Q5): 10.88%**

This suggests that companies growing their assets more conservatively tended to outperform companies expanding their assets aggressively.

---

## 2. Long-Short Investment Strategy

We then tested a simple investment strategy:

> **Buy low-asset-growth companies and sell high-asset-growth companies.**

This is called a **long-short portfolio**.

The strategy generated an average return difference of approximately:

### **2.47% per year**

This provides evidence that asset growth is related to future stock returns.

---

## 3. Is the Difference Just Market Risk?

Higher returns do not automatically mean a better investment strategy. They could simply be compensation for taking more risk.

To test this, we used the **Capital Asset Pricing Model (CAPM)**.

### What is CAPM?

CAPM is a financial model used to determine how much of an investment's return can be explained by its exposure to the overall stock market.

After controlling for market risk, the long-short strategy produced an estimated:

### **3.98% annual CAPM alpha**

This suggests that the difference between low- and high-asset-growth companies cannot be explained by general market risk alone.

---

## 4. Testing Other Risk Factors

We also used the **Fama-French Three-Factor Model**.

### What is the Fama-French Model?

The model expands on CAPM by considering three major factors:

- **Market Risk** — overall stock market movements
- **Company Size** — small vs. large companies
- **Value** — value stocks vs. growth stocks

After controlling for these factors, the long-short alpha decreased to approximately:

### **2.00% per year**

This suggests that company size and value characteristics explain part of the asset growth effect, but not all of it.

---

## 5. Does Company Size Matter?

We then separated companies into **small and large firms**.

The asset growth effect was much stronger among smaller companies.

The small-company portfolio produced a Fama-French alpha of:

### **3.11% per year**

The effect was weaker and statistically insignificant among large companies.

This suggests that company size plays an important role in the relationship between asset growth and stock returns.

---

## 6. Does Industry Matter?

One of the most interesting parts of the project was testing whether the effect comes from individual companies or from differences between industries.

Some industries naturally invest and grow assets much more aggressively than others.

We therefore adjusted each company's asset growth relative to other companies in the **same industry**.

After making this adjustment, the asset growth effect largely disappeared.

This suggests that much of the pattern may be driven by:

> **Differences between industries rather than differences between individual companies within the same industry.**

---

## Key Findings

**1. Low-asset-growth companies earned higher average returns.**  
Companies with the lowest asset growth returned 13.59% annually compared with 10.88% for the highest-growth companies.

**2. A low-growth vs. high-growth strategy produced a return spread.**  
The difference was approximately 2.47% per year.

**3. Market risk alone does not explain the pattern.**  
The strategy generated a positive CAPM alpha after controlling for market exposure.

**4. Company size and value explain part of the effect.**  
The return difference became smaller after applying the Fama-French model.

**5. The effect is stronger among smaller companies.**  
Small firms showed a much stronger asset growth effect than large firms.

**6. Industry differences appear to be very important.**  
Once asset growth was compared within the same industries, the effect largely disappeared.

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Financial Data Analysis
- Portfolio Analysis
- CAPM
- Fama-French Three-Factor Model
- Regression Analysis
- Statistical Testing
- CRSP
- Compustat
- Jupyter Notebook

---

## Key Takeaway

This project shows that **how aggressively a company grows its assets can contain information about its future stock performance**.

Historically, companies with lower asset growth tended to outperform companies with higher asset growth.

However, our deeper analysis showed that the relationship is more complicated than it initially appears. Company size matters, and much of the effect appears to come from differences between industries.

The project demonstrates how financial data, portfolio construction, and statistical models can be used to test real investment theories using historical market data.
