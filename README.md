# FactoryPilot AI

FactoryPilot AI is an autonomous factory disruption solver leveraging Groq AI, Google OR-Tools CP-SAT math optimization, and SAP ERP integration.

## Repository Structure

```text
├── backend/
│   ├── adapters/            # SAP Inventory & Supplier Adapters (SQLite & SAP HANA)
│   ├── config.py            # Environment variables & Groq API client
│   ├── groq_parser.py       # Groq AI unstructured text parser module
│   ├── hashchain.py         # Cryptographic SHA-256 audit logger
│   ├── main.py              # FastAPI application entrypoint
│   ├── models.py            # Pydantic v2 schemas (Disruption, SAP Entities)
│   ├── solver.py            # Google OR-Tools CP-SAT math optimizer
│   └── state_machine.py     # Governance State Machine & FSM logic
├── frontend/
│   └── app.py               # Streamlit interactive dashboard
├── manifest.yml             # SAP BTP Cloud Foundry deployment spec
├── Procfile                 # Cloud Foundry process execution command
├── requirements.txt         # Python package dependencies
└── .env.example             # Configuration template
```

## Setup & Getting Started

1. Copy `.env.example` to `.env` and fill in required keys.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run backend:
   ```bash
   uvicorn backend.main:app --reload
   ```
4. Run frontend:
   ```bash
   streamlit run frontend/app.py
   ```
