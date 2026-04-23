# Database Schema

This document describes the data structures used in the simplified accounting system.

---

## 1. Transactions Table

| Field | Type | Description |
|-------|------|-------------|
| id | string | Unique transaction ID |
| date | string | Transaction date |
| vendor | string | Supplier name |
| description | string | Item description |
| total_amount | float | Total cost |
| gst_amount | float | GST component |
| source_type | enum | PAYG / SOLE_TRADER / BOTH |
| business_percent | float | % allocated to business |
| payg_percent | float | % allocated to PAYG |
| personal_percent | float | % allocated to personal |
| gl_code | string | General Ledger code |
| ato_label | string | ATO tax return label |
| is_asset | bool | Whether item is an asset |
| receipt_id | string | Link or ID of receipt |
| confidence | float | AI confidence score |
| needs_review | bool | True if < 90% confidence |

---

## 2. Assets Table

| Field | Type | Description |
|-------|------|-------------|
| id | string | Asset ID |
| transaction_id | string | Linked transaction |
| description | string | Asset name |
| cost | float | Purchase cost |
| business_percent | float | Business use % |
| payg_percent | float | PAYG use % |
| pool_flag | bool | In simplified depreciation pool |
| effective_life_years | int | For PAYG depreciation |
| acquisition_date | string | Purchase date |

---

## 3. Vehicle Trips Table

| Field | Type | Description |
|-------|------|-------------|
| id | string | Trip ID |
| date | string | Trip date |
| km | float | Distance |
| purpose_source | enum | PAYG or SOLE_TRADER |
| logbook_percent | float | Business use % |
| notes | string | Optional notes |

---

## 4. GL Accounts Table

Includes:
- GL code
- Account name
- Type (Revenue, Expense, Asset, Liability, Equity)
- Category (COGS, Operating Expenses, etc.)
- ATO label

See README for full list.

---

## 5. Bank Statements Table (future extension)

| Field | Type | Description |
|-------|------|-------------|
| id | string | Statement ID |
| date | string | Transaction date |
| description | string | Bank description |
| amount | float | Debit or credit |
| balance | float | Running balance |
| matched | bool | Whether reconciled |

---

This schema supports:
- Tax calculations  
- GL reporting  
- ATO compliance  
- Vehicle logbook  
- Asset depreciation  

