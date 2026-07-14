# UnyKorn | Kiwi's Mulligan 1 — Sovereign RWA Platform

This repository hosts the dedicated RWA (Real-World Asset) joint venture platform for **Kiwi's Mulligan 1, LLC** (under Fine Mulligans, Inc.) developed in partnership with UnyKorn LLC.

The platform provides institutional-grade ingestion vetting, BitGo child organization custody, x402 on-chain yield routing, and macro-hedging derivatives to secure and scale the $27,500,000 preferred equity raise for the experiential golf venue in Alpharetta, GA.

---

## 🏗️ Architectural Overview

```
                  ┌────────────────────────────────────────┐
                  │ 1. INGESTION & FORENSIC DD COCKPIT     │
                  │ (Vets Bad Actors, SEC 506(d) & Debt)   │
                  └──────────────────┬─────────────────────┘
                                     │  Passes Compliance Vetting
                                     ▼
                  ┌────────────────────────────────────────┐
                  │ 2. ISOLATED BITGO ENTERPRISE CUSTODY   │
                  │ (3-of-5 Multi-Sig, Whitelist Escrow)   │
                  └──────────────────┬─────────────────────┘
                                     │  Secures $27.5M Raise Capital
                                     ▼
                  ┌────────────────────────────────────────┐
                  │ 3. x402 TOKENIZATION & YIELD ENGINE    │
                  │ (POS Gateway ➔ On-Chain Yield Payouts) │
                  └────────────────────────────────────────┘
```

### 1. Multi-Agent DD Cockpit (`prompts/`)
Sovereign prompts coordinate three distinct agent roles in Google Cloud:
- **Agent 1: Underwriting & Vetting:** Scans deal decks and SEC databases to flag disqualified bad actors (SEC Rule 506(d)) and ring-fence legacy Reg A+ liabilities ($1.2M).
- **Agent 2: BitGo Custody Architect:** Dynamically structures isolated sub-organizations, 3-of-5 multi-sig key matrices, and whitelisted transaction policies.
- **Agent 3: x402 Tokenization Structurer:** Outlines preferred security token rules (Solana Token-2022 / Stellar Anchor) and yield distribution hooks.

### 2. x402 Revenue Yield Dashboard
Sweeps real-world venue Stripe/Toast POS transactions (dining checks, hourly bay bookings) into stablecoin pools, automatically routing monthly yields (9.5% APY preferred return) to verified token holders on-chain.

### 3. Macro Risk Hedging Desk
Integrated Central Limit Order Book (CLOB) matching engine allowing sponsors and lenders (like Castle Placement or LD Capital) to purchase event contracts to hedge regional monetary policy and macroeconomic shifts.

---

## 🛠️ System Inventory

- `index.html` ➔ Premium, glassmorphic RWA portal styled with forest-green & gold country-club tokens.
- `app.js` ➔ Ingestion orchestration, dynamic tab view controller, and live POS log sweep simulations.
- `server.js` ➔ Express API gateway (listening on port `3392`) linking the portal to the backend and the BitGo proxy.
- `clob_server.js` ➔ Central Limit Order Book WebSocket server (listening on port `3398`) supporting price-time priority crossing.
- `delta_hedging_engine.js` ➔ Black-Scholes risk engine computing analytical delta hedges.
- `cryptographic_ledger.js` ➔ SHA-256 hash-chained recorder verifying the immutability of custody sweeps in `default.json`.

---

## 🚀 Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Start the Broker and WebSocket CLOB Servers
```bash
node server.js
```

### 3. Launch Web Server (Local Dev)
Serve the directory on port `9092` (or using python server):
```bash
python -m http.server 9092
```
Navigate to `http://localhost:9092` to access the live Unykorn RWA Command Center.

### 4. Run Multi-User Matching Simulation
```bash
node simulate_multi_user_clob.js
```
