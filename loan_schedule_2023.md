# Pet Shop Loan Calculation 2023

**Loan Principal:** $45,000
**Loan Start:** March 1, 2023 (3rd month of 2023)
**Monthly Interest Rate:** 5.12% compounded monthly
**Weekly Payment Rate:** 12% of weekly profit
**Data Source:** `/data/Pet Care 2023 Weekly Financials.csv`

## Summary

- **Total 2023 Profit (52 weeks):** $342,870
- **Total Potential Annual Payments (12%):** $41,144.40
- **Profit from Week 9 onward (Mar 1 - Dec 31):** $291,455 → Payments $34,974.60
- **Profit from Week 10 onward (first full March week):** $285,115 → Payments $34,213.80

### Modeling Approach (Most Realistic)

Payments applied weekly when due, Interest applied at month end on outstanding balance.

**Result after Dec 31, 2023:** **$27,875.55** remaining.

Alternative assume loan start after Week9/before only full March weeks:
- Week10+ payments, interest after payments: **$29,129.05**
- Week9+ payments, interest BEFORE payments each month: **$30,129.03**
- Week10+ payments, interest before payments: **$31,321.47**

### Simple Interest-Only then Subtract Payments (No amortization)
- 10 months compound: $45,000 × 1.0512^10 = $74,142.30
  - Minus Week9+ payments $34,974.60 = $39,167.70 remaining
  - Minus Week10+ payments $34,213.80 = $39,928.50 remaining
- 9 months compound: $45,000 × 1.0512^9 = $70,531.10
  - Minus Week10+ payments = $36,317.30 remaining

## Monthly Breakdown (Payments after, interest after)

| Month | Weeks | Payment Total | Balance Before Interest | Interest 5.12% | Balance After Interest |
|-------|-------|---------------|--------------------------|----------------|------------------------|
| March | 4 (W9-W12) | $3,166.92 | $41,833.08 | $2,141.85 | $43,974.93 |
| April | 5 (W13-W17) | $3,921.72 | $40,053.21 | $2,050.72 | $42,103.94 |
| May | 4 (W18-W21) | $3,000.48 | $39,103.46 | $2,002.10 | $41,105.56 |
| June | 4 (W22-W25) | $3,218.04 | $37,887.52 | $1,939.84 | $39,827.36 |
| July | 5 (W26-W30) | $4,040.64 | $35,786.72 | $1,832.28 | $37,619.00 |
| August | 4 (W31-W34) | $3,104.28 | $34,514.72 | $1,767.15 | $36,281.87 |
| September | 4 (W35-W38) | $3,198.96 | $33,082.91 | $1,693.84 | $34,776.75 |
| October | 5 (W39-W43) | $4,020.36 | $30,756.39 | $1,574.73 | $32,331.12 |
| November | 4 (W44-W47) | $3,231.24 | $29,099.88 | $1,489.91 | $30,589.80 |
| December | 5 (W48-W52) | $4,071.96 | $26,517.84 | $1,357.71 | **$27,875.55** |

## Key Weekly Profits Used

Week 9: $6,340 → $760.80
Week 10: $6,596 → $791.52
Week 11: $6,868 → $824.16
Week 12: $6,587 → $790.44
Week 13: $6,658 → $798.96
Week 14: $6,736 → $808.32
Week 15: $6,201 → $744.12
Week 16: $6,384 → $766.08
Week 17: $6,702 → $804.24
Week 18: $6,108 → $732.96
Week 19: $5,860 → $703.20
Week 20: $6,572 → $788.64
Week 21: $6,464 → $775.68
Week 22: $6,942 → $833.04
Week 23: $6,691 → $802.92
Week 24: $6,602 → $792.24
Week 25: $6,582 → $789.84
Week 26: $6,786 → $814.32
Week 27: $6,971 → $836.52
Week 28: $6,698 → $803.76
Week 29: $6,720 → $806.40
Week 30: $6,497 → $779.64
Week 31: $6,419 → $770.28
Week 32: $6,849 → $821.88
Week 33: $6,420 → $770.40
Week 34: $6,181 → $741.72
Week 35: $6,475 → $777.00
Week 36: $6,616 → $793.92
Week 37: $6,718 → $806.16
Week 38: $6,849 → $821.88
Week 39: $7,057 → $846.84
Week 40: $6,835 → $820.20
Week 41: $6,513 → $781.56
Week 42: $6,577 → $789.24
Week 43: $6,521 → $782.52
Week 44: $6,180 → $741.60
Week 45: $6,680 → $801.60
Week 46: $7,110 → $853.20
Week 47: $6,957 → $834.84
Week 48: $6,709 → $805.08
Week 49: $6,927 → $831.24
Week 50: $6,579 → $789.48
Week 51: $6,801 → $816.12
Week 52: $6,917 → $830.04

## Conclusion
With weekly 12% profit payments starting March 1 and monthly 5.12% interest compounded on declining balance, you'd still owe **≈ $27.9k** on Dec 31, 2023.

If you paid the entire year's profit share ($41,144), you'd owe ≈ $32,998 under simple interest-then-pay model.
