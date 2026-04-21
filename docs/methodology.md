# SMC Quantitative Methodology

## Visual Representation of Alpha

The indicators in this suite serve as the visual analytical interface for Castle Trade's proprietary quantitative strategies. While execution is handled by high-performance C++ and MQL5 components, these scripts provide the necessary real-time market structure visualization for risk monitoring and manual oversight.

### 1. Market Structure Shifts (MSS)
We identify structural changes through matrix-based tracking of swing points. A breach of a matrix-stored swing high/low indicates a potential shift in institutional order flow.

### 2. Institutional Order Blocks (IOB)
Unlike retail supply and demand zones, our IOB detection requires a volume multiplier threshold and an engulfing price action signature. These zones are stored in matrices to track their life cycle—from creation to mitigation or violation.

### 3. Fair Value Gaps (FVG) and Imbalances
Price inefficiencies are flagged as areas of high-priority execution. The `FVG_Scanner` acts as a sensor, pushing alerts to our execution bridge whenever a high-probability imbalance is detected on the institutional timeframes.

### 4. Liquidity Pools and Sweeps
Institutional participants require liquidity to fill large orders. We track Asian, London, and New York session extremes as major liquidity pools. Identifying a "Sweep" (a move beyond these points followed by a reversal) is a core component of our entry logic.

## Integration with Whale Rider

These indicators are designed to be "execution-ready." Each signal includes a structured JSON payload that can be ingested by the `Whale Rider` oms (Order Management System) via webhooks, ensuring a seamless transition from visual signal to automated execution.
