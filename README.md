# Mileage Tracker v2

IRS-substantiation-grade mileage log for self-employed Schedule C filers. Records trips with §274(d) fields, resolves time-effective IRS standard mileage rates from database reference data, computes year-end deductions, and exports CSV/PDF reports.

## Features

- Single-user authentication (Argon2id, session expiry, rate-limited login)
- Vehicle management with per-tax-year odometer readings
- Trip CRUD with explicit category selection, late-entered flags, and audit trail
- Time-effective mileage rate resolution (2025/2026 IRS rates seeded)
- Year-end deduction summary with business-use percentage
- IRS-compliant CSV trip log and PDF year summary export
- Ledger Slate design system (Inter + JetBrains Mono)

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python run.py
```

Open http://127.0.0.1:8000 — register the single account on first visit.

## Tests

```bash
pytest -q
```

## Branch

MVP implementation: `feat/mvp-v2`
