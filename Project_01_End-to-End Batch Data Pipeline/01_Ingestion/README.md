# Ingestion Layer

This folder contains batch ingestion scripts responsible for:
- Reading source CSV files from the datasets folder
- Performing basic schema validation and cleaning
- Writing raw data into the bronze layer with metadata

Each ingestion script handles one data domain independently.
