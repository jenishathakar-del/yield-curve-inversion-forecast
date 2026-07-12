# yield-curve-inversion-forecast
# The Liquidation of the 'Common Measure': An Undergraduate Exploration of Algorithmic Price Discrimination vs. Lockean Distributive Justice

## Project Introduction & Intent
As a high school student fascinated by the intersection of computational data and macroeconomics, I wanted to understand how modern dynamic pricing engines isolate individual user data to systematically extract consumer surplus. In standard textbook models, markets naturally seek an equilibrium price that leaves a portion of saved wealth in the hands of the consumer. However, modern digital platforms utilize micro-data tracking to charge individual prices based on specific purchasing power.

I engineered this Python simulation framework to transition past simplified textbook equations and visually map how these real-time dynamic pricing shifts affect market dynamics. By framing this technical transition within the context of recent global consumer blowback against airline fare volatility and real-estate software investigations, this project explores the boundary conditions where market efficiency clashes with moral fairness.

## Theoretical Framework: The Death of the 'Common Measure'
This research frames the transition from flat-rate transactions to algorithmic optimization through John Locke’s 17th-century economic essay *Venditio*. Locke argued for the structural necessity of a **"Common Measure"**—a transparent, predictable market price applied uniformly to all buyers at a given time to preserve individual economic agency. Under Locke's framework, targeting an individual’s specific vulnerability or urgent need to extract a higher price shifts the transaction from fair commerce to economic coercion.

Conversely, modern pricing algorithms utilize tracking layers (cookies, device telemetry, browser history) to calculate an individual's specific maximum **Willingness-to-Pay (WTP)**. In doing so, they execute near-perfect first-degree price discrimination. This project evaluates the resulting trade-off: dynamic pricing maximizes *allocative efficiency* by clearing all available units, but it completely liquidates *distributive justice* by transferring the entire consumer utility zone into corporate revenue.

## Quantitative Simulator Architecture
The computational engine relies on an Object-Oriented Programming (OOP) design pattern built across stateful `Consumer` and `PricingEngine` classes. The simulation environment populates an agent matrix of $N=1,000$ unique buyers. Rather than using arbitrary hardcoded values, agent budgets are modeled using a clipped Gaussian distribution to reflect authentic consumer capital capacity constraints under high-demand travel regimes:

$$WTP_i \sim \max\left(150, \min\left(700, \mathcal{N}(350, 100^2)\right)\right)$$

The system executes and compares two contrasting market regimes:

1. **The Lockean Transparent Flat Market:** Operates at a unified baseline price $P_{\text{flat}}$, where a transaction occurs only if an individual agent's budget matches or exceeds the threshold. The preserved consumer surplus is calculated as:
$$\text{Surplus}_i = WTP_i - P_{\text{flat}} \quad \forall \ WTP_i \ge P_{\text{flat}}$$

2. **The Algorithmic Extraction Framework:** Simulates perfect data visibility where the pricing engine dynamically reads each agent's maximum budget and charges that exact value:
$$P_{\text{dynamic}, i} = WTP_i \implies \text{Surplus}_i = 0$$

![Wealth Extraction Analysis](wealth_extraction_simulation.png)

## Empirical Simulation Results & Analysis
Running the execution script across the consumer agent matrix yields the following structural breakdown:

| Simulation Metric | Lockean Transparent Flat Price | Algorithmic WTP Extraction |
| :--- | :--- | :--- |
| **Units Cleared / Sold** | 513 Units | 1000 Units |
| **Aggregate Corporate Revenue** | $179,550.00 | $356,128.91 |
| **Preserved Consumer Surplus** | $32,185.08 | $0.00 (100% Extracted) |
| **Allocative Deadweight Loss** | $176,578.91 | $0.00 |

### Core Insights From the Model
* **The Efficiency Paradox:** The simulation highlights a major friction point in economic theory. From a purely mathematical perspective, the algorithmic engine is perfectly efficient because it completely eliminates deadweight loss. However, it achieves this by entirely wiping out consumer wealth retention, demonstrating how optimization can run counter to consumer welfare.
* **Systemic Wealth Transfer:** Shifting from a unified transparent baseline to the data-driven framework scales corporate revenue by **98.34%** without creating new inventory or modifying the underlying service. The algorithm performs a highly optimized transfer of utility from the consumer balance sheet straight to corporate revenue, mirroring the real-world performance spikes captured by digital travel and ride-hailing networks.

## Conclusion & Undergraduate Research Takeaways
Building this computational framework forced me to confront the limitations of basic textbook models. When platforms possess the data architecture to track custom footprints, market equilibrium ceases to be a cooperative, mutually beneficial exchange. By exploring these boundaries independently, this portfolio project allowed me to develop tangible skills in object-oriented Python programming, statistical distributions, and microeconomic policy analysis, providing a rigorous foundation for future undergraduate research.
