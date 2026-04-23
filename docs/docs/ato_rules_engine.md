# ATO Rules Engine

This document explains how the system applies Australian tax rules.

---

## 1. Instant Asset Write-Off (< $20,000)

If:
- Business portion of asset < $20,000  
Then:
- 100% deduction in year of purchase  
- Asset moves into simplified depreciation pool

---

## 2. Simplified Depreciation Pool

Rates:
- 15% in first year
- 30% each year after

Applies to:
- AST-01 Plant & Equipment
- AST-02 Motor Vehicle Asset
- AST-POOL

---

## 3. PAYG Asset Rules (< $300)

If:
- PAYG portion < $300  
Then:
- Immediate deduction  
Else:
- Depreciate over effective life

---

## 4. GST Rules

### GST Collected
10% of sales (INC-01)

### GST Paid
10% of purchases (if GST included)

### Net GST
GST Collected – GST Paid

---

## 5. Vehicle Rules

### PAYG
- 88c per km
- Max 5,000 km
- Warning at 4,500 km

### Sole Trader
- Actual expenses × logbook %

---

## 6. Benchmark Alerts

System compares:
- COGS
- Motor vehicle
- Travel
- Other expenses

Against ATO industry benchmarks.

If > benchmark:
- Flag as “High audit risk”

---

## 7. Tax Calculation

Total taxable income =
PAYG gross (annualised) + Sole trader profit

Tax liability =
Income tax + Medicare levy – PAYG withheld

Weekly saving rate =
Tax shortfall ÷ weeks remaining
