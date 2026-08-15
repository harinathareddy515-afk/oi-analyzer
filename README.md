# OI Pulse Pro — V7.1 Trader UI

Trader-first Streamlit terminal for intraday index analysis using Upstox market data.

## V7.1 changes
- Dynamic index selector based on the Upstox instrument universe, with NIFTY 50 and BANK NIFTY always available as primary fallbacks.
- Full OI/options analytics when an active option chain exists.
- Automatic index-only mode when an instrument does not have a usable option chain; the app never fabricates OI/EOS/EOR data.
- Reworked OI Battlefield for readability: fixed strike column, balanced CE/PE pressure bars, OI values, ΔOI arrows, ATM/EOS/EOR tags and strongest-wall summary.
- Cleaner trader-first visual hierarchy and responsive layout.

## Deployment
Use the repository connected to Streamlit Cloud. Put the Upstox access token in Streamlit Secrets as `UPSTOX_ACCESS_TOKEN`.

## Data note
Upstox's instrument documentation describes the BOD instrument files as the daily universe of tradable instruments and identifies `NSE_INDEX`/`BSE_INDEX` index records with `instrument_type=INDEX`. The app attempts to load that universe daily and falls back safely if the public instrument file is temporarily unreachable.

The OI battlefield uses the option-chain data already supported by the app. For instruments without an option chain, only index price/structure analytics are shown.
