# AI Agent Design

This system uses an LLM as an “accounting assistant” that interacts with the structured ledger.

---

## 1. Philosophy

The AI does NOT guess.  
It calls Python functions to retrieve real data.

Example:
User: “How much did I spend at Bunnings?”

LLM decides:
→ Call function get_vendor_total("Bunnings")

Backend returns:
→ 1450.00

LLM responds:
“You spent $1,450 at Bunnings this year.”

---

## 2. Tools (Python Functions)

Examples:

- get_vendor_total(vendor)
- get_gl_summary(gl_code)
- project_tax_and_savings()
- get_vehicle_km_summary()
- can_afford_purchase(amount)

The LLM chooses which tool to call.

---

## 3. Workflow

1. User asks a question  
2. LLM analyses intent  
3. LLM selects a tool  
4. Tool runs Python code  
5. Tool returns structured data  
6. LLM explains the result in plain English  

---

## 4. Benefits

- Accurate  
- Auditable  
- Cheap (no sending full spreadsheets to LLM)  
- Fast  
- Compliant with ATO rules  

---

## 5. Future Extensions

- Real OCR  
- Real LLM API  
- Real bank feeds  
- Real SBR export  
