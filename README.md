# Simplified Accounting System for Sole Traders

This project is a prototype accounting system designed for sole traders.  
It includes receipt processing, expense categorisation, dual-wallet logic (PAYG + Sole Trader), vehicle logbook tracking, real-time tax estimation, ATO rules handling, and export-ready general ledger reporting.

The backend is implemented in Python using a Google Colab notebook.  
The repository includes documentation, mock UI screens, and a structured folder layout to demonstrate a complete software architecture.

---

## Features

### Receipt Processing
- Upload receipts via a mobile-friendly interface (mocked)
- OCR + LLM categorisation (simulated in notebook)
- Confidence scoring with manual review if < 90%
- Apportionment between Business, PAYG, and Personal

### Dual Wallet Architecture
- Every transaction tagged as:
  - PAYG
  - Sole Trader
  - Both
- Automatic cost splitting based on user input

### Vehicle Logbook
- PAYG km counter (cents-per-km method)
- Business km counter (logbook % method)
- Warning at 4,500 km (approaching 5,000 km cap)

### Real-Time Tax Estimation
- Combines PAYG income + Sole Trader profit
- Calculates:
  - Income tax
  - Medicare levy
  - Tax shortfall
  - Weekly saving rate

### ATO Rules Engine
- Instant asset write-off (< $20,000)
- Simplified depreciation pool
- PAYG <$300 rule
- GST collected vs GST paid
- Benchmark alerts for high-risk categories

### General Ledger Reporting
- One central spreadsheet-style table
- Filter by GL code, ATO label, source, category
- Includes:
  - Date
  - Vendor
  - GST
  - GL Code
  - ATO Label
  - Apportionment %
  - Confidence score
  - Receipt link

---

## Folder Structure

