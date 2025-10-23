
# Task 03 — Taxi Fare

**Pricing:** First 2 km cost **4.00 €** total.  
Every additional kilometer (or part of it) costs **1.50 €** per km, **rounded up** to the next km.

**Input:** One non‑negative integer `k` (driven kilometers).  
**Output:** Total fare as a decimal with **two digits** (e.g., `7.00`).

### Interpretation
If `k <= 2` → `4.00`.  
Else → `4.00 + 1.50 * ceil(k - 2)`.

### Samples
```
in: 0      out: 4.00
in: 2      out: 4.00
in: 3      out: 5.50
in: 4      out: 7.00
```
