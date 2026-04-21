# Pine Script SMC Indicators

## Institutional SMC Analysis Suite (Pine Script v5)

This repository hosts a suite of high-end TradingView indicators focused on Smart Money Concepts (SMC). The scripts utilize advanced Pine Script v5 features, including `matrix` and `array` data structures, to provide accurate, non-repainting market structure analysis.

### Included Indicators

- **OrderBlocks_Matrix**: Uses matrix storage to track and update institutional supply and demand zones dynamically.
- **FairValueGap_Scanner**: High-efficiency detection of price imbalances (FVGs) with automated JSON-structured webhook alerts for execution bridging.
- **LiquiditySweeps**: Logic for identifying liquidity runs above/below key session highs and lows across Asian, London, and New York kill zones.

### Technical Implementation

- **Object-Oriented Logic**: Emulated through user-defined types (UDTs) and matrix manipulations.
- **Non-Repainting**: All calculations are performed on confirmed bars to ensure historical accuracy and reliable backtesting.
- **Webhook Optimized**: Designed to interface with external execution bots via structured JSON payloads.

---

### Intellectual Property Notice

This software and its documentation are the exclusive property of Castle Trade LLC. Unauthorized copying, distribution, or use of these materials constitutes a violation of intellectual property laws and contractual agreements. Access is granted solely for professional evaluation purposes.

© 2026 Castle Trade LLC. All rights reserved.
