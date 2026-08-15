# Changelog — Trader UI / Dynamic Index Upgrade

## V7.1
- Replaced fixed NIFTY/BANK NIFTY navigation with a live Upstox index selector.
- Added daily discovery of domestic index instruments from Upstox's BOD instrument universe, with safe fallbacks.
- Added optional global-index discovery and index-only/context mode.
- Added automatic capability fallback when an index has no active option expiry or usable option chain.
- Automatically infers option strike spacing from the returned chain instead of assuming 50/100 points.
- Rebuilt OI Battlefield with a fixed strike spine, compact OI bars, readable ΔOI, ATM/EOS/EOR anchors, strongest-call/put wall cards and chain-balance summary.
- Improved hero cards, metrics, spacing, responsive layout, tabs, expander styling and index-only view.
- Prevented NIFTY/BANK constituent weights from being incorrectly reused for unrelated indices.
- Existing OI, EOS/EOR, setup, research, backtesting, futures and validation features remain intact.
