# Cournot vs. Bertrand — Welfare Comparison

A simulation comparing two classic models of duopoly competition — **Bertrand (price competition)** and **Cournot (quantity competition)** — across welfare metrics using Python.

Built as part of the [Arthashaastra](https://github.com/arthashaastra) portfolio: applied economic modelling for real-world market analysis.

---

## What This Does

Two firms. Same market. Different strategic variables. Completely different outcomes.

This notebook solves for the Nash Equilibrium under both models and compares:

| Metric | Bertrand | Cournot |
|---|---|---|
| **Strategic variable** | Price | Quantity |
| **Price at NE** | Lower | Higher |
| **Output at NE** | Higher | Lower |
| **Consumer Surplus** | ✅ Higher | ❌ Lower |
| **Producer Surplus** | ❌ Lower | ✅ Higher |
| **Total Welfare** | ✅ Higher | ❌ Lower |

---

## Models

### Bertrand (Differentiated Products)
Each firm faces demand: `q_i = a - b·p_i + c·p_j`

Firms set prices simultaneously. Best response functions are derived analytically and the Nash Equilibrium is solved numerically using `scipy.optimize.fsolve`.

### Cournot (Linear Inverse Demand)
Market price follows: `P = A - B·(q1 + q2)`

Firms set quantities simultaneously. Same fsolve approach, now in quantity space.

---

## Outputs

1. **Nash Equilibrium** — prices, quantities, and profits under both models
2. **Welfare table** — Consumer Surplus, Producer Surplus, Total Welfare side by side
3. **Bar chart** — visual welfare comparison
4. **Dual best-response plot** — Bertrand in price space vs. Cournot in quantity space
5. **Sensitivity analysis** — how all three welfare metrics shift as marginal cost varies from 50 to 400

---

## Setup
```bash
pip install numpy matplotlib scipy
jupyter notebook cournot_vs_bertrand.ipynb
```

Or open directly in VS Code with the Jupyter extension.

---

## Parameters (easily adjustable)
```python
a  = 1000   # base demand
b  = 5      # own-price sensitivity
c  = 2      # cross-price sensitivity
mc = 200    # marginal cost
```

Change these to model different markets.

---

## Stack

- Python 3
- NumPy
- Matplotlib
- SciPy (`fsolve`)

---

## Part of

→ [Bertrand Competition — Nash Equilibrium Simulation](https://github.com/arthashaastra/pricing-strategies)

*Arthashaastra | Applied Economics & Market Strategy*
